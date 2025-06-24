# Assignment D2: NGINX Deployment on Kubernetes – Summary

### Objective

Create a scalable Deployment for NGINX instead of a single Pod. This introduces ReplicaSets and ensures the application stays available.

---

### I faced a few issues:

- I had to ensure that the selector matched the pod template labels, otherwise, no pods would get created.

---

## Steps Followed

```bash
kubectl apply -f deployment.yaml
kubectl get deployments
kubectl get rs
kubectl get pods
kubectl describe deployment nginx-deployment
```

---

### Screenshots

> ![Deployment Created](./images/Screenshot%202025-06-21%20191307.png)  
> ![Deployment Pods](./images/Screenshot%202025-06-21%20190748.png)  
> ![ReplicaSet](./images/Screenshot%202025-06-21%20190748.png)

---

### Output Samples

```
deployment.apps/nginx-deployment created

NAME               READY   UP-TO-DATE   AVAILABLE   AGE
nginx-deployment   2/2     2            2           1m
```

---

