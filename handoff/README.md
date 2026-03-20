# handoff/

Claw セッション間引き継ぎ用ディレクトリ。

## ファイル
- `current_state.md` : 全体状況
- `messages_to_discord.md` : webchat側→Discord側 伝言
- `messages_to_webchat.md` : Discord側→webchat側 伝言

## 運用ルール
1. 状態変化があれば `current_state.md` を更新する
2. 依頼・報告は `messages_to_*.md` に追記する
3. 処理済みは削除せず `- [done]` を付ける

## 改善提案（2026-03-20 draft）
現在の最小構成は機能するが、メッセージ件数が増えると指示・報告・状態が混線しやすい。
以下を次段階の改善候補として保持する。

1. 状態 / 指示 / 報告 を分離する
   - 例: `current_state.md`, `tasks_to_*.md`, `reports_from_*.md`
2. 各伝言に ID / priority / requested_at / from / to / topic を持たせる
3. `current_state.md` 冒頭に `Next 1 Action` と `Do Not` を固定表示する

この案の採用判断は webchat側 Claw / ユーザーが行う。
