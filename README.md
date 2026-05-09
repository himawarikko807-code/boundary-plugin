# mariko-plugins marketplace

Mariko Mochimaru's personal Claude Code / Cowork plugin marketplace.

## Available plugins

| Plugin | Description |
|---|---|
| `boundary` | Auto modeセッション冒頭のBoundary宣言テンプレ展開 |

## How to install

### Claude Code (CLI)

```
/plugin marketplace add himawarikko807-code/boundary-plugin
/plugin install boundary@mariko-plugins
```

After install:

```
/boundary:boundary HP改修
```

### Claude Cowork (claude.ai)

Use `/plugin` UI from within Cowork:
1. Add marketplace `himawarikko807-code/boundary-plugin`
2. Install `boundary` plugin
3. Trigger with `/boundary:boundary <作業内容>`

## Repo structure

```
boundary-plugin/
├── .claude-plugin/
│   └── marketplace.json   ← marketplace catalog
└── plugins/
    └── boundary/
        ├── .claude-plugin/
        │   └── plugin.json
        ├── commands/
        │   └── boundary.md
        └── README.md
```

## Maintenance

- 正本: `~/.claude/commands/boundary.md`（Mariko's local Claude Code）
- このrepo: 配布用ミラー。正本更新時は手動で `plugins/boundary/commands/boundary.md` にもコピー
