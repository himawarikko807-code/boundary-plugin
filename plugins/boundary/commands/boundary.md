---
description: Auto modeセッション冒頭のBoundary宣言テンプレを展開（引数に作業内容）
---

Auto modeのclassifierに渡すBoundary宣言。引数部分（$ARGUMENTS）に今日の作業内容が入る。以下をそのまま会話に貼り付けてください。

---

今日は$ARGUMENTSをやります。以下は毎回確認してください:
- Notion本番更新
- Gmail送信
- git push（main直push・force push・新規ブランチ作成）
- @client_reviewerを通さないクライアント文書の提出
- 本番デプロイ・DB書き込み
- MCP経由の外部送信（Slack通知・scheduled tasks作成等）

ローカルファイル編集・CSS/MDX調整・knowledge/配下の整理・skills/配下の編集は自動で進めてOK。

---

引数なし（`/boundary`）で起動した場合は、「$ARGUMENTS」を「[作業内容]」に読み替えて、まりこさんが手動で埋める前提で展開する。

対象作業の例: HP改修 / 柊Instagram / note記事 / harness-app-builder / クライアント文書作成 / knowledge整理
