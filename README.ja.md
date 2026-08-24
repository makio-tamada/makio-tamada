<div align="right">

[![English](https://img.shields.io/badge/lang-English-lightgrey?style=flat)](./README.md)
[![日本語](https://img.shields.io/badge/lang-日本語-0A66C2?style=flat)](./README.ja.md)

</div>

# Tama

**統計モデリングからアプリのリリースまで、一気通貫でつくる。**

日本の EC 企業でデータ / ML エンジニアをしています。統計手法の設計、パイプラインの構築、API 化、その上に乗るアプリの実装まで、一連の流れを自分で手がけています。

- 📊 **生存解析と因果推論** — 傾向スコアマッチング、Kaplan–Meier、Cox 比例ハザード
- 🤖 **LLM アプリケーション** — RAG システム、エージェントパイプライン、ベクトル検索
- 🛠️ **自動化** — 手作業の繰り返しを、放っておいても回るパイプラインに変える
- ✍️ つくったものについて [subbrain-works.net](https://subbrain-works.net/) で書いています

---

## 技術スタック

**言語**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Swift](https://img.shields.io/badge/Swift-F05138?style=flat&logo=swift&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

**データ & ML**

![pandas](https://img.shields.io/badge/pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![statsmodels](https://img.shields.io/badge/statsmodels-3F4F75?style=flat)
![lifelines](https://img.shields.io/badge/lifelines-8B5CF6?style=flat)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

**LLM & 検索**

![OpenAI API](https://img.shields.io/badge/OpenAI%20API-412991?style=flat)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![Firestore Vector Store](https://img.shields.io/badge/Firestore%20Vector%20Store-FFCA28?style=flat&logo=firebase&logoColor=black)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat&logo=qdrant&logoColor=white)

**クラウド & インフラ**

![Google Cloud](https://img.shields.io/badge/Google%20Cloud-4285F4?style=flat&logo=googlecloud&logoColor=white)
![Cloud Run](https://img.shields.io/badge/Cloud%20Run-4285F4?style=flat&logo=googlecloud&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)

**開発ツール**

![uv](https://img.shields.io/badge/uv-DE5FE9?style=flat&logo=uv&logoColor=white)
![Ruff](https://img.shields.io/badge/Ruff-D7FF64?style=flat&logo=ruff&logoColor=black)
![mypy](https://img.shields.io/badge/mypy-2A6DB2?style=flat)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat&logo=pytest&logoColor=white)

---

## 主なプロジェクト

> 以下の多くはプライベートリポジトリです（臨床データおよび未公開プロダクトのため）。
> 設計やコードについては、お話しする場で詳しくご説明できます。

### 🏥 生存解析パイプライン &nbsp;<sub>`private`</sub>

医療領域の研究協業のために構築した、臨床データを対象とする time-to-event 解析の再現可能なパイプライン。

- **傾向スコアマッチング**による交絡調整と、バランス診断
- **Kaplan–Meier** 生存曲線と **Cox 比例ハザード**モデリング
- 再利用可能な `src/` ライブラリとしてパッケージ化（前処理 / マッチング / 生存解析 / 評価 / 可視化）し、生データからすべての結果を再現できる構成に

`Python` `lifelines` `scikit-survival` `statsmodels` `pandas`

### 🔍 Stera — Structured-text Extraction & Retrieval Assistant &nbsp;<sub>`private`</sub>

WordPress サイトを RAG ベースのチャット体験に変えるマルチテナント SaaS。サイト運営者が WordPress 管理画面から対象ページを選ぶと、非同期パイプラインがクロール・埋め込み生成・インデックス登録を行い、ショートコードで公開サイトにチャットウィジェットを設置できます。

- 検索基盤に **Firestore Vector Store** を採用 — 固定費ほぼゼロ、リアルタイム更新、GCP ネイティブ統合
- テナントごとの API キー認証を備えた **Cloud Run 上の FastAPI** バックエンド
- RAG パラメータ調整・ナレッジ管理・回答プレビューを行う **React + TypeScript + Vite + Tailwind** の管理コンソール
- Firestore Emulator でローカル完結の再現環境を用意し、GitHub Actions で CI を実行

`FastAPI` `GCP` `Firestore` `React` `TypeScript` `PHP`

### 🎧 TM Beat Studio &nbsp;<sub>`private`</sub>

長尺の Lo-Fi 音楽動画を生成し、人手を介さず YouTube へ公開するエンドツーエンドのパイプライン。デモではなく実際に運用しているシステムです。

- **拡散モデル**による音声生成と、長時間トラックへの結合
- **MoviePy** / FFmpeg による動画合成とレンダリング
- **YouTube Data API** を用いたアップロード・メタデータ付与・公開スケジューリングの自動化

`Python` `diffusers` `MoviePy` `YouTube Data API`

### 📱 iOS アプリ & 開発テンプレート &nbsp;<sub>`private`</sub>

- **Life is Quest** — 目標を RPG のクエストに見立てるゲーミフィケーションタスク管理アプリ。レトロゲーム風 UI（`Swift` / `SwiftUI`）
- **AWS CLF Exam App** — LLM で類似問題を生成する資格学習アプリ。Firestore ベースの Python サービスと学習進捗の統計分析つき（`Swift` / `Python` / `Firestore` / `OpenAI API`）
- **Python Analysis Template** — 分析プロジェクトの出発点となるテンプレート。`uv` + src レイアウト + `Ruff` + `mypy` + `pytest` で、初日から再現性のある状態をつくる

---

## Activity

<sub>言語・コミット統計にはプライベートリポジトリを含みます（リポジトリ名やコミット内容は公開されません）。</sub>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./profile-summary-card-output/github_dark/1-repos-per-language.svg">
  <img src="./profile-summary-card-output/github/1-repos-per-language.svg" width="49%" alt="言語別リポジトリ">
</picture>
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./profile-summary-card-output/github_dark/2-most-commit-language.svg">
  <img src="./profile-summary-card-output/github/2-most-commit-language.svg" width="49%" alt="コミットの多い言語">
</picture>
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./profile-summary-card-output/github_dark/3-stats.svg">
  <img src="./profile-summary-card-output/github/3-stats.svg" width="49%" alt="統計">
</picture>
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./profile-summary-card-output/github_dark/4-productive-time.svg">
  <img src="./profile-summary-card-output/github/4-productive-time.svg" width="49%" alt="活動時間帯">
</picture>

---

## 執筆

データ分析・LLM アプリケーション・自動化についての記事を
**[subbrain-works.net](https://subbrain-works.net/)** で公開しています。上記プロジェクトを進める中でぶつかった問題の記録が中心です。

---

## 連絡先

[![Blog](https://img.shields.io/badge/Blog-subbrain--works.net-0A66C2?style=flat&logo=googlechrome&logoColor=white)](https://subbrain-works.net/)
[![X](https://img.shields.io/badge/X-@tama__program-000000?style=flat&logo=x&logoColor=white)](https://x.com/tama_program)
