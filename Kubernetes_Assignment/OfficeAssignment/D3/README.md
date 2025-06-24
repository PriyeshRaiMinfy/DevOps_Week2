# Assignment D3: Exposing NGINX Deployment with Service – Summary

### Objective

Expose the NGINX Deployment using a Kubernetes Service of type NodePort to allow access from outside the cluster.

---

### I faced a few issues:

- Initially tried to access the pod directly using its IP, which failed since it's only reachable inside the cluster.
- Learned the difference between ClusterIP, NodePort, and how `minikube service` simplifies testing.

---

## Steps Followed

```bash
kubectl apply -f service.yaml
kubectl get svc
minikube service nginx-service
```

---

### Screenshots

> ![Service Created](./image/Screenshot%202025-06-21%20201858.png)  
> ![Service Access](./image/Screenshot%202025-06-21%20202034.png)  
> ![Service Access](./image/Screenshot%202025-06-21%20202051.png)  
> ![Service Access](./image/Screenshot%202025-06-21%20202343.png)  
.
---
 - nginx-deployment-priyesh-live got created
> ![Service Access](./image/Screenshot%202025-06-21%20202618.png)  
> ![Service Access](./image/Screenshot%202025-06-21%20202633.png)  

---

### Output Samples

```
service/nginx-service created

NAME            TYPE       CLUSTER-IP     EXTERNAL-IP   PORT(S)        AGE
nginx-service   NodePort   10.96.0.1      <none>        80:30080/TCP   10s
```

---

### Cleanup
>![Cleanup](./image/Screenshot%202025-06-21%20202804.png)
---