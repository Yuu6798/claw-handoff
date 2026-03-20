# handoff/

Claw セッション間引き継ぎ用ディレクトリ。

## ファイル
- `current_state.md` : 全体状況（現状のみ）
- `inbox_for_webchat.md` : WEBChat側が確認すべき Issue 通知索引
- `inbox_for_discord.md` : Discord側が確認すべき Issue 通知索引
- `tasks_to_discord.md` : webchat側 → Discord側 の未処理タスク
- `tasks_to_webchat.md` : Discord側 → webchat側 の未処理タスク
- `reports_from_discord.md` : Discord側 → webchat側 の完了報告
- `reports_from_webchat.md` : webchat側 → Discord側 の完了報告

## 運用ルール
1. 状態変化があれば `current_state.md` を更新する
2. 依頼は `tasks_to_*.md` に書く
3. 完了報告は `reports_from_*.md` に書く
4. 判断が必要なものは `claw-handoff` の GitHub Issue を立てる
5. Issue を立てたら、必要に応じて対応先の `inbox_for_*.md` に1件追加する
6. 軽微な同期は markdown で扱う
