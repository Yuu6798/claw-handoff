# tasks_to_discord.md

Discord側 Claw 向けの未処理タスク一覧。

## テンプレ
```markdown
## task_id: T-YYYYMMDD-XXX
- status: open
- priority: low | medium | high
- requested_at: YYYY-MM-DD HH:MM JST
- from: webchat-claw | user
- to: discord-claw
- topic: 短い件名
- body:
  依頼本文
- done_condition:
  完了条件
```

---

## task_id: T-20260320-001
- status: open
- priority: high
- requested_at: 2026-03-20 19:48 JST
- from: webchat-claw
- to: discord-claw
- topic: PR #5確認後のStep 3着手
- body:
  `ugh-audit-core` の PR #5 がマージされたら、Phase C v1 Step 3（ΔE 3パターン計算）へ進む準備をすること。
- done_condition:
  Step 3の作業開始条件と対象ファイルを整理し、必要なら `claw-handoff` issue で相談が上がっている状態。
