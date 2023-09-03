#core/softwareengineering 

Kubernetes supports the design of multi-container pods, **where multiple containers are deployed in the same pod.** In these scenarios, the containers share the same network and storage resources, allowing them to cooperate and provide combined functionality. Here are some common multi-container pod patterns:

## 1. Sidecar Pattern

In the sidecar pattern, the main application is accompanied by one or more helper containers that enhance or complement its functionality. The sidecar container can do tasks like log or data change watching, monitoring, proxying, etc.

```
apiVersion: v1
kind: Pod
metadata:
  name: myapp-pod
spec:
  containers:
  - name: myapp-container
    image: myapp
  - name: my-log-watcher
    image: log-watcher
```

## 2. Ambassador Pattern

The ambassador pattern is used to connect containers with the outside world. The ambassador container can be used as a proxy that sends network requests to other services on behalf of the main application container.

```
apiVersion: v1
kind: Pod
metadata:
  name: myapp-pod
spec:
  containers:
  - name: myapp-container
    image: myapp
  - name: myapp-ambassador
    image: ambassador
```

## 3. Adapter Pattern

The adapter pattern normalizes and exposes the monitoring data from the main application to be consumed in a standard way. The adapter container transforms the output into a format that monitoring tools can understand.

```
apiVersion: v1
kind: Pod
metadata:
  name: myapp-pod
spec:
  containers:
  - name: myapp-container
    image: myapp
  - name: myapp-adapter
    image: adapter
```

## 4. Init Pattern

In the Init pattern, one or more init containers are started before the app containers of a pod. These init containers can contain utilities or setup scripts not present in the app image. They are used when you need to perform setup tasks before the main container starts.

```
apiVersion: v1
kind: Pod
metadata:
  name: myapp-pod
spec:
  initContainers:
  - name: init-myapp
    image: myapp-init
  containers:
  - name: myapp-container
    image: myapp
```

## Advantages of Multi-Container Pods

- **Shared resources**: Containers inside a pod share the same network space, which means they can communicate with each other using `localhost`. They can also share storage volumes.
- **Simplified communication**: The inter-container communication is simplified as they're deployed on the same host.
- **Tight coupling**: If the containers are tightly coupled and need to be scaled together, deploying them in the same pod simplifies the process.

## Disadvantages of Multi-Container Pods

- **Limited scalability**: Since all containers in a pod are scheduled on the same node, you can't scale them individually. They have to be scaled together.
- **Shared resources can be a disadvantage**: If one container uses up most of the resources, it can starve the other containers, leading to performance issues.
- **Failure propagation**: If one container fails, it could bring down the entire pod.