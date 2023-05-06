# ChatGPTを使ったAllen Mouse Brain Connectivity Atlasデータベース解析手法の提案

## 動作チェックサンプル

openai apiの接続テストと、supabase（データベースサービス）への接続とデータの読み出しテストを行います。

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/FujiiWebWorks/chatgpt-database-analysis-app/blob/main/sample.ipynb)

※自身のopenaiアカウントからapi keyを取得してください。
https://platform.openai.com/account/api-keys

※supabaseの情報は管理者にお尋ねください。


## [STEP1] Embeddingによるクエリに関連するデータベーステーブル・カラムの選定

クエリにデータベース構造情報を直接付与した場合と、
各データベースカラムをEmbeddingし、クエリとの類似性を評価した場合とで、回答結果を比較しました。

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/FujiiWebWorks/chatgpt-database-analysis-app/blob/main/STEP1_select_table_columns_with_embedding.ipynb)
