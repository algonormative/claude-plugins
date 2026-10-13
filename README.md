# algonormative Claude Code plugins

A [Claude Code plugin marketplace](https://code.claude.com/docs/en/plugins/create-marketplace) of mods by algonormative.

## Install

In a terminal `claude` session, add the marketplace once:

```
/plugin marketplace add algonormative/claude-plugins
```

Then install what you want:

```
/plugin install subagents-plus@algonormative
/plugin install beads-band@algonormative
/plugin install canvas@algonormative
```

Outside a session use `claude plugin marketplace add algonormative/claude-plugins` and `claude plugin install <name>@algonormative`. A plugin installed at the user scope also loads in the desktop app's Code tab.

Updates arrive when a plugin's version changes. Run `/plugin marketplace update algonormative`, or turn on auto-update for this marketplace under `/plugin` → Marketplaces.

These are mods: they run hooks with your permissions. Read a plugin's source, or run `claude plugin validate` on it, before you install it. They need a Claude Code build with function-hook mods (2.1.295 or newer).

## Plugins

| Plugin | What it does | Repo |
|---|---|---|
| `subagents-plus` | See your subagents: a `/subagents` pane with an expandable live tree of every subagent (activity, tokens, transcripts) and a timeline, live cards on Agent rows, and a band above the prompt | [algonormative/subagents-plus](https://github.com/algonormative/subagents-plus) |
| `beads-band` | A band above the prompt for a [beads](https://github.com/steveyegge/beads) task queue: the ready count when idle, the task this session claimed while it works | [algonormative/beads-band](https://github.com/algonormative/beads-band) |
| `canvas` | Panes the model can draw (markdown, stats, tables, SVG, buttons that run allowlisted commands), and media curation with previews and verdicts. Needs its Python CLI; see the repo | [algonormative/canvas](https://github.com/algonormative/canvas) |

Each plugin repository is also a marketplace of its own (`/plugin install <name> --marketplace algonormative/<repo>`). Releases are published from each repo.

## License

MIT for this catalog; each plugin carries its own license.
