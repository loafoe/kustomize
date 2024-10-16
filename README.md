# kustomize

A collection of kustomize scripts used for various projects


## k8s-observability

```shell
argocd app create k8s-observability \
    --repo https://github.com/loafoe/kustomize \
    --revision main \
    --path k8s-observability \
    --dest-namespace argocd \
    --dest-server https://kubernetes.default.svc \
    --config-management-plugin envsubst-plugin \
    --plugin-env host=gw.local
    --sync-policy auto \
    --self-heal \
    --auto-prune
```
