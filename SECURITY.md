# Politique de sécurité / Security policy

**En bref (FR).** Cette politique couvre tous les dépôts publics de github.com/amineutron (Lyra, fedora-agents, mcp-tracking, neutroncore et les serveurs MCP). Pour signaler une faille, utilisez l'onglet *Security* puis *Report a vulnerability* du dépôt concerné, ou écrivez à amine.neutroncore@gmail.com avec « [security] » dans l'objet. Vous recevrez un accusé de réception sous 7 jours. Merci de ne pas ouvrir d'issue publique pour une faille non corrigée. Il n'y a pas de programme de récompense.

## Scope

All public repositories under github.com/amineutron. These projects run **locally** (LLM agents with hands on virtual machines, backups and home devices): a bug that lets an agent perform an action without confirmation, escape its permission table, or leak local data is considered a security issue.

## Reporting

1. Preferred: the repository's *Security* tab, then *Report a vulnerability* (private vulnerability reporting).
2. Otherwise: amine.neutroncore@gmail.com, subject starting with `[security]`.

Please include the repository, version or commit, steps to reproduce and impact. Do not open a public issue before a fix is available.

## What to expect

- Acknowledgement within 7 days.
- A fix or a mitigation plan within 30 days for confirmed issues, with credit in the release notes if you wish.
- No bug bounty.

## Supported versions

Only the latest release of each repository receives fixes.
