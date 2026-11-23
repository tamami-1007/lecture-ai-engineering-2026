# 第6回 解答

## 演習

<!-- [tool call] の行は、表示された行をそのまま貼り付けてください。終わらなかった STEP は、空欄のままでかまいません。 -->

- STEP 1 のツールの名前：
- STEP 2 の [tool call]：
- STEP 3 の [tool call]：
- STEP 4 の [tool call]：
- 気づき・疑問：

## 宿題

<!-- 基礎・実装・発展のどれか1つに取り組めば完了です。 -->

- 取り組んだレベル：基礎
- やったこと：app/mcp_server.py の TODO の下に server.tool()(tools.get_lecture_summary) を追加し、get_lecture_summary を MCP ツールとして公開した。app/mcp_servers.json と app/mcp_agent.py は変更していない。
- 結果：git status で変更ファイルが app/mcp_server.py だけであることを確認した。uv run python -m app.mcp_agent --list-tools で glossary_get_lecture_summary が表示された。「第2回では何を学びますか？」と質問したところ、trace に glossary_get_lecture_summary({'lecture': 2}) と表示され、第2回の要約が返った。uv run pytest -q では 21 passed in 4.48s となった。
- 気づき・疑問：エージェント側のコードを変更しなくても、MCP サーバーが公開するツールを追加すると、エージェント起動時に新しいツールが一覧に追加され、質問から呼び出せることが分かった。疑問は特になし。
