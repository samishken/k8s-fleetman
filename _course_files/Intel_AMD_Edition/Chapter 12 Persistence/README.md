## Install Prometheus

``` bash
kubectl create ns monitoring
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo add stable https://charts.helm.sh/stable
helm repo update
helm install prometheus prometheus-community/kube-prometheus-stack -n monitoring
kubectl port-forward deployment/prometheus-grafana 3000 -n monitoring

username: admin
password: prom-operator
```
