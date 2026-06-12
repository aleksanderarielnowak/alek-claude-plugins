# aleksander-plugins

Marketplace plug­inów do **Claude Code** — kolekcja Aleksandra Nowaka (netin.pro).

## Instalacja

```
/plugin marketplace add aleksanderarielnowak/aleksander-plugins
/plugin install claude-codex-synapse@aleksander-plugins
```

Aktualizacja listy: `/plugin marketplace update aleksander-plugins`

## Pluginy

| Plugin | Opis | Repo |
|---|---|---|
| **claude-codex-synapse** | Synapse — współpraca Claude × Codex (mózg/ręce): auto-delegacja fetch, Excel, obrazów AI, pandoc/docx, bulk + przeglądarka; tryb REVIEW; samodoskonalenie. | `aleksanderarielnowak/claude-codex-synapse` |

## Dodanie nowego pluginu (na przyszłość)

1. Zbuduj plugin we własnym repo (z `.claude-plugin/plugin.json` + `skills/`, `commands/`, `.mcp.json`, …; komponenty w korzeniu pluginu, NIE w `.claude-plugin/`).
2. Dorzuć wpis do `.claude-plugin/marketplace.json` z `source: { "source": "github", "repo": "owner/repo" }`.
3. Commit + push. Użytkownicy dostaną go po `/plugin marketplace update aleksander-plugins`.

> Wersjonowanie: pomijamy `version` w aktywnym rozwoju — Claude Code używa commit SHA, więc każdy push = nowa wersja, bez ręcznego bumpowania.
