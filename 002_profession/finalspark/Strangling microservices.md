#core/softwareengineering

![[strangling.jpg]]

The strangler fig pattern is a **strategy for incrementally migrating a monolithic system to microservices** by gradually replacing specific functionalities until the original system can be decommissioned. Named after strangler fig trees that grow around host trees and eventually replace them.

## Why Strangle?

| Approach | Risk | Downtime | Cost |
|----------|------|----------|------|
| Big bang rewrite | High | Significant | Front-loaded |
| Strangler pattern | Low | Minimal | Distributed |

- **Avoid "second system syndrome"**: Rewrites often fail or exceed timelines
- **Continuous delivery**: New services can ship independently
- **Reversibility**: Easy to roll back individual migrations
- **Learning**: Team gains microservices experience incrementally

## The Process

### 1. Identify Seams

Find **natural boundaries** in the monolith where functionality can be extracted:
- Distinct business domains (e.g., payments, inventory)
- High-change areas that would benefit from independent deployment
- Performance bottlenecks requiring different scaling

### 2. Build the Strangler Facade

Insert a **routing layer** (API gateway, reverse proxy) between clients and the monolith:
- Initially routes 100% of traffic to monolith
- Enables gradual traffic shifting to new services
- Provides single entry point for clients

### 3. Extract and Redirect

For each capability:
1. **Build** the microservice implementing that functionality
2. **Test** thoroughly (shadow traffic, canary deployment)
3. **Redirect** traffic from monolith to new service
4. **Remove** dead code from monolith

### 4. Repeat Until Complete

Continue extracting services until the monolith is either:
- Fully decomposed (ideal)
- Reduced to a stable, maintainable core (pragmatic)

## Anti-Patterns to Avoid

> [!warning] Common Mistakes
> - **Distributed monolith**: Services too tightly coupled, requiring coordinated deployments
> - **Premature extraction**: Moving code before understanding domain boundaries
> - **Ignoring data**: Extracting services without addressing shared database dependencies
> - **No facade**: Direct client-to-service calls create migration friction

## When to Use

**Good candidates:**
- Monoliths with clear domain boundaries
- Systems requiring different scaling per component
- Teams ready for distributed systems complexity

**Poor candidates:**
- Small applications without scaling needs
- Teams lacking DevOps maturity
- Tightly coupled data models without clear ownership

## Tools and Techniques

- **API Gateways**: Kong, AWS API Gateway, Traefik
- **Service Mesh**: Istio, Linkerd (for traffic management)
- **Feature Flags**: Gradual rollout control
- **[[Pull-based deployments]]**: GitOps for managing service configurations

> [!tip] Start Small
> Begin with a low-risk, well-understood component. Success builds confidence and reveals patterns for subsequent extractions.
