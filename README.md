# .github

Fichiers communautaires par défaut des dépôts publics d'amineutron : politique de sécurité, code de conduite, guide de contribution et modèles de tickets. GitHub les applique automatiquement à tout dépôt du compte qui n'a pas les siens.

Default community health files for amineutron's public repositories (security policy, code of conduct, contributing guide, issue and pull request templates).

## Workflows réutilisables

| Workflow | Usage |
|---|---|
| `python-ci.yml` | tests avec uv (matrice 3.11/3.12), lint ruff, garde-fou anti chemins personnels |
| `node-ci.yml` | npm ci, build, tests, audit haute/critique, garde-fou |
| `release-pypi.yml` | build et publication PyPI par Trusted Publishing |

Exemple dans un dépôt :

```yaml
jobs:
  ci:
    uses: amineutron/.github/.github/workflows/python-ci.yml@main
```
