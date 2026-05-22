# 🔴 Pod CrashLoopBackOff

## What is this alert?
Pod is restarting repeatedly — something is wrong inside the container.

## Quick Fix
```bash
# Check logs
kubectl logs <pod-name> -n hipster-shop --previous

# Check events
kubectl describe pod <pod-name> -n hipster-shop

# Restart deployment
kubectl rollout restart deployment/<name> -n hipster-shop
```

## Common Causes
- Missing environment variables
- Database connection failed
- OOM killed
- Application bug
