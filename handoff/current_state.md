# current_state.md

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

## 次アクション
1. PR #5 の確認・マージ
2. Step 3: ΔE 3パターン計算（core/full/summary）
3. Step 4: レポートを温度別・role別に再構成
4. Step 5: v1再採点・v1レポート生成

## 絶対ルール
- `ugh-audit-core` のみ変更する
- `ugh3-metrics-lib` は参照のみ、勝手に変更しない
- `phase_c_raw.jsonl` は絶対に上書きしない
- OpenAI API呼び出しはユーザー明示承認時のみ
- 大きい変更はPR単位で進める

## 役割分担の想定
- Discord側 Claw: 実装・コード生成・PR更新
- webchat側 Claw: 統括・レビュー・方針整理・引き継ぎ管理

## 最終更新
- 2026-03-20 JST
