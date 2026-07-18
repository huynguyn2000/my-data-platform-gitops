# my-data-platform-gitops

GitOps source of truth for a local data platform, deployed by [ArgoCD](https://argo-cd.readthedocs.io/).

**The rule:** nothing is deployed by hand. Change YAML here → push → ArgoCD makes the cluster match.

## Layout

```
apps/
  postgres/        # Phase 2 — Postgres via raw Kubernetes manifests
```

## Phases

- **Phase 2** — Postgres deployed from raw manifests (`apps/postgres`).
- **Phase 3** — Kafka/Trino via Helm charts (coming).
- **Phase 4** — App-of-Apps root that deploys everything (coming).
