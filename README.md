


### Create cluster
```
kind create cluster --config kind-cluster.yaml
kind update cluster --config kind-cluster.yaml
flux bootstrap github \
  --owner=son-la \
  --repository=flux-fleet \
  --branch=main \
  --path=clusters/snorlax-local \
  --token-auth \
  --components-extra=image-reflector-controller,image-automation-controller \
  --version=v2.2.3

```