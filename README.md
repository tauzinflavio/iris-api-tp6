# Kit de démarrage — TP6 (Docker, ACR, Kubernetes/AKS)

ECE Paris — Distributed Systems & Cloud Computing — Dr. BENNAI Soufia — année 2026-2027

Ce dossier contient **tous les fichiers du lab, déjà écrits et testés** (Python 3.13,
Docker 29, Kubernetes 1.36). Vous n'avez rien à recopier depuis le PDF : lisez chaque
fichier en suivant l'énoncé, puis exécutez les commandes.

| Fichier / dossier | Rôle | Partie |
|---|---|---|
| `tp6.env.example` | Modèle du fichier de variables (à copier en `~/tp6.env`) | 0 |
| `scripts/verifier-outils.sh` | Vérifie Docker, az, kubectl, minikube, git | 0 |
| `scripts/trouver-region.sh` | Trouve une région autorisée et une taille de VM pour AKS | 0 et 4 |
| `train.py` | Entraîne le modèle Iris et l'enregistre | 1 |
| `app/main.py` | API FastAPI (prédiction, santé, statistiques) | 1 |
| `tests/test_api.py` | Tests automatiques (pytest) | 1 et 5 |
| `requirements*.txt` | Dépendances Python, versions figées | 1 |
| `Dockerfile`, `.dockerignore` | Construction de l'image | 1 |
| `Dockerfile.naive` | Contre-exemple à comparer | 1 |
| `compose.yaml` | API + Redis (facultatif) | 1 |
| `k8s/` | Manifestes Kubernetes | 3 et 4 |
| `k8s/optional/` | Ingress, KEDA (facultatifs) | 3, bonus |
| `partie5/deploy.yml` | Workflow GitHub Actions, à copier dans `.github/workflows/` **seulement en Partie 5** | 5 |

Démarrage rapide (Git Bash sous Windows, Terminal sous macOS/Linux) :

```bash
cd iris-api
cp tp6.env.example ~/tp6.env      # puis éditez vos initiales, région et taille
bash scripts/verifier-outils.sh
```

Ne commitez jamais de secret : `~/tp6.env` reste dans votre dossier personnel,
hors du dépôt.
