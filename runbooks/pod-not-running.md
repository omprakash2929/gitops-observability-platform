# 🔴 Pod Not Running

## What is this alert?
Pod is not in Running state — could be Pending, Failed, or Unknown.

## Quick Fix
```bash
# Check pod status
kubectl get pods -n hipster-shop

# Check events
kubectl describe pod <pod-name> -n hipster-shop

# Check node resources
kubectl top nodes
```

## Common Causes
- Insufficient resources on node
- Image pull error
- Node not ready
