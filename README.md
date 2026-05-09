# mariko-plugins marketplace

Mariko Mochimaru's personal Claude Code / Cowork plugin marketplace.

## Available plugins

| Plugin | Description |
|---|---|
| `boundary` | Auto modeセッション冒頭のBoundary宣言テンプレ展開 |
| `ohayou-mobile` | 朝のブリーフィング（Cowork/モバイル特化版） |

## How to install

### Claude Code (CLI)

```
/plugin marketplace add himawarikko807-code/boundary-plugin
/plugin install boundary@mariko-plugins
/plugin install ohayou-mobile@mariko-plugins
```

After install:

```
/boundary:boundary HP改修
/ohayou-mobile:ohayou
```

### Claude Cowork (claude.ai)

Cowork UI から install:
1. 個人用プラグインの「+」→「プラグインを作成」→「マーケットプレイスを追加」
2. URL欄に `himawarikko807-code/boundary-plugin` を入力 → 同期
3. `個人用` タブから各 plugin を install

トリガー（Cowork chat内）:
- `/boundary HP改修`
- `/ohayou`

## Repo structure

```
boundary-plugin/
├── .claude-plugin/
│   └── marketplace.json   ← marketplace catalog
└── plugins/
    ├── boundary/
    │   ├── .claude-plugin/plugin.json
    │   └── commands/boundary.md
    └── ohayou-mobile/
        ├── .claude-plugin/plugin.json
        └── commands/ohayou.md
```

## Maintenance

- 正本: `~/.claude/commands/boundary.md` / `~/.claude/skills/ohayou/SKILL.md`（Mariko's local Claude Code）
- このrepo: 配布用ミラー。正本更新時は手動で `plugins/{name}/commands/{cmd}.md` にもコピー
- `ohayou-mobile` は CLI版 `/ohayou` のスリム版（ローカル依存を全削除）。フル機能版はローカル `/ohayou` を使う
