# 🟡 High Memory Usage

## What is this alert?
Pod memory usage is above 85% of its limit.

## Quick Fix
```bash
# Check memory usage
kubectl top pods -n hipster-shop

# Check limits
kubectl describe pod <pod-name> -n hipster-shop | grep -A3 Limits

# Increase memory limit in values.yaml
resources:
  limits:
    memory: "512Mi"  # increase this
```

## Common Causes
- Memory leak in application
- Traffic spike
- Memory limit too low
