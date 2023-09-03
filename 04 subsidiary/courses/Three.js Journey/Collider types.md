#lead/spatialcomputing

![[colliders.jpeg]]

- **CuboidCollider:** Creates a cuboid (box) shape based on provided width, height, and depth arguments. Useful for basic box collisions.

- **SphereCollider:** Creates a sphere shape based on provided radius argument. Useful for basic spherical collisions.

- **CylinderCollider:** Creates a cylinder shape based on provided radius and height arguments. Useful for cylindrical objects like poles or pipes.

- **CapsuleCollider:** Creates a capsule (rounded cylinder) shape based on provided radius and height arguments. Useful for character controllers or rounded shapes.

- **ConvexHullCollider:** Creates a convex hull representing the collider shape from the given mesh geometry. Can be expensive to calculate but good for complex shapes.

- **TrimeshCollider:** Creates a collider from the triangle mesh geometry of the given mesh. Less expensive than convex hull but less accurate.

- **HeightfieldCollider:** Creates a collider from a heightfield/terrain map. Useful for terrain collisions.

- **BallCollider:** Alias for SphereCollider.

- **MeshCollider:** Generates a collider automatically based on the given mesh and collider type (trimesh, convex hull etc).

- **CompoundCollider:** Allows combining multiple collider shapes into a single compound collider.
