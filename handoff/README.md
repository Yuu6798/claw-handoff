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
