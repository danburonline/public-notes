#fundamental/logic

Problem decomposition is the **process of breaking down a complex problem into smaller, more manageable sub-problems.** This approach makes it easier to understand, tackle, and solve intricate challenges by addressing each component individually before integrating them into a comprehensive solution.

## Key Concepts

- **Reduction of Complexity:**  
  Decomposing a problem allows you to isolate and focus on individual aspects, reducing the cognitive load and making each part simpler to solve.
- **Modularity:**  
  Sub-problems can be developed and tested separately when their interfaces and dependencies are explicit. Independent optimisation is not always safe: local improvements can worsen the integrated system.
- **Parallelism:**  
  By splitting a large problem into independent pieces, teams (or processes) can work on different parts simultaneously, accelerating overall progress.
- **Abstraction:**  
  Decomposition helps filter out unnecessary details, allowing you to concentrate on the core elements of the problem without getting lost in complexity.

## Unique Insights

- **Scalability and Adaptability:**  
  A decomposed problem is easier to scale and modify. As requirements change, individual modules can be updated or replaced without overhauling the entire system.
- **Iterative Refinement:**  
  The decomposition approach supports an iterative process where initial solutions to sub-problems can be refined over time, leading to increasingly better overall results.
- **Improved Troubleshooting:**  
  When problems are broken into smaller parts, it becomes easier to pinpoint where issues arise. This leads to faster debugging and more reliable solutions.
- **Foundation for Advanced Methods:**  
  Many sophisticated techniques—such as divide and conquer algorithms, functional decomposition in programming, and microservices in software architecture—are built on the principles of problem decomposition.

---

## Examples

### Software Development

When building a web application, you might:

- **Decompose the project into modules:**
  - **Front-end:** User interface, client-side logic, responsive design.
  - **Back-end:** Server-side processing, database interactions, API endpoints.
- **Further decompose each module:**  
  For example, the user authentication feature can be split into user registration, login, password recovery, and session management.

### Everyday Life

Planning a large family dinner can be decomposed into:

- **Menu Planning:** Decide on courses and dishes.
- **Grocery Shopping:** Make a detailed list based on the menu.
- **Cooking:** Break down recipes into individual steps.
- **Setup and Decoration:** Organise seating, table settings, and ambience.

### Project Management

In constructing a building project:

- **Divide the project into phases:**
  - **Design:** Architectural planning, structural engineering.
  - **Construction:** Laying the foundation, building the framework, finishing.
- **Assign tasks within each phase:**  
  Each phase can have clear milestones and resource allocation, while scheduling respects dependencies between design, construction, and finishing.

## Decomposition needs a composition rule

[Compositional modelling](../_general/compositional_modelling.md) asks how partial solutions connect and whether their meanings remain valid after integration. In software, matching types is only one condition: units, timing, failure behaviour, and assumptions also belong to the interface.

This distinguishes problem decomposition from [coarse-graining](../papers/coarse_graining.md). Decomposition separates interacting parts; coarse-graining merges distinctions within a description. Both reduce cognitive or computational burden, but they perform different operations.
