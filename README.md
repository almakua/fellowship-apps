# Fellowship Apps

Repository GitOps per le applicazioni del cluster K3s Fellowship.

Gestito da ArgoCD.

## 📁 Struttura

```
fellowship-apps/
├── apps/                    # Manifest delle applicazioni
│   ├── uptime-kuma/
│   ├── ...
│   └── _template/          # Template per nuove app
├── argocd/                  # ArgoCD Applications
│   ├── app-of-apps.yaml    # Root application
│   └── applications/       # Application per ogni app
└── base/                    # Risorse condivise
    └── namespaces/
```

## 🚀 Come aggiungere una nuova app

1. Copia la cartella `apps/_template` con il nome della tua app
2. Modifica i manifest
3. Crea un'Application ArgoCD in `argocd/applications/`
4. Commit e push - ArgoCD deploierà automaticamente!

## 📦 Applicazioni

| App | Namespace | URL | Descrizione |
|-----|-----------|-----|-------------|
| uptime-kuma | uptime-kuma | status.mbianchi.me | Monitoring & Status Page |
| ntfy | ntfy | ntfy.mbianchi.me | Push Notifications Server |

## 🔗 Links

- [ArgoCD Dashboard](https://argocd.mbianchi.me)
- [Cluster Infra Repo](https://github.com/your-org/fellowship)

