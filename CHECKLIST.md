# Checklist de parité d'emballage

À cocher avant toute soumission d'un dépôt à un annuaire (registre MCP, awesome-mcp-servers, Glama, PulseMCP, Smithery, mcp.so, Ollama) ou avant une release annoncée. Elle existe parce que les dépôts comparables qui ont des centaines d'étoiles ont tous ces éléments, et que les annuaires les lisent automatiquement.

## Fiche GitHub
- [ ] Description en une phrase, en anglais, avec le mot-clé de positionnement (sovereign / local-first / self-hosted) quand il s'applique.
- [ ] Topics : `mcp`, `mcp-server`, le langage, le domaine (`home-automation`, `devops`...), et `local-first` / `self-hosted` / `sovereign-ai` / `on-prem` selon le cas.
- [ ] Homepage renseignée : page PyPI ou npm du paquet, sinon la documentation.
- [ ] Licence déclarée et détectée par GitHub (MIT pour les serveurs, AGPL-3.0 + licence commerciale pour lyra).

## README
- [ ] Première ligne : titre, badges (tests, licence, version publiée).
- [ ] Résumé en anglais en tête, contenu détaillé en français ensuite.
- [ ] Installation en une ligne : `uvx <paquet>` ou `npx <paquet>`, et le bloc `mcpServers` prêt à coller.
- [ ] Démo enregistrée (GIF ou vidéo) avec le script qui la régénère.
- [ ] Table des outils générée depuis le code (pas écrite à la main).
- [ ] Marqueur de propriété du registre MCP : `<!-- mcp-name: io.github.amineutron/<dépôt> -->` (PyPI, NuGet) ou `mcpName` dans package.json (npm).
- [ ] Section « Écosystème Lyra » qui relie les dépôts entre eux.

## Paquet et release
- [ ] Paquet publié sur PyPI ou npm par Trusted Publishing, depuis un `release.yml` autonome (les registres refusent les workflows réutilisables).
- [ ] Code dans un paquet à son nom (`<nom>_mcp/`), jamais de module de premier niveau générique (`server`, `utils`...) : deux serveurs installés dans le même environnement s'écraseraient (constaté sur catt/denon/pylips avant la 0.3.0). Un `server.py` minimal à la racine peut rester pour lancer depuis un clone, hors du wheel.
- [ ] `<commande> --help` et `--version` répondent sans configuration ni appareil, et sans démarrer le serveur ni ouvrir de journal (vérifié depuis un dossier vide avec `uvx` / `npx`).
- [ ] Installer ensemble les serveurs publiés dans un seul environnement et vérifier que chaque commande répond.
- [ ] `server.json` valide (`mcp-publisher validate`) et version identique à celle du paquet publié.
- [ ] Job `registry` dans `release.yml` : `mcp-publisher` (version et sha256 figés), `login github-oidc`, `publish`. Plus de connexion manuelle ; `workflow_dispatch` relance le registre seul.
- [ ] CHANGELOG.md à jour ; notes de release générées par git-cliff (`cliff.toml`).
- [ ] Release GitHub avec le wheel/sdist ou le tarball et les attestations.
- [ ] Tag signé pour lyra et fedora-agents.

## Communauté
- [ ] CONTRIBUTING.md, CODE_OF_CONDUCT.md, SECURITY.md (hérités de ce dépôt `.github` si absents).
- [ ] Modèles d'issue et de PR (hérités).
- [ ] Aucun chemin personnel, adresse privée ni secret : garde-fou CI `no-personal-paths` et, en local, hooks git globaux `~/dotfiles/git/hooks` (commit et push). Exemples génériques admis : `/home/user`, `192.168.122.x`, plages de documentation (`192.0.2.x`).

## Soumission
- [ ] Entrée awesome-mcp-servers : `- [amineutron/<dépôt>](url) [badge Glama] 🐍 ou 📇, 🏠, 🐧 - description courte. \`uvx <paquet>\``.
- [ ] Fiche Glama revendiquée (connexion GitHub), badge ajouté au README une fois servi.
- [ ] Inscrit dans le registre officiel : `curl "https://registry.modelcontextprotocol.io/v0/servers?search=amineutron"`.
