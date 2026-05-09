# ohayou-mobile

朝のブリーフィング（Cowork/モバイル特化版）。

寝起きスマホからCowork（claude.ai）を開いて `/ohayou` で起動すると、今日の予定・昨日の続き・今日の最優先を1枚にまとめたブリーフィングが返ってくる。

## 想定利用シーン

- 朝、布団でスマホ → Cowork開く → `/ohayou`
- 移動中・電車内で今日の準備確認

## 起動

```
/ohayou
```

## 取得ソース

| ソース | 取得内容 |
|---|---|
| Google Calendar (MCP) | 今日の予定 + 明日朝イチ |
| Notion mariko-notion (MCP) | 昨日の日報 + 作業インボックス |

## CLI版との関係

ローカルClaude Codeの `/ohayou` （`~/.claude/skills/ohayou/SKILL.md`）はフル機能版（統合まとめ救済・学習ログ蒸留・月初/月曜サジェスト等を含む）。

このCowork版は **速報のみ** に絞ったスリム版。ローカルファイル参照が必要な前段STEPは全削除している。詳細版が必要ならPCに移ってCLI版を打ち直す。

## ファイル構造

```
ohayou-mobile/
├── .claude-plugin/
│   └── plugin.json
├── commands/
│   └── ohayou.md
└── README.md
```

## バージョン履歴

- 0.1.0 (2026-05-09): 初回plugin化。速報フォーマットのみ
