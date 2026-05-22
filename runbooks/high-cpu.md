# 🟡 High CPU Throttling

## What is this alert?
Pod CPU is being throttled more than 25%.

## Quick Fix
```bash
# Check CPU usage
kubectl top pods -n hipster-shop

# Increase CPU limit
resources:
  limits:
    cpu: "500m"  # increase this
  requests:
    cpu: "250m"
```

## Common Causes
- CPU limit too low
- Traffic spike
- Inefficient code
