---
description: Safely delete unnecessary local git branches while skipping checked-out or worktree branches and confirming remote deletion needs.
---
不要なブランチを削除して

- git branchでブランチ一覧を取得
- 先頭に*がつく現在チェックアウトしているブランチや、先頭に+がつくworktreeで別作業中のブランチは削除対象外
- ローカルブランチのみ削除し、同じリモートブランチが存在する場合は、削除が必要かユーザーに確認して
