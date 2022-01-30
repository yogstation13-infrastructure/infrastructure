# Downloading a chart

```shell
helm dependency update
```

# Installing/Upgrading a chart to a cluster
```shell
helm upgrade --install --create-namespace --wait --post-renderer ./kustomize.sh -f values.yaml --namespace <namespace> <releaseName> <chart>
```

# Debugging a chart
```shell
helm template --create-namespace --wait --post-renderer ./kustomize.sh -f values.yaml --namespace <namespace> <releaseName> <chart>
```

# Encrypt secrets
```shell
helm secrets enc secrets.yaml
```

# Decrypt secrets
```shell
helm secrets dec secrets.yaml
```