To edit secret for runner:
1. get secret: kubectl get secret sitebuilds-gb5-v3-dockerconfig-secret -n sitebuilds -o yaml --cluster=gb5-st-unityv3
2. edit secret: kubectl edit secret sitebuilds-gb5-v3-dockerconfig-secret -n sitebuilds -o yaml --cluster=gb5-st-unityv3

k9s:
- :ctx to view all contexts
- :ns to view all namespaces
- /{input} to filter by input
- :pods to view all pods in namespace
- :secrets to view secrets in pod
- l on pod to view logs
- e on secret to edit it
  - data is base64 encoded. Decode in online decoder
