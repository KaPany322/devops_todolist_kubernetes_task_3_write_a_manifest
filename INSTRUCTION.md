To apply all manifests run:
```
kubectl apply -f .infrastructure/namespace.yml
kubectl apply -f .infrastructure/busybox.yml
kubectl apply -f .infrastructure/todoapp-pod.yml
```

To port forward on 8081 run:

```
kubectl port-forward pod/kube2py 8081:8080 -n todoapp
```

To curl todoapp with busybox run:
```
kubectl -n todoapp exec -it busybox -- sh

curl 10.244.0.12:8080
```