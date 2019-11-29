# flux-deploy

Install Flux in your cluster, pointing to this repo.

```
kubectl create ns flux

fluxctl install \
--git-user=cheesybot \
--git-email=bot@cheesy.dev \
--git-url=git@github.com:cheesydev-labs/flux-deploy \
--git-path=namespaces,workloads \
--namespace=flux | kubectl apply -f -
```

Add ssh deploy key in the repo's settings.
```
fluxctl identity --k8s-fwd-ns flux
```

