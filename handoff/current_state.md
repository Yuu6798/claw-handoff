# current_state.md

## Next 1 Action
- `ugh-audit-core` の PR #5 を確認・マージし、その後 Phase C v1 Step 3（ΔE 3パターン計算）へ進む。

## Do Not
- `phase_c_raw.jsonl` を上書きしない
- `ugh3-metrics-lib` を変更しない
- OpenAI API をユーザー明示承認なしで実行しない
- `claw-handoff` を実装リポジトリ代わりに使わない

## 現在の対象プロジェクト
- リポジトリ: `Yuu6798/ugh-audit-core`
- ローカル: `/home/work/.openclaw/workspace/ugh-audit-core`

## プロジェクト目的
UGHer（無意識的重力仮説）の監査基盤を実装・検証する。
主要指標は PoR / ΔE / grv。
現在は Phase C の実データ収集後の v1 校正フェーズ。

## 現在の状況
- Phase C v0 の生回答データ（306件）は取得済み
- v0 採点結果・HTMLレポート・calibration_notes は作成済み
- `data/phase_c_v0/` として GitHub に保存済み
- Phase C v1 は step-by-step PR 方式で進行中

## 直近の進捗
- Step 1: por_fired 境界条件確認 → 完了・マージ済み
- Step 2: grv日本語トークナイズ修正 → PR #5 で進行
- Step 2 には追加レビュー修正（stopwords / katakana / comments）が反映済み

## 現在の重要PR / ブランチ
- main
- `claude/phase-c-v1`
- PR #5: `Phase C v1 — Step 2: grv日本語トークナイズ修正`
  - URL: `https://github.com/Yuu6798/ugh-audit-core/pull/5`
  - `fix-stopwords-katakana-GLI2g` の修正も取り込み済み

## handoff inbox ルール
- GitHub Issue = 対話本体
- `handoff/inbox_for_webchat.md` / `handoff/inbox_for_discord.md` = 通知索引
- inbox は要約本文ではなく、Issueへの導線に徹する

## WEBChat-side Claw 監視ルール（最小）
- `claw-handoff` open issue を定期確認する
- 対象条件: `to:webchat` + 種別ラベル（`proposal` / `question` / `report`）
- 未処理判定: WEBChat-side Claw の初回応答コメントがまだ無いこと
- 重要事項のみ `reports_from_webchat.md` / `current_state.md` へ戻す

## handoff運用ルール（最新版）
- 判断が必要なものは `claw-handoff` の GitHub Issue に寄せる
- 軽微な同期は `handoff/*.md` で扱う
- タスクは `tasks_to_*.md`
- 完了報告は `reports_from_*.md`
- 重要判断は Issue comment に残し、完了時は `done comment + close`

## 役割分担の想定
- Discord側 Claw: 実装・コード生成・PR更新
- webchat側 Claw: 統括・レビュー・方針整理・引き継ぎ管理

## 最終更新
- 2026-03-20 JST
