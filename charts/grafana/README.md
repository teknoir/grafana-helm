# Grafana Helm Chart

This chart deploys the Grafana to a Kubernetes cluster.

> The implementation of the Helm chart is right now the bare minimum to get it to work.

## Usage in Teknoir platform
Use the HelmChart to deploy the Grafana to a Device.

```yaml
---
apiVersion: helm.cattle.io/v1
kind: HelmChart
metadata:
  name: grafana
  namespace: default
spec:
  repo: https://teknoir.github.io/grafana-helm
  chart: grafana
  targetNamespace: default
  valuesContent: |-
    deviceId: "orin-demo-se"
    teamspace: "teknoir-ai"
```

## Example values.yaml

```yaml
# TBD
```

## Adding the repository

```bash
helm repo add teknoir-grafana https://teknoir.github.io/grafana-helm/
```

## Installing the chart

```bash
helm install grafana teknoir-grafana/grafana -f values.yaml
```