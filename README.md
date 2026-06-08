# Sandbox Project

Java 21, Spring Boot 3, PostgreSQL, Thymeleaf の学習用サンドボックスプロジェクトです。
ユーザー（漂泊者）と長離（Antigravity）でペアプログラミングを行いながら開発を進めます。

---

## 📌 プロジェクト概要
このプロジェクトは、APIファースト設計を取り入れたタスク管理（Todo）アプリケーションです。
画面はThymeleafで構成しつつ、データの登録や取得はJavaScriptからREST APIを非同期に呼び出す構成（アプローチ②）で実装します。

## 📁 ドキュメント一覧 (docs/)
プロジェクトの設計書や学習メモは、プロジェクトの整理整頓のため `docs/` ディレクトリに集約しています。

* **[作業履歴・現在のフェーズ (Project.md)](file:///g:/work/sandbox/docs/Project.md)**
  * これまでに実施した作業や、現在の進捗、次のステップなどを記録しています。
* **[Gitセットアップメモ (git_setup_memo.md)](file:///g:/work/sandbox/docs/git_setup_memo.md)**
  * GitHubとの連携方法や、初期プッシュに関する手順をまとめています。
* **[API & OpenAPI学習ガイド (api_guide.md)](file:///g:/work/sandbox/docs/api_guide.md)**
  * REST APIの設計思想（1ボタン1APIなど）や、OpenAPI/Swaggerとの違いについて解説したガイドです。

---

## 🚀 現在のフェーズと次のステップ
現在の詳細なステータスについては、[Project.md](file:///g:/work/sandbox/docs/Project.md) を参照してください。

1. **API設計書の作成 (openapi.yaml)** ➔ 策定済み。
2. **Spring Bootプロジェクトの初期化** ➔ 展開済み。
3. **バックエンドおよびフロントエンドの実装（次のフェーズ）** ➔ DB接続設定（Docker）と、APIの実装へ移行します。

