# git_practice

```yaml
apiVersion: v1
kind: Pod
metadata: 
  name: prom-example
  labels:
    app: prom-example
  annotations:
    prometheus.io/scrape: 'true'    # turn on scraping first
    prometheus.io/path: '/minio/prometheus/metrics'  # the URL path of the endpoint that provides metrics
    prometheus.io/scheme: 'http'              # protocol scheme of the endpoint 
    prometheus.io/port: '9000'                # port of the endpoint
spec:
  containers:
  - image: minio/minio
    name: minio
    args:
    - server
    - /tmp/minio
```
