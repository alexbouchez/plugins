# Alex Bouchez — Claude Code plugins

Marketplace personnelle pour mes plugins Claude Code (ghostwriting LinkedIn + X, gestion devis Dougs).

## Install

```
/plugin marketplace add alexbouchez/plugins
```

Puis installe les plugins :

```
/plugin install linkedin-ghostwriter@alexbouchez   # accès privé requis
/plugin install x-ghostwriter@alexbouchez          # accès privé requis
/plugin install dougs@alexbouchez
```

## Plugins

| Plugin | Visibilité | Repo | Description |
|---|---|---|---|
| `linkedin-ghostwriter` | Private | alexbouchez/linkedin-ghostwriter | Rédige des posts LinkedIn viraux + lead magnets. DB ~10k posts classifiés. |
| `x-ghostwriter` | Private | alexbouchez/x-ghostwriter | Rédige des posts X/Twitter fidèles au style de l'auteur (scraping + génération). |
| `dougs` | Public | [alexbouchez/dougs](https://github.com/alexbouchez/dougs) | Gestion des brouillons de devis Dougs via fetch direct + cookie session. Brouillon-only. |

## Architecture

Hub-and-spoke : ce repo héberge la marketplace ; chaque plugin vit dans son propre repo. Le plugin `dougs` utilise `git-subdir` source (son code vit dans `./plugin/` du repo) — c'est sa structure historique préservée.

Pas de version pinning : les users récupèrent toujours la dernière version.
