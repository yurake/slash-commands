---
description: Use github-mcp-server tools to locate PR (ask number), fetch Codex comments, fix them, push with Conventional Commit, and notify @codex.
---
github-mcp-server mcpのget_review_commentsでレビューを取得して。
pr番号わからなかった聞き返して。
codexからコメントがあることを確認したら、修正対応して。
github-mcp-server mcpのpush_filesで、Conventional Commits 形式でpushまで実施して。
最後に、github-mcp-server mcpのadd_issue_commentで、そのprに「@codex 修正したので確認してください」とコメントして
