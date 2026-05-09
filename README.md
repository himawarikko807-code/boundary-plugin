# boundary-plugin

Auto modeセッション冒頭のBoundary宣言テンプレを展開するpluginミラー版。

正本: `~/.claude/commands/boundary.md`
このplugin: 配布検証用ミラー

## インストール（ローカル開発）

```bash
claude --plugin-dir ~/.claude/plugins-dev/boundary-plugin
```

起動後:

```
/boundary:boundary HP改修
```

namespace `boundary:` がついた状態で発火する。

## ファイル構造

```
boundary-plugin/
├── .claude-plugin/
│   └── plugin.json
├── commands/
│   └── boundary.md
└── README.md
```

## 注意

これはミラー版。**正本は `~/.claude/commands/boundary.md`**。
plugin側を直接編集しない。正本を更新したら、plugin側に手動コピー。

## 配布

- **Claude Code他環境への配布**: GitHubでpublic/private repoにpush → marketplace経由でinstall
- **Cowork側への配布**: 同上。Cowork固有のlocal upload経路は2026-05時点で未確認

## バージョン履歴

- 0.1.0 (2026-05-09): 初回plugin化PoC
