merge from main.

- git fetch origin 後、**まずは rebase を試す**：追従すべきブランチ（例: origin/main）に対して `git rebase origin/main` を行い、コンフリクトが出たら解消して `git rebase --continue`
- 共同開発で同じトピックブランチに他者コミットが入っている場合のみ `git rebase origin/<current_branch>` を選ぶ
- **もしリベースが難航/中断する場合は `git rebase --abort` で元に戻し、「merge で取り込み」に切り替える**：`git merge --ff-only origin/<current_branch>`（共同ブランチの場合のみ早送り追従）→ `GIT_EDITOR=true git merge --no-edit origin/main`（必要なら `--no-ff`）
- 取り込み完了後は、初回 push なら `git push -u origin <current_branch>` を使い追跡ブランチを設定する。以降は `git push` で済ませられる。**rebase 経路で履歴を書き換えた場合のみ** `git push --force-with-lease origin <current_branch>` を使って安全に更新する（**merge 経路では原則不要**）
