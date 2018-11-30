# git_practice

```yaml
apiVersion: v1  
kind: Pod
metadata: 
  name: prom-example
  labels:
    app: prom-example
spec:
  containers:
  - image: minio/minio
    name: minio
    args:
    - server
    - /tmp/minio
```
