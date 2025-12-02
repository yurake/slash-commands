sonarqubeの指摘を取得し、最優先の1件をgithub issueに起票してください。

前提:
この作業においてrmやtodoの紐付けは不要です。

手順:
1. 静的解析結果取得: bash scripts/run_export_sonar_issues.sh を実行し正常終了することを確認したら、temp/sonar_issues_by_file.jsonファイルの結果を確認してください。
2. オプション利用: --branch / --severities / --types / --statuses オプションを使うことで、特定のブランチや重大度、タイプ、ステータスの指摘に絞り込んで取得できます。必要に応じてこれらのオプションを利用してください。
3. 実行結果共有: jq 等で結果をし、最優先で修正すべき1件を特定してください。
4. 全体結果と、最優先で修正すべき指摘1件の詳細を共有し、対応の承認を得てください。
  - 取得した指摘の総件数と、ブランチ／オプションなど実行条件の概要
  - 重大度ごとの件数（BLOCKER / CRITICAL / MAJOR など）と、主なタイプ（BUG / CODE_SMELL など）の内訳
  - 指摘が多い上位ファイルやモジュール（件数ベースで 3〜5 件程度）
5. 指摘対応: 承認を得られたら、github issueを作成してください。
  - テンプレート .github/ISSUE_TEMPLATE/bug_report.yml に合わせてください。
  - SonarCloud issue key など、悪用される情報は記載しないでください。
  - 個人が特定されうるファイルの絶対パスなども記載しないでください。
