# homelab

Creating a SealedSecret from a Helm values.yaml (see the renovate app for an example of use)
kubectl -n <namespace-name> create secret generic <secret-name> --from-file=values.yaml --dry-run=client --output=yaml > values.ext.yaml
kubeseal --format=yaml --cert=pub-sealed-secrets.pem < values.ext.yaml > values-sealed.yaml