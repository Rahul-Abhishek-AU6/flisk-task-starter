## Vision
Flisk becomes the leanest local execution plane for multi-service development, giving teams and automated coding agents deterministic environment startup without Docker Compose sprawl or bespoke wrapper scripts.

## Next 6 months
| Item | Who it is for | Impact | Confidence | Ease | ICE | Number to watch |
|------|---------------|--------|------------|------|-----|-----------------|
| Agent Worktree Isolation (`flisk worktree`) | Engineers running multiple autonomous coding agents in parallel checkouts | 9 | 9 | 8 | 648 | Workspace setup duration under 3 seconds |
| Lightweight Runtime Adapters (OrbStack and Colima) | Developers looking to cut memory consumption compared to Docker Desktop | 8 | 8 | 8 | 512 | Stack idle RAM reduction above 40 percent |
| Non-Blocking Healthcheck Exclusions (`healthCheck.required: false`) | Teams running microservice suites with non-critical sidecars | 7 | 8 | 9 | 504 | Local stack startup exit-failure rate below 1 percent |

## Not now
Production cluster orchestration and cloud deployment targets, because trying to manage remote infrastructure dilutes local developer velocity and duplicates mature Kubernetes tooling.
