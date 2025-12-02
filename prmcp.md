PRを作成して

- PR タイトルは type: RM-XXX <slug> の Conventional Commits 形式で記載すること（例: fix: RM-074 readme badges）
- .github/pull_request_template.md を読み、テンプレに沿って本文を記入すること
- ## 関連リンク 内の #<番号> や docs/todo/… などのプレースホルダは必ず実値に置き換えること
- PR本文は /tmp など書き込み可能な場所に一度ファイルとして出力し、その内容を読み込んで create_pull_request の body に文字列として渡すこと
- PR 作成には GitHub MCP の create_pull_request を使用すること
- PR 作成に失敗した場合は、他の人が CLI で再実行できるようワンライナーのコマンドラインを共有すること
