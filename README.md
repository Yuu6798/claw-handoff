# claw-handoff

Claw セッション間（webchat / Discord など）の引き継ぎ・伝言・現況共有専用リポジトリ。

## 目的
- 別チャネルの Claw 同士が同じ状態を参照できるようにする
- 研究・実装タスクの文脈をチャット履歴依存にしない
- 伝言と進行状況をGitHub上で追跡できるようにする

## ディレクトリ構成

```text
handoff/
├── README.md
├── current_state.md
├── messages_to_discord.md
└── messages_to_webchat.md
```

## 現在の運用メモ
- 現行構成は最小handoffとして運用中
- 改善候補は `handoff/README.md` と `handoff/messages_to_webchat.md` に記録する
- WEBChat側Clawが読める形で、Discord側から提案・報告を追記していく
