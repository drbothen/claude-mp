# claude-mp

drbothen's Claude Code plugin marketplace.

## Install a plugin

In a Claude Code session:

```
/plugin marketplace add drbothen/claude-mp
/plugin install <plugin-name>@claude-mp
/reload-plugins
```

## Available plugins

### vsdd-factory

Verified Spec-Driven Development (VSDD) dark factory for software. Full SDLC pipeline: brownfield ingest, spec crystallization, story decomposition, TDD delivery, adversarial review, holdout evaluation, formal verification, and release gating.

- Repo: <https://github.com/drbothen/vsdd-factory>
- Install: `/plugin install vsdd-factory@claude-mp`

## How this marketplace is structured

This repo contains only the marketplace manifest (`.claude-plugin/marketplace.json`). Each plugin lives in its own repository. The marketplace points at each plugin's source via a `git-subdir` reference pinned to the plugin repo's release branch (typically `main`).

This split keeps the marketplace catalog small (one tiny repo) while plugins evolve independently in their own repos. To add a new plugin, append a new entry to `.claude-plugin/marketplace.json` and bump its `version` field whenever the plugin ships a new release.

## License

MIT — see [LICENSE](LICENSE).
