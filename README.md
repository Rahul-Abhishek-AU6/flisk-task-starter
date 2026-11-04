# Polyglot Voting Application

Local five-service application runtime configured with Flisk.

## Quickstart

Run the stack locally:

```bash
npx @flisk-sh/flisk up
```

Service endpoints after startup:
- Vote interface: http://localhost/api/vote
- Results interface: http://localhost/api/result

Inspect stack health, Traefik routes, and container statuses:

```bash
npx @flisk-sh/flisk doctor
npx @flisk-sh/flisk networks
```

## What was hard
Translating Docker Compose host port mappings required manual adjustments because Flisk routes public web traffic through Traefik instead of publishing raw container ports to the host interface.
The result service uses Node inspection on port 9229 alongside the HTTP server, which needed container entrypoint overrides so nodemon debug flags stayed intact without breaking internal networking.
The .NET worker depends on both Postgres and Redis readiness probes, so startup ordering had to wait for database socket initialization rather than just container boot status.
