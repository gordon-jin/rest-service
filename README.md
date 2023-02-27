# Simple REST Service
based on https://spring.io/guides/gs/rest-service/

```
tanzu apps workload apply rest-service \
  --app rest-service \
  --git-repo https://github.com/making/rest-service \
  --git-branch main \
  --type web \
  --label apis.apps.tanzu.vmware.com/register-api=true \
  --param-yaml api_descriptor='{"description":"simple rest api.","location":{"path":"/v3/api-docs"},"owner":"demo","system":"dev","type":"openapi"}' \
  --annotation autoscaling.knative.dev/minScale=1 \
  -n demo \
  -y
```
test
