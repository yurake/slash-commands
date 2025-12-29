---
description: Address GitHub issue #$1 using github-mcp-server.issue_read; branch from main if needed and no RM/ToDo creation required.
---
Github issue # $1 に対応して
前提:
  - 今回のタスクでは ToDo や RM を作成しなくてよい
  - `git remote get-url origin` を実行し、リポジトリ情報を取得・確認する
  - github-mcp-server.issue_read のmcpを使ってissueの情報を取得できる
  - 対応着手する前に、mainブランチの場合はブランチを作成する
  - 対応着手する前に、mainブランチ以外の場合は、そのブランチを継続利用するかをユーザーに確認する
  - 修正後にテストを実施し、mainとの差分カバレッジが80%を超えるように
