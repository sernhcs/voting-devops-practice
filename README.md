# voting-devops-practice

Voting app desplegada con Docker, Kubernetes, Terraform y Helm.

## Stack
- **Docker** — imágenes de la app
- **kind** — cluster Kubernetes local
- **Helm** — chart en `voting-chart/`
- **GitHub Actions** — CI build+push, CD deploy

## CI/CD
- Push a `main` con cambios en `vote/` → build imagen → push a ghcr.io
- CI exitoso → helm upgrade en el cluster
