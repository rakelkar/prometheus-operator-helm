# prometheus-operator-helm
Helm Chart repo for Prometheus operator with fixes rakelkar/charts
(See commits in the repo for what was fixed)

This repo is published as github pages based on instructions from:
https://medium.com/containerum/how-to-make-and-share-your-own-helm-package-50ae40f6c221

Published at: https://rakelkar.github.io/prometheus-operator-helm/index.yaml

To use:
```
helm repo add po https://rakelkar.github.io/prometheus-operator-helm/
helm install po/prometheus-operator
```
Note: If install fails, you need to purge custom resources manually between tries as Helm does not do this..

```
kubectl delete customresourcedefinitions prometheuses.monitoring.coreos.com prometheusrules.monitoring.coreos.com servicemonitors.monitoring.coreos.com alertmanagers.monitoring.coreos.com
```
