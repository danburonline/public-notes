#core/softwaredevelopment

The 12-factor **app development methodology is a set of best practices for building modern, scalable, and maintainable web applications.** It was first introduced by Heroku's Adam Wiggins in 2011.

1. **Codebase:** One codebase tracked in version control, many deploys.
2. **Dependencies:** Explicitly declare and isolate dependencies.
3. **Config:** Store config in the environment.
4. **Backing services:** Treat backing services as attached resources.
5. **Build, release, run:** Strictly separate build and run stages.
6. **Processes:** Execute the app as one or more stateless processes.
7. **Port binding:** Export services via port binding.
8. **Concurrency:** [Scale](../../001_private/videos/Decoupling%20of%20scale.md) out via the process model.
9. **Disposability:** Maximise robustness with fast startup and graceful shutdown.
10. **Dev/prod parity:** Keep development, staging, and production as similar as possible.
11. **Logs:** Treat logs as event streams.
12. **Admin processes:** Run admin/management tasks as one-off processes.
