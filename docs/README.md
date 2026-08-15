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

## サマリ

- データ領域での実務 4 年（2022/04〜）。BigQuery + dbt を中心としたデータ基盤の構築・運用が専門
- 個人情報の統制設計から権限管理のコード化まで、データガバナンスの整備を主導
- 約 20 データソース / 約 1.3 TB / 7,000 テーブル超の基盤を構築し、事業部メンバーが自走できる状態まで移譲

---

## 保有スキル

### データガバナンス・データマネジメント

- ポリシータグ（列レベルのアクセス制御）と Dataplex による個人情報の管理
- Terraform による IAM・権限のコード管理と半期ごとの権限レビュー
- DMBOK に基づくデータマネジメント成熟度アセスメントの運用

### ディメンショナルモデリング

- ビジネスプロセス単位でファクトの粒度を定義するスタースキーマ設計
- staging / dimension・fact / mart のレイヤー構成による dbt モデルの設計・運用

### データ基盤の設計・構築・運用

- BigQuery + dbt を中心としたデータ基盤の構築・運用
- freshness 監視やテストカバレッジ検査などデータ品質の CI/CD
- TROCCO を用いた CRM・マーケティングツールへのリバース ETL
- データ基盤と連携した AI エージェントの開発（ADK / MCP）

---

## 職務経歴詳細

### ファインディ株式会社（2024/05〜現在）

データソリューションチーム所属。データエンジニアとして、全社横断のデータ基盤の構築・運用、管理会計データモデリング、BI ダッシュボード開発、AI エージェント開発を担当。モデリング規約やデータガバナンス体制の策定、事業部への運用委任までを主導。

#### データ基盤の構築・運用

- Findy Freelance のデータ基盤の設計・開発・運用
  - BigQuery + dbt を用いたプロダクトデータ基盤を構築。社内プロダクト DB 5 種・外部 SaaS 12 種を含む約 20 のデータソースを統合し、約 1.3 TB・7,000 テーブル超の分析環境を運用
  - staging / dimension・fact / mart のレイヤー構成と層ごとの責務をモデリング規約として定義。累計 370 件超の PR で dbt モデルを開発
  - ビジネスプロセスごとにファクトの粒度を定義し、企業・ユーザーなどの適合ディメンションと組み合わせたスタースキーマで設計
  - 広告媒体・行動ログを含む複数データソースを統合し、TROCCO で CRM・マーケティングツールへ連携するデータマートを構築（リバース ETL）
  - dbt 実行環境を dbt Platform へ移行。データアナリストがデータエンジニアを介さずにモデルを開発・デプロイできる体制を構築

- データガバナンスの設計・運用
  - 複数の Google Cloud プロジェクトに分散していた基盤を単一プロジェクトへ統合し、東京リージョンに移行
  - 個人情報はポリシータグ（列レベルのアクセス制御）と Dataplex で lake 層に閉じ込め、スプレッドシート経由でアクセス制御を迂回できるリスクを解消
  - Cloud DLP によるマスキングで、個人情報を含むデータも分析者へ安全に提供
  - BigQuery データセット・サービスアカウント・IAM と GitHub リポジトリの権限を Terraform でコード管理（本番/ステージング環境の再現性を確保）
  - 半期ごとの権限レビューをチームの運用サイクルとして定着
  - DMBOK に基づくデータマネジメント成熟度アセスメントを半期ごとに主導し、データガバナンス領域のスコアを 0.5 → 3.2 へ改善

- データ品質と運用
  - freshness 監視・テストカバレッジ検査を CI/CD に組み込み、データ品質の劣化を検知
  - アラート対応の体制を整えて安定運用。社内の利用者アンケートではデータストレージ・運用領域が 4.4/5.0
  - Looker を導入し、事業部メンバーがセルフサービスで分析できる BI 環境を構築
  - 日常運用を事業部メンバーへ委任し、データチームを介さないデータ活用のサイクルを確立

#### 管理会計データモデリング

- 経営企画向け管理会計基盤の設計・構築（2025）
  - 会計実績値の算出ロジックがスプレッドシートとネストされた BigQuery ビューに散在し、翌年度の実績値を再現できない状態が課題。4 事業部以上の管理会計データを BigQuery + dbt のモデルへ集約
  - 総勘定元帳を起点に売上・費用・原価をトランザクションファクトへ分解し、見通し系は周期スナップショットファクトとして実績と同一の粒度・構造で設計
  - 変動しうる共通費の配賦率を変換ロジックから分離し、マスタデータとして管理してハードコードを排除。経営企画メンバー自身が更新できるよう、マスタ更新は Slack 起点のワークフローと AI エージェント（Claude Code Actions）で自動化
  - 経営企画メンバーをレビュアーとする Design Doc ベースの設計レビューを導入
  - LookML で P/L 指標・人件費・人員をメジャー化し、連結・事業部別・共通部門の内訳でドリルダウンできるダッシュボードを構築
  - Looker の会話分析エージェントを整備し、自然言語での予実分析にも対応
  - 翌年度の会計実績値をデータ基盤上で算出できるようになり、実績値算出のリードタイムは 3 人日から 10 分へ短縮。月次 2〜3 営業日の集計作業も不要化

#### AI エージェント開発

- 事業部横断の CRM 検索エージェント
  - 複数プロダクトの展開で顧客情報がサイロ化していた課題に対し、ADK と MCP を用いた Slack ベースの企業検索エージェントを開発
  - SQL スキルのない営業・CS メンバーでも共通企業マスタを検索できるよう、エージェントへ提供するデータの範囲と権限を設計
  - 運用開始 1 ヶ月でインサイドセールス・カスタマーサクセスメンバーの約 40％ が利用

- 社内 AI プラットフォームの構築・運用
  - Dify を GKE 上に構築し、社内向け AI プラットフォームとして運用

### 株式会社wevnal（2022/04〜2024/04）

チャットボット SaaS「BOTCHAN」シリーズを提供する企業にて、機械学習エンジニア・データエンジニアとして、AI 機能開発、データ基盤構築、テクニカルディレクションを担当。

#### 新規 AI-FAQ プロダクト「BOTCHAN AI」の AI 機能開発

- toC 企業向け AI-FAQ プロダクトの自然言語処理（NLP）機能を開発
  - FAQ 検索・マッチングおよび意図分類モデルの開発。ユースケースの検討・ロードマップ策定から、前処理・特徴量エンジニアリング・学習・推論まで一貫して担当
  - モデルの蒸留・量子化による推論の高速化・軽量化で、プロダクション運用に耐えるパフォーマンスを確保
  - オフショア先を含む運用体制の設計と、アナリティクス画面のデザイン設計・バックエンド実装を担当

- ChatGPT 搭載の接客オートメーションツールへの進化
  - Azure OpenAI Service / Azure AI Search / Azure API Management を用いた技術構成の仕様策定・PoC 検証を担当し、プロダクトの LLM 移行方針を確立

- クライアント向けテクニカルディレクション
  - Biz メンバーと連携し、クライアント独自データのマネジメント、プロンプトチューニング、追加開発要望の見積もり・要件整理を担当

#### LINE コミュニケーション SaaS「BOTCHAN Relation」のデータ基盤構築

- クライアント向けレポート提供のためのデータ基盤をゼロから設計・構築
  - 約 1 ヶ月でデータ基盤の設計から初期クライアントへのレポート提供までを完了
  - 計測指標の定義を策定し、プロダクト導入前後の効果をレポート化
  - データ基盤の CI にバリデーションを導入し、安全にデプロイできる開発ルールとしてチームに定着

### 副業・業務委託

#### SNIFFOUT Inc.

- [RAG Ready Converter](https://rag-ready-converter.sniffout.net) の開発に参画。Excel・PowerPoint・画像など多様なファイル形式を RAG に適した形式へ変換する SaaS プロダクト
  - 一部の変換失敗が全体を停止させない非同期処理の基盤を設計・構築
  - LLM を活用したドキュメント変換ロジックの開発と、変換精度・処理速度の継続的な改善
  - 既存の AWS インフラを Terraform で IaC 化し、CI/CD を整備
  - 本番運用・障害対応を担当。β 版から正式版リリースまで支え、150 社以上が利用するサービスへ成長

#### 生成 AI 人材育成スクール

- 動画コンテンツ自動生成システムの開発（2024、Python / GitHub Actions / Google Cloud）
  - スライド画像と読み上げ台本から、字幕付きの講義動画を自動生成する仕組みを構築
  - 非エンジニアが素材を置いて PR を出すだけで動画を生成できるワークフローを設計し、制作フローを内製化
  - 差分検知で変更のあったレクチャーのみ再生成し、CI の実行時間と音声合成 API のコストを抑制
  - 要件定義から運用までを主導

---

## 技術スタック

### 言語

- Python
- SQL
- TypeScript
- Shell Script

### クラウド・インフラ

- Google Cloud
- AWS
- Azure
- Terraform (HCL)
- Kubernetes
- Docker
- GitHub Actions

### DWH・データモデリング

- BigQuery
- dbt (Platform / Core)
- Dataform

### データガバナンス・セキュリティ

- BigQuery ポリシータグ（列レベルセキュリティ）
- Dataplex
- Cloud DLP
- Cloud IAM（Terraform による権限管理）

### BI

- Looker
- Looker Studio
- LookML

### ETL・ワークフロー

- TROCCO
- Embulk
- Digdag
- dbt Platform
- GitHub Actions

### 機械学習・AI

- PyTorch
- Agent Development Kit (ADK)
- Model Context Protocol (MCP)
- Dify
- Claude Code Actions
- Azure OpenAI Service / Azure AI Search

---

## 学歴・資格

- 東京理科大学 応用生物科学科（2022 年 3 月卒業）
- Google Cloud Professional Data Engineer（2025 年 5 月取得）

---

## 自己PR

### データガバナンスによる統制と信頼性の担保

データを増やすことよりも、安全に使える状態を保つことに価値があると考えています。個人情報の参照範囲を絞り、権限をコードで管理して定期的に見直す運用をつくってきました。仕組みを入れて終わりにせず、成熟度を定期的に評価しながら改善を続けています。

### データ基盤のゼロからの構築・運用

データ基盤が存在しない状態から、要件定義・技術選定・設計・構築・運用までを一貫して担ってきました。構築して終わりではなく、データアナリストや事業部メンバーが自律的にデータを活用できることをゴールに設計しています。直近では事業部メンバーへ運用を委任し、データチームを介さずにデータ活用が回るようにしました。

### ビジネス課題を起点としたソリューション設計

事業部門が抱える課題を直接ヒアリングし、データやツールで解決するプロセスを重視しています。経営企画や営業・CS など非エンジニア職と要件をすり合わせ、具体的な指標やデータモデルへ落とし込んできました。

---

## 今後の展望

データ規模の拡大よりも、統制と信頼性によってデータの価値を高める方向を伸ばしたいと考えています。これまでプロジェクト単位で進めてきたセキュリティとガバナンスを、組織全体の設計として扱えるようになることが当面の目標です。あわせて、データ契約や SLO のようにデータの品質を利用者へ約束する仕組みと、AI エージェントが安全にデータを扱える提供のかたちにも取り組んでいきたいと考えています。

---

## 業務外活動

### 登壇

- [事業拡大と共に歩むプラットフォームへの道 Google Cloudによる拡張可能なデータ基盤](https://speakerdeck.com/ktagashira/shi-ye-kuo-da-togong-nibu-mupuratutohuomuhenodao-google-cloudniyorukuo-zhang-ke-neng-nadetaji-pan)（Google Cloud Community Tech Surge 2026）
- [Findyのユーザーサクセス面談を支えるデータ技術](https://speakerdeck.com/ktagashira/findynoyuzasakusesumian-tan-wozhi-erudetaji-shu)（#TROCCOUG 東京：TROCCO で取り組むデータ活用とリバース ETL / 780 views）
- [データモデリングを通じて管理会計のオペレーションを再設計する](https://speakerdeck.com/ktagashira/detamoderinguwotong-ziteguan-li-hui-ji-nooperesiyonwozai-she-ji-suru)（事業成長に効かせるファインディ流データエンジニアリングの実践 / 1.6k views）
- [ADKを活用して事業部横断の企業検索エージェントを作成した話](https://speakerdeck.com/ktagashira/adkwohuo-yong-siteshi-ye-bu-heng-duan-noqi-ye-jian-suo-ezientowozuo-cheng-sitahua)（ADK 活用の実践事例 AI エージェントの作り方から現場での活用事例まで / 1.3k views）

### テックブログ・記事執筆

- [事業拡大に伴うマルチプロダクトデータ基盤のプラットフォーム化](https://tech.findy.co.jp/entry/2026/03/16/070000)（Findy Tech Blog, 2026/03）
- [MCPとAIエージェントを活用してSlackから複数CRMの顧客情報を横断検索できる仕組みを作った話](https://tech.findy.co.jp/entry/2025/07/08/070000)（Findy Tech Blog, 2025/07）
- [Looker SDKを使ってLookMLのバリデーションCIを自作した話](https://zenn.dev/chabasssy/articles/d3aebc9d30d6b8)（Zenn, 2025/12）
- [Dataformの活用とその効果](https://tech.findy.co.jp/entry/2024/07/01/083000)（Findy Tech Blog, 2024/07）
- [Google Cloud Professional Data Engineer合格記(2025.5)](https://zenn.dev/chabasssy/articles/e2e90956e4824c)（Zenn, 2025/05）
- [dbt / Dataformで管理外のテーブルを削除して、気持ち良く正月を迎えたい](https://zenn.dev/chabasssy/articles/27e37e51eb0125)（Zenn, 2024/12）

### OSS

- [adk-slack-adapter](https://github.com/ktagashira/adk-slack-adapter) - Google Agent Development Kit で作成したエージェントと Slack を連携するためのツール
