# Contribuer / Contributing

**FR.** Merci de votre intérêt. Pour une correction simple, ouvrez directement une pull request. Pour une fonctionnalité ou un changement de comportement, ouvrez d'abord une issue pour en discuter : cela évite du travail perdu. Les messages de commit suivent le format conventionnel (`feat:`, `fix:`, `docs:`, `chore:`...) en anglais ; le code et la documentation utilisateur des projets restent en français quand c'est déjà le cas. Chaque correction de bug s'accompagne d'un test de régression quand le projet a des tests. Pour **Lyra** (licence AGPL-3.0 avec option commerciale), toute contribution suppose l'acceptation du [CLA](https://github.com/amineutron/lyra/blob/main/CLA.md).

**EN.** Small fixes: open a pull request directly. Features or behaviour changes: open an issue first. Commit messages use the conventional format in English. Bug fixes come with a regression test when the project has a test suite. Contributions to **Lyra** (AGPL-3.0 with a commercial option) require accepting its [CLA](https://github.com/amineutron/lyra/blob/main/CLA.md).

## Checklist for a pull request

- [ ] The change is scoped to one subject.
- [ ] Tests pass locally (`make test`, `pytest` or `npm test` depending on the repository).
- [ ] No personal path, private IP address or secret in the diff.
- [ ] Documentation updated if the behaviour changed.
