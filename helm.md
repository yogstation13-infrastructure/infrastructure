# Downloading a chart

```shell
helm pull --untar <repo>/<chart> --version <chartVersion>
```

# Installing/Upgrading a chart to a cluster
```shell
helm upgrade --install --create-namespace --wait --post-renderer ./kustomize.sh -f values.yaml --namespace <namespace> <releaseName> <chart>
```

# Debugging a chart
```shell
helm template --create-namespace --wait --post-renderer ./kustomize.sh -f values.yaml --namespace <namespace> <releaseName> <chart>
```