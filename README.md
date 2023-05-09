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


## [STEP2] ChatGPTによるSQL生成

STEP1で選定したカラムを出力するSQLをChatGPTを用いて自動生成しました。

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/FujiiWebWorks/chatgpt-database-analysis-app/blob/main/STEP2_generate_sql_with_openai_api.ipynb)



## [STEP3,4 - 解析1] 大まかな脳領域からの投射関係を出力

STEP1, 2で適切なデータセットが得られたと仮定して、3つの解析対象について、現在のデータベースから出力が得られるか検証を行いました。
STEP3で得た結果と、データ構造などのメタ情報から、OpenAI APIを用いて洞察を得ました。


[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/FujiiWebWorks/chatgpt-database-analysis-app/blob/main/STEP3_4_for_ANALYSIS_1.ipynb)


## [STEP3,4 - 解析2] 特定の脳部位に対し、投射関係を逆に辿った経路を出力

[解析1]と同様、[解析2]に対して、STEP3から4までの出力結果を表示します。

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/FujiiWebWorks/chatgpt-database-analysis-app/blob/main/STEP3_4_for_ANALYSIS_2.ipynb)


## 統計データ

### specimens（マウス標本）

Allen Brain Mouse Connectivity Atlasで行われたマウス投射実験（n=2409）において、標本マウスの性別, 年齢(日数), 体重(g),　系統データや、注入方式, 脳内の位置, 薬物情報についての情報を掲載します。

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/FujiiWebWorks/chatgpt-database-analysis-app/blob/main/stats_specimens.ipynb)
