# vault-mirror

**vault-mirror turns a folder of markdown notes into a set of evidence-linked reports about the person who wrote them.** You copy the folder next to your notes, tell any agent with file access (Claude Code, Cursor, Codex) to read prompts/00-start.md, and it works through years of your writing and returns 16 reports: how you think, what you value against where your attention actually goes, why projects die, and a 30-day plan built around your real failure patterns. Every claim is backed by a quote or a link to a specific note. Bonus prompts write a letter from your past self, a reusable style prompt that writes like you, and a system prompt that advises like your most honest friend. There is nothing to install and no dependencies: the repository is prompts.

<div align="center">

[![Star on GitHub](https://img.shields.io/github/stars/N23eos/vault-mirror?style=for-the-badge&logo=github&label=Star%20this%20repo&color=FFD700&labelColor=1a1a1a)](https://github.com/N23eos/vault-mirror)

</div>

## What you get

**Core (`prompts/`, runs automatically in order):**

| # | Report | One line |
|---|--------|----------|
| 01 | Corpus Survey | Census of your vault + the methodology everything else uses |
| 02 | Thinking Portrait | How your mind works, judged by how you actually write |
| 03 | Chronicle | Your story by period: themes, turning points, silences |
| 04 | Cycles | The mechanics of what you start, abandon, and finish |
| 05 | Values vs Behavior | What you say matters vs where your attention goes |
| 06 | Strengths | Real, evidenced strengths — including underused ones |
| 07 | Growth Areas | 3–5 highest-leverage areas, prioritized, not a wish list |
| 08 | Open Questions | The questions your notes keep asking without answering |
| 09 | Executive Summary | The whole thing in a ten-minute read |
| 10 | 30-Day Action Plan | A plan designed around your real failure patterns |

**Bonus (`bonus/`, run on request):**

| Report | One line |
|--------|----------|
| Letter to Past Self | A letter using only wisdom your notes prove you gained |
| Author Voice | A reusable style prompt that writes like you |
| Digital Advisor | A "second self" system prompt that advises like your most honest friend |
| Advisor Bot Guide | How to turn that prompt into an actual bot, any stack |

**Hard mode (`hard-mode/`, opt-in, uncomfortable by design):**

| Report | One line |
|--------|----------|
| Blind Spots | Self-narratives your own record contradicts |
| Failure Patterns | The anatomy of how your projects actually die |

## Quickstart

1. Copy this repository into your vault (or a sibling folder).
2. Open your AI agent with file access to the vault.
3. Say: `Read prompts/00-start.md and begin.`
4. Reports appear in `<vault>/Analysis/`, one file per module, in the
   dominant language of your vault. Progress is checkpointed in
   `Analysis/_progress.md`, so an interrupted session resumes where it stopped.

## Running it

| Agent | How |
|-------|-----|
| Claude Code | `cd` into the vault, run `claude`, paste the quickstart line |
| Cursor | Open the vault as a folder, ask the agent the quickstart line |
| Codex CLI | Run it in the vault directory, paste the quickstart line |
| Anything else | Any agent that can read/write files in the folder works |

## Privacy — read this

Your notes will be sent to whatever model powers your agent. If your vault
contains things you would not paste into that model's chat window, don't run
this on it — or use a **local model** (Ollama, LM Studio, etc. with a
file-capable agent), which keeps everything on your machine.

The output in `Analysis/` is a concentrated psychological profile of you. If
your vault is under git, add `Analysis/` to `.gitignore` before running.

## Hard mode warning

The two `hard-mode/` modules are intentionally blunt: they hunt
self-contradictions and dissect failures. They run only if you explicitly ask,
and the agent will confirm first. This is analysis of your own written record,
**not therapy** — if you're in a rough place, a well-formatted list of your
failure patterns is not what you need; a human is.

## Example output (fictional)

> **From 04-cycles.md** *(fictional persona, illustrative only)*
>
> The typical cycle runs 6–8 weeks: an intense spark phase with daily notes
> (`[[2023-03-04 gamedev engine idea]]`), a peak around week 3, then entries
> shift from building to meta-planning (`[[Rethinking my roadmap]]` —
> `likely` the first wobble signal), and by week 6 the topic disappears.
> Of 14 undertakings found, 3 were finished — all three had an external
> deadline. `confirmed`

## FAQ

**My vault is small (a few dozen notes).** It works, but confidence markers
will lean `hypothesis`. The chronicle and cycles modules need history to bite.

**My notes aren't Obsidian.** Fine. Anything that is a folder of `.md` files
works. Wikilinks in reports degrade to plain references.

**My vault is in language X.** Prompts are English; reports are written in
your vault's dominant language automatically.

**Can I run just one module?** Yes — run `00-start.md` plus `01`, then any
module you want. Only 09 and 10 require the others.

## License

MIT — see [LICENSE](LICENSE).

## Support

If this project was useful to you, feel free to support further development:

[![ETH](https://img.shields.io/badge/ETH-0x7777...88C4-blue?logo=ethereum&style=flat-square)](https://etherscan.io/address/0x77777da54702AC8789D53fc7cC6201C29a1A88C4)
[![Donate](https://img.shields.io/badge/donate-crypto-orange?style=flat-square)](https://etherscan.io/address/0x77777da54702AC8789D53fc7cC6201C29a1A88C4)
