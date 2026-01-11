#core/softwaredevelopment

In Kubernetes, an Ingress is **an API object that manages external access to services within a cluster.** It provides HTTP and HTTPS route management to services based on the rules defined.

## Purpose

Ingress in Kubernetes is a set of routing rules dictating how external users can access services within a [[Multi-container pod patterns|Kubernetes]] cluster.

## Example

An example of an Ingress might look like the following:

```yaml
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: example-ingress
spec:
  rules:
  - host: myapp.mydomain.com
    http:
      paths:
      - pathType: Prefix
        path: "/"
        backend:
          service:
            name: my-service
            port:
              number: 80
```

In this example, traffic that is directed to `myapp.mydomain.com` is routed to the service named `my-service` on port 80.

## Important Points

- **Ingress Controller**: Before you can use Ingress, an Ingress controller must be present in the cluster. This daemon controller runs on each node and is responsible for fulfilling the Ingress rules.

- **Ports and Protocols**: Ingress does not expose arbitrary ports or protocols. For exposing services other than HTTP and HTTPS to the internet, a service of type `Service.Type=LoadBalancer` or `Service.Type=NodePort` is typically used.

- **DNS Entry**: For the host specified in your Ingress rules, you must have a DNS entry that resolves to the Ingress controller’s external IP address.
