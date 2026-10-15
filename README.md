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
| **claude-codex-webdev-inc** | Budowa i modyfikacja stron WordPress od zera (źródło o firmie → research → gotowa, edytowalna strona). Metoda nadrzędna: budowa **sekcjami** komponentami buildera, drabina builder → builder+wtyczka → blok HTML jako wyjątek. Playbooki branżowe, biblioteka sekcji, hardened recipes, QA headless. | `aleksanderarielnowak/claude-codex-webdev-inc` |
| **nova** | Dyrygent sieci własności internetowych NOVA: budowa i eksploatacja serwisu w sześciu etapach z bramkami, role, zamki etapów, stan w teczce własności. | `aleksanderarielnowak/nova-ai` (katalog `nova/`) |
| **nova-pracownia** | Warsztat mediowy NOVA: Grafik i Reżyser. Biblioteka stockowa, kadry i ujęcia przez fal.ai, montaż ffmpeg, z cennikiem i limitem wydatku. | `aleksanderarielnowak/nova-ai` (katalog `nova-pracownia/`) |
| **seo-sztafeta** | Przekazuje wątki Claude Code między komputerami przez Dysk Google (pałeczki). | `aleksanderarielnowak/seo-sztafeta` |

## Dodanie nowego pluginu (na przyszłość)

1. Zbuduj plugin we własnym repo (z `.claude-plugin/plugin.json` + `skills/`, `commands/`, `.mcp.json`, …; komponenty w korzeniu pluginu, NIE w `.claude-plugin/`).
2. Dorzuć wpis do `.claude-plugin/marketplace.json` z `source: { "source": "github", "repo": "owner/repo" }`; gdy plugin siedzi w podkatalogu repo (jak NOVA), użyj `{ "source": "git-subdir", "url": "https://github.com/owner/repo.git", "path": "katalog" }`.
3. Commit + push. Użytkownicy dostaną go po `/plugin marketplace update alek-claude-plugins`.

> Wersjonowanie: pomijamy `version` w aktywnym rozwoju — Claude Code używa commit SHA, więc każdy push = nowa wersja, bez ręcznego bumpowania.
