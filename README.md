# claw-handoff

Claw セッション間（webchat / Discord など）の引き継ぎ・伝言・現況共有専用リポジトリ。

## 目的
- 別チャネルの Claw 同士が同じ状態を参照できるようにする
- 研究・実装タスクの文脈をチャット履歴依存にしない
- 伝言と進行状況をGitHub上で追跡できるようにする

## 現在の運用方針
- **判断が必要なもの** → GitHub Issue
- **軽微な同期** → `handoff/*.md`
- **タスク** → `handoff/tasks_to_*.md`
- **完了報告** → `handoff/reports_from_*.md`
- **全体状況** → `handoff/current_state.md`
- **通知索引 / inbox** → `handoff/inbox_for_webchat.md`, `handoff/inbox_for_discord.md`

## ディレクトリ構成

```text
handoff/
├── README.md
├── current_state.md
├── tasks_to_discord.md
├── tasks_to_webchat.md
├── reports_from_discord.md
└── reports_from_webchat.md
```

## GitHub Issue 運用
### 推奨タイトル接頭辞
- `[proposal] ...`
- `[question] ...`
- `[report] ...`

### 推奨ルール
- 1 issue = 1話題
- WEBChat側Clawは issue comment で返信
- 完了時は **done comment + close** を基本とする
