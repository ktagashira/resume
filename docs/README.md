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

<p>
<img src="https://img.shields.io/badge/Python-3776AB.svg?style=flat&logo=python&logoColor=white">
<img src="https://img.shields.io/badge/SQL-4479A1.svg?style=flat&logo=amazondynamodb&logoColor=white">
<img src="https://img.shields.io/badge/TypeScript-3178C6.svg?style=flat&logo=typescript&logoColor=white">
<img src="https://img.shields.io/badge/Shell%20Script-4EAA25.svg?style=flat&logo=gnu-bash&logoColor=white">
<img src="https://img.shields.io/badge/HCL-7B42BC.svg?style=flat&logo=terraform&logoColor=white">
<img src="https://img.shields.io/badge/LookML-4285F4.svg?style=flat&logo=looker&logoColor=white">
</p>

### データ基盤

<p>
<img src="https://img.shields.io/badge/Google%20Cloud-4285F4.svg?style=flat&logo=google-cloud&logoColor=white">
<img src="https://img.shields.io/badge/BigQuery-669DF6.svg?style=flat&logo=googlebigquery&logoColor=white">
<img src="https://img.shields.io/badge/dbt-FF694B.svg?style=flat&logo=dbt&logoColor=white">
<img src="https://img.shields.io/badge/Dataform-4285F4.svg?style=flat&logoColor=white">
<img src="https://img.shields.io/badge/Looker-4285F4.svg?style=flat&logo=looker&logoColor=white">
<img src="https://img.shields.io/badge/Terraform-7B42BC.svg?style=flat&logo=terraform&logoColor=white">
<img src="https://img.shields.io/badge/Kubernetes-326CE5.svg?style=flat&logo=kubernetes&logoColor=white">
<img src="https://img.shields.io/badge/Embulk-DE3727.svg?style=flat&logoColor=white">
<img src="https://img.shields.io/badge/Digdag-F2B40C.svg?style=flat&logoColor=white">
<img src="https://img.shields.io/badge/GitHub%20Actions-2088FF.svg?style=flat&logo=githubactions&logoColor=white">
<img src="https://img.shields.io/badge/Docker-2496ED.svg?style=flat&logo=docker&logoColor=white">
</p>

### 機械学習・AI

<p>
<img src="https://img.shields.io/badge/Azure-0078D4.svg?style=flat&logo=microsoftazure&logoColor=white">
<img src="https://img.shields.io/badge/PyTorch-EE4C2C.svg?style=flat&logo=pytorch&logoColor=white">
<img src="https://img.shields.io/badge/Agent%20Development%20Kit-4285F4.svg?style=flat&logo=google&logoColor=white">
<img src="https://img.shields.io/badge/Dify-1677FF.svg?style=flat&logoColor=white">
</p>

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

### 株式会社wevnal（2022/04〜2024/04）

LINE を活用したマーケティング SaaS「BOTCHAN」シリーズを提供する企業にて、機械学習エンジニア・データエンジニアとして、AI-FAQ プロダクトの ML 機能開発、データ基盤構築、テクニカルディレクションを担当。

#### 新規 AI-FAQ プロダクト「BOTCHAN AI」の AI 機能開発

- toC 企業向け AI-FAQ プロダクトの自然言語処理機能開発
  - ML を活用できるユースケースの検討・ML 機能開発ロードマップの策定
  - 技術選定・PoC 検証
  - データの前処理・特徴量エンジニアリング・学習・推論
  - 運用に向けた ML 推論の高速化・処理の軽量化
  - オフショア先と連携した運用
  - アナリティクス画面のデザイン設計・バックエンドの分析機能実装

- ChatGPT 搭載の接客オートメーションツールへの進化に伴う開発
  - Azure OpenAI Service / Azure AI Search / Azure API Management を活用した仕様策定・PoC 検証・開発

#### LINE コミュニケーション SaaS「BOTCHAN Relation」のデータ基盤構築

- データ基盤構築およびレポート提供
  - 分析データ基盤の設計・実装・保守運用
  - プロダクト利用データの解析基盤を設計し、レポートへ反映
  - 約 1 ヶ月でデータ基盤の設計から初期クライアントへのレポート提供までを完了
  - データ基盤の CI にバリデーションを導入し、迅速かつ安全なデプロイを実現
  - 計測指標を具体的な定義に落とし込み、プロダクト導入前後の効果をレポート化。データドリブンなプロダクト改善を促進

#### 「BOTCHAN AI」テクニカルディレクション

- Biz メンバーと連携し、BOTCHAN AI のクライアントに対するテクニカルディレクションを担当
  - クライアント側の独自データのマネジメント
  - 各クライアントの要望に合わせたプロンプトチューニング
  - クライアントからの追加開発要望に対する見積もり・要件整理

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
