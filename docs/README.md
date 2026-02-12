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

### クラウド・インフラ

- Google Cloud
- Azure
- Terraform (HCL)
- Kubernetes
- Docker
- GitHub Actions

### DWH・データモデリング

- BigQuery
- dbt (Cloud / Core)
- Dataform

### BI

- Looker
- Looker Studio
- LookML

### ETL・ワークフロー

- Embulk
- Digdag

### 機械学習・AI

- PyTorch
- Agent Development Kit (ADK)
- Dify

---

## 職務経歴詳細

### ファインディ株式会社（2024/05〜現在）

データソリューションチーム所属。データエンジニアとして、全社横断のデータ基盤の構築・運用、管理会計データモデリング、BI ダッシュボード開発、AI エージェント開発を担当。

#### データ基盤の構築・運用

- Findy Freelance のデータ基盤の設計・開発・運用
  - BigQuery + dbt を用いたプロダクトデータ基盤を構築。社内プロダクト DB 5 種・外部 SaaS 12 種を含む約 20 のデータソースを統合し、約 1.3 TB・7,000 テーブル超の分析環境を構築・運用
  - dbt Core から dbt Cloud へ移行。GUI ベースの開発環境と CI/CD・ジョブ管理の一元化により、データアナリストがデータエンジニアの介在なしにモデル開発・デプロイできる体制を構築し、開発サイクルを短縮
  - Analytics Hub を利用した本番/ステージング間のデータ共有の仕組みを設計し、安全な開発環境を確保

- データプラットフォームの整備
  - Terraform による Google Cloud リソース（BigQuery データセット、サービスアカウント、IAM）および GitHub リポジトリ・チーム権限の IaC 化。本番/ステージング環境の再現性を確保し、権限管理を一元化・可視化
  - Cloud DLP を活用した個人情報マスキングの仕組みを構築し、個人情報を含むデータを分析者へ安全に提供できる環境を整備

#### 管理会計データモデリング

- 経営企画向け管理会計基盤の構築
  - それまでスプレッドシートで手作業集計していた 4 事業部以上の管理会計データを、BigQuery + dbt で自動化。経営企画部門と密に連携し、要件ヒアリングからデータモデル設計・ダッシュボード構築までをアジャイルに推進
  - 事業部別の損益計算書（P/L）を連結・事業部別・共通部門の内訳で可視化し、ボタン一つで最新数値を更新できる仕組みを構築。月次で 2〜3 営業日かかっていた集計作業を不要にし、属人化リスクも解消
  - LookML を用いた管理会計ダッシュボードにより、経営企画部門がセルフサービスで売上分析を行える環境を整備

#### AI エージェント開発

- 事業部横断の CRM 検索エージェント
  - 複数プロダクト展開に伴い顧客情報がサイロ化していた課題に対し、BigQuery 上の共通企業マスタを SQL スキルのない営業・CS メンバーでも活用できるよう、Slack ベースの企業検索エージェントを開発
  - 運用開始 1 ヶ月でインサイドセールス・カスタマーサクセスメンバーの約 40% が利用

- 社内 AI プラットフォームの構築・運用
  - Dify を GKE 上に構築し、社内向け AI プラットフォームとして運用

#### その他

- Looker SDK を利用した LookML バリデーション CI の構築
- 分析プロジェクトの標準化（分析ナレッジ・クエリの蓄積基盤の整備）

### 株式会社wevnal（2022/04〜2024/04）

チャットボット SaaS「BOTCHAN」シリーズを提供する企業にて、機械学習エンジニア・データエンジニアとして、AI 機能開発、データ基盤構築、テクニカルディレクションを担当。

#### 新規 AI-FAQ プロダクト「BOTCHAN AI」の AI 機能開発

- toC 企業向け AI-FAQ プロダクトの自然言語処理機能を開発
  - FAQ 検索・マッチングおよび意図分類モデルの開発。ユースケースの検討・ロードマップ策定から、データの前処理・特徴量エンジニアリング・学習・推論まで一貫して担当
  - モデルの蒸留・量子化による推論高速化・軽量化を行い、プロダクション運用に耐えるパフォーマンスを実現
  - オフショア先と連携した運用体制の構築、アナリティクス画面のデザイン設計・バックエンド実装

- ChatGPT 搭載の接客オートメーションツールへの進化
  - Azure OpenAI Service / Azure AI Search / Azure API Management を用いた技術構成の仕様策定・PoC 検証を担当し、プロダクトの LLM 移行方針を確立

#### LINE コミュニケーション SaaS「BOTCHAN Relation」のデータ基盤構築

- クライアント向けレポート提供のためのデータ基盤をゼロから構築
  - 約 1 ヶ月でデータ基盤の設計から初期クライアントへのレポート提供までを完了
  - 計測指標を具体的な定義に落とし込み、プロダクト導入前後の効果をレポート化。クライアントへのデータドリブンな価値提供を実現
  - データ基盤の CI にバリデーションを導入し、迅速かつ安全なデプロイを実現

#### 「BOTCHAN AI」テクニカルディレクション

- Biz メンバーと連携し、クライアントに対するテクニカルディレクションを担当
  - クライアント独自データのマネジメント、要望に合わせたプロンプトチューニング、追加開発要望の見積もり・要件整理を一手に担当

### 副業・業務委託

#### SNIFFOUT Inc.

- [RAG Ready Converter](https://rag-ready-converter.sniffout.net) の開発に参画。Excel・PowerPoint・画像等の多様なファイル形式を RAG に適した形式へ変換する SaaS プロダクト
  - ドキュメント変換ロジックの開発
  - AWS インフラの構築・整備

---

## 学歴

- 東京理科大学 応用生物科学科（2022 年 3 月卒業）

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
