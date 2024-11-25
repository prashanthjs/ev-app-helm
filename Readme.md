# Commands
```shell
helm install  -f values.yaml -n dev ev-test .
helm upgrade  -f values.yaml -n dev ev-test .

kubectl port-forward service/ev-frontend1-service 3000:80 -n ev-test
kubectl port-forward service/ev-frontend2-service 3000:8081 -n ev-test

```

General Purpose Node.js API:
```yaml
    resources:
        requests:
            cpu: "250m"
            memory: "256Mi"
        limits:
            cpu: "1000m"
            memory: "1024Mi"

```

High-Traffic or Heavy Node.js API:
```yaml
    resources:
        requests:
            cpu: "750m"
            memory: "1024Mi"
        limits:
            cpu: "2000m"
            memory: "2048Mi"

```