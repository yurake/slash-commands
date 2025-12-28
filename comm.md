---
description: Git commit and push workflow—review diffs, craft Conventional Commits, and reference relevant issues before pushing.
---
commit, push.

- git status -sb で差分と不要ファイルが無いか確認する
- git diff を精査し、問題がなければ Conventional Commits 形式でサブジェクトをまとめる（例: feat(ui): add preview button / fix(core): adjust layout）
- コミットで参照する Issue 番号を確認する（docs/todo/<対象ToDo>.md の 関連Issue 行を参照。番号が未記載の場合は Issue 参照なしで進めてよい）
  - 対象のtodoやrmが不明な場合はユーザーに確認する。ない場合もあるためユーザーの指示に従う
- git add で変更をステージングする
- git commit -m "<type(scope): subject [refs #<番号>]>" を実行する（Issue 番号が無い場合は refs を省略し、本文のみ記載）
- git status -sb でコミット漏れや不要ファイルがないか再確認する
- git push origin <ブランチ名> でリモートへプッシュする
