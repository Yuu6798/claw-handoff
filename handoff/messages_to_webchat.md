# messages_to_webchat.md

## 使い方
- Discord側 Claw / ユーザーから webchat側 Claw への伝言をここに追記する
- 処理後は `- [done]` を付ける

---

- [done] （初期化）Discord側からの報告待ち
- [open] 2026-03-20 JST: Discord側Clawが `handoff/current_state.md` を確認。`ugh-audit-core` の現状を把握済み。ローカル読取の結果、リポジトリは実装済みの研究用監査基盤として成立しており、`pytest -q` は 23 passed / 3 skipped。主要認識は以下：
  - Phase C v0〜v1 の導線（collect / score / export）は実装済み
  - 現状は「完成監査基盤」より「校正中の監査実験装置」に近い
  - 強みは、3層fallbackの `UGHScorer`、SQLite保存、GoldenStore、Phase Cスクリプト群、grv日本語対策、通過済みテスト
  - 弱みは、ΔEのreference依存、grv辞書の近似性、backend記録の厳密性不足、レポート粒度不足
  - 次の自然な作業順は、PR #5確認/マージ → Step 3（ΔE 3パターン計算）→ Step 4（温度別・role別レポート）→ Step 5（v1再採点・v1レポート）
  - 絶対ルールは把握済み：`ugh-audit-core` のみ変更、`ugh3-metrics-lib` は参照のみ、`phase_c_raw.jsonl` 上書き禁止、OpenAI API実行は明示承認時のみ
- [open] Discord側Clawは handoff 運用手順も把握。今後は `current_state.md` を起点に現状確認し、webchat向け報告を `messages_to_webchat.md` に追記する。
