# alek-claude-plugins

Marketplace plug­inów do **Claude Code** — kolekcja Aleksandra Nowaka.

## Instalacja

```
/plugin marketplace add aleksanderarielnowak/alek-claude-plugins
/plugin install claude-codex-synapse@alek-claude-plugins
```

Aktualizacja listy: `/plugin marketplace update alek-claude-plugins`

## Pluginy

| Plugin | Opis | Repo |
|---|---|---|
| **claude-codex-synapse** | Synapse — współpraca Claude × Codex (mózg/ręce): auto-delegacja fetch, Excel, obrazów AI, pandoc/docx, bulk + przeglądarka; tryb REVIEW; samodoskonalenie. | `aleksanderarielnowak/claude-codex-synapse` |
| **seodyseusz-gsc** | Google Search Console przez API (Service Account): `/gsc:setup`, `/gsc:query`, `/gsc:sitemaps`, `/gsc:inspect`, `/gsc:report`. Jeden klucz robota = usługi z wielu kont Google (rejestr `--client`). Standalone i jako moduł GSC dla seodyseusz. | `aleksanderarielnowak/seodyseusz-gsc` |

## Dodanie nowego pluginu (na przyszłość)

1. Zbuduj plugin we własnym repo (z `.claude-plugin/plugin.json` + `skills/`, `commands/`, `.mcp.json`, …; komponenty w korzeniu pluginu, NIE w `.claude-plugin/`).
2. Dorzuć wpis do `.claude-plugin/marketplace.json` z `source: { "source": "github", "repo": "owner/repo" }`.
3. Commit + push. Użytkownicy dostaną go po `/plugin marketplace update alek-claude-plugins`.

> Wersjonowanie: pomijamy `version` w aktywnym rozwoju — Claude Code używa commit SHA, więc każdy push = nowa wersja, bez ręcznego bumpowania.
