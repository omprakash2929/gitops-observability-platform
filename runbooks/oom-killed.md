# 🔴 OOMKilled — Out of Memory

## What is this alert?
Pod was killed because it exceeded memory limit.

## Immediate Fix
```bash
# Check which pod was killed
kubectl get pods -n hipster-shop

# See previous logs before kill
kubectl logs <pod-name> -n hipster-shop --previous

# Increase memory limit immediately
kubectl set resources deployment/<name> \
  --limits=memory=1Gi \
  -n hipster-shop
```

## Permanent Fix
Update values.yaml and push to Git — ArgoCD will auto-deploy.

## Common Causes
- Memory limit too low
- Memory leak
- Large data processing
