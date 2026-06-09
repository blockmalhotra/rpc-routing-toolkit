# rpc-routing-toolkit

HA Blockchain RPC Platform.

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)
![Docker](https://img.shields.io/badge/docker-ready-blue)
![Kubernetes](https://img.shields.io/badge/k8s-ready-blue)

## Problem
RPC endpoints need HA, failover, rate limit to avoid downtime.

## Architecture
```mermaid
graph TD
    C[Client] --> H[HAProxy]
    C --> N[NGINX]
    H --> R1[RPC1]
    H --> R2[RPC2]
    N --> R1
    N --> R2
```

## Components
HAProxy, NGINX, health checks.

## Quick Start
docker compose up

## Demo
See docker-compose.yml

## Screenshots
screenshots/request-flow.png etc.

## Monitoring
Health checks, logs.

## Security
Rate limit.

## CI/CD
.github/workflows/ci.yml

## Production Deployment
k8s ingress.

## Roadmap
- More backends

## Runbooks
docs/runbook.md

## Troubleshooting
docs/troubleshooting.md
