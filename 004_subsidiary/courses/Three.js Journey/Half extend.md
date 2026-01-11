#core/softwaredevelopment

A half extent (or half-extents) refers to **half the size of an object along each axis from its centre point.** It defines the distance from the centre of a bounding box to its edges, commonly used in collision detection and physics calculations.

## Relationship to Bounding Boxes

Half extents define an **Axis-Aligned Bounding Box (AABB)** - a box whose edges align with the coordinate axes. Given a centre point and half extents, the full bounding box spans:

| Axis | Min | Max |
|------|-----|-----|
| X | `centre.x - halfExtent.x` | `centre.x + halfExtent.x` |
| Y | `centre.y - halfExtent.y` | `centre.y + halfExtent.y` |
| Z | `centre.z - halfExtent.z` | `centre.z + halfExtent.z` |

> [!example]
> A cube with dimensions 10×6×4 has half extents of `(5, 3, 2)`. Its full width is `5 × 2 = 10`.

## Usage in Three.js / Rapier

```javascript
import { CuboidCollider } from '@react-three/rapier'

// Half extents: width/2, height/2, depth/2
<CuboidCollider args={[0.5, 1, 0.5]} /> // Creates a 1×2×1 box

// Extracting half extents from a mesh's bounding box
const box = new THREE.Box3().setFromObject(mesh)
const halfExtents = new THREE.Vector3()
box.getSize(halfExtents).multiplyScalar(0.5)
```

## Why Half Extents?

Physics engines use half extents rather than full dimensions because:

1. **Efficient centre-based calculations** - Collision checks measure distance from centre
2. **Symmetric operations** - Expanding/shrinking boxes is simply adding/subtracting from half extents
3. **Standard in physics APIs** - Rapier, Cannon.js, PhysX all use this convention

## Related

- [[Collider types]] - Different collider shapes available in physics engines
