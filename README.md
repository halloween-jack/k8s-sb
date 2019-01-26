# k8s examples
from [Docker/Kubernetes 実践コンテナ開発入門](https://gihyo.jp/book/2018/978-4-297-10033-9)

## Pod
```
kubectl apply -f simple-pod.yaml
```

Pod内のコンテナ内に入る
```
kubectl exec -it simple-echo sh -c nginx
```

## RepicaSet
```
kubectl apply -f simple-replicaset.yaml
```

## Deployment
```
kubectl apply -f simple-deployment.yaml
kubectl rollout history deployment echo --revision=1
kubectl rollout undo deployment echo
```

## Service
```
kubectl apply -f simple-service.yaml
```

## Ingress
IngressをローカルのK8s環境で動作させる場合Nginx Ingress Controllerが必要(https://kubernetes.github.io/ingress-nginx/deploy/)
```
kubectl apply -f simple-service.yaml
```
