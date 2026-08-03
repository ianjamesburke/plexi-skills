# plexi-skills

Agent skills for [Plexi](https://plexiapp.com) — teach your coding agent to drive a running Plexi host.

## Install

```sh
npx -y skills@latest add ianjamesburke/plexi-skills
```

This installs the `plexi-cli` skill into your project's agent directories (Claude Code, Cursor, Codex, and others). Add `-g` to install globally instead.

To pin the skill to a specific Plexi release:

```sh
npx -y skills@latest add "ianjamesburke/plexi-skills#v0.2.0"
```

If a pinned install reports a clone URL with the `#v…` ref embedded in it and
ends with `not valid`, a stale `skills` CLI is being used. Run the command above
instead of bare `npx skills add`.

## Skills

| Skill | What it teaches |
|-------|-----------------|
| `plexi-cli` | The `plexi` CLI surface: panes, apps, contexts, notifications, secrets, agents |

## Versioning

Each skill's frontmatter carries `plexi_version` — the Plexi release it was verified against. Compare it with your installed binary:

```sh
plexi --version
```

If they differ, your skill may describe commands your binary doesn't have (or miss ones it does). Update with:

```sh
npx skills update
```

An unpinned install tracks this repo's `main` branch, which always documents the latest stable Plexi release. Tags (`v0.2.0`, …) match Plexi release versions, so a pinned install stays with its release until you re-add with a newer tag.

## Where this content comes from

The canonical copy of these skills lives in the Plexi source tree; this repo is a mirror, republished at each stable Plexi release. Don't send content PRs here — they'd be overwritten on the next release.
