# 職務経歴書

## 基本情報

|key|value|
|---|---|
|氏名|田頭 啓介 (Keisuke Tagashira)|
|生年月日|1997/05/01|
|X|[@tagasyksk](https://x.com/tagasyksk)|
|Qiita|[@tagasyksk](https://qiita.com/tagasyksk)|
|Zenn|[@chabasssy](https://zenn.dev/chabasssy)|
|SpeakerDeck|[ktagashira](https://speakerdeck.com/ktagashira)|

---

## 保有スキル

- データ基盤の設計・構築・運用（BigQuery / dbt / Dataform / Looker）
- 現場部門と密に連携したアジャイルなデータモデリング
- Google Cloud を活用したデータパイプラインの構築・管理
- Terraform によるデータ基盤インフラの IaC 化
- Looker を用いた BI ダッシュボードの構築
- データ基盤と連携した AI エージェントの設計・開発

---

## 技術スタック

### 言語

- Python
- SQL
- TypeScript
- Shell Script
- HCL (Terraform)
- LookML

### フレームワーク・その他

- Google Cloud
- dbt / Dataform
- Looker / Looker Studio
- Terraform
- GitHub Actions
- Agent Development Kit (ADK)
- Dify
- Docker

---

## 職務経歴詳細

### ファインディ株式会社（2024/05〜現在）

データソリューションチーム所属。データエンジニアとして、全社横断のデータ基盤の構築・運用、管理会計データモデリング、BI ダッシュボード開発、AI エージェント開発を担当。

#### データ基盤の構築・運用

- 全社共通データ基盤の設計・開発
  - BigQuery + dbt を用いたデータ基盤の構築。複数事業部のデータを統合し、全社横断で分析可能な環境を整備
  - HubSpot・SendGrid・KARTE 等の外部サービスとのデータ連携パイプラインの構築
  - Analytics Hub を利用した本番/ステージング間のデータ共有の仕組みを設計し、安全な開発環境を実現

- データプラットフォームの整備
  - Terraform による Google Cloud リソース（BigQuery データセット、サービスアカウント、IAM）および GitHub リポジトリ・チーム権限の IaC 化
  - Cloud DLP を活用した個人情報マスキングの仕組み構築
  - Datastream / Fluent Bit によるリアルタイムデータ連携基盤の構築

#### 管理会計データモデリング

- 経営企画向け管理会計基盤の構築
  - 経営企画部門と密に連携し、要件のヒアリングからデータモデル設計・ダッシュボード構築までをアジャイルに推進。短いサイクルでフィードバックを得ながら、事業部ごとに異なる会計要件を段階的にモデルへ反映
  - 事業部別の損益計算書（P/L）を随時算出するシステムを構築し、連結・事業部別・共通部門の詳細内訳を可視化
  - LookML を用いた管理会計ダッシュボードを構築し、経営企画部門がセルフサービスで売上分析を行える環境を整備

#### AI エージェント開発

- 事業部横断の CRM 検索エージェント
  - Google ADK を活用し、Slack から複数 CRM の顧客情報を横断検索できるエージェントを開発

- IS 架電支援エージェント
  - 架電に必要な企業情報をデータ基盤から収集・要約する AI エージェントを開発し、インサイドセールスの業務効率化に貢献

- 社内 AI プラットフォームの構築・運用
    - Dify を GKE 上に構築し、社内向け AI プラットフォームとして運用

#### その他

- Looker SDK を利用した LookML バリデーション CI の構築
- 分析プロジェクトの標準化（分析ナレッジ・クエリの蓄積基盤の整備）

### 副業・業務委託

#### SNIFFOUT Inc.

- [RAG Ready Converter](https://rag-ready-converter.sniffout.net) の開発に参画。Excel・PowerPoint・画像等の多様なファイル形式を RAG に適した形式へ変換する SaaS プロダクト
  - ドキュメント変換ロジックの開発
  - AWS インフラの構築・整備

---

## 資格

- Google Cloud Professional Data Engineer（2025 年 5 月取得）

---

## 業務外活動

### テックブログ・記事執筆

- [MCPとAIエージェントを活用してSlackから複数CRMの顧客情報を横断検索できる仕組みを作った話](https://tech.findy.co.jp/entry/2025/07/08/070000)（Findy Tech Blog）
- [Dataformの活用とその効果](https://tech.findy.co.jp/entry/2024/07/01/083000)（Findy Tech Blog）
- [Looker SDKを使ってLookMLのバリデーションCIを自作した話](https://zenn.dev/chabasssy/articles/d3aebc9d30d6b8)（Zenn, 2025/12）
- [Google Cloud Professional Data Engineer合格記(2025.5)](https://zenn.dev/chabasssy/articles/e2e90956e4824c)（Zenn, 2025/05）
- [dbt / Dataformで管理外のテーブルを削除して、気持ち良く正月を迎えたい](https://zenn.dev/chabasssy/articles/27e37e51eb0125)（Zenn, 2024/12）

### 登壇

- [ADKを活用して事業部横断の企業検索エージェントを作成した話](https://speakerdeck.com/ktagashira)（SpeakerDeck, 1.3k views）
- [Findyのユーザーサクセス面談を支えるデータ技術](https://speakerdeck.com/ktagashira)（SpeakerDeck, 780 views）

### OSS

- [adk-slack-adapter](https://github.com/ktagashira/adk-slack-adapter) - Google Agent Development Kit で作成したエージェントと Slack を連携するためのツール
