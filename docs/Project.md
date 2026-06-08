# プロジェクト作業履歴 (Project.md)

## 実施フェーズ: API設計と環境構築
**実施日**: 2026-06-08

### 実施した作業内容
1. **API設計書の作成**
   - APIファースト設計の方針に基づき、`openapi.yaml` を作成しました。
   - タスク管理（Todo）アプリケーションに必要なCRUD操作（作成、取得、更新、削除）の仕様をOpenAPI 3.0で定義しました。
2. **Spring Bootプロジェクトの初期化**
   - Spring Initializrを利用し、プロジェクトの雛形を展開しました。
   - **主要な依存関係**: Web, Thymeleaf, Spring Data JPA, PostgreSQL Driver, Lombok
3. **ドキュメントの整理と学習ガイドの作成**
   - プロジェクトルートに散らばっていたドキュメント（`Project.md`, `git_setup_memo.md`）を `docs/` 配下に移動し、整理しました。
   - API、REST API、OpenAPI、Swaggerの概念や、「1ボタン1API」の設計思想についてまとめた [api_guide.md](file:///g:/work/sandbox/docs/api_guide.md) を作成しました。
   - 今後の開発アプローチとして「Thymeleaf画面からJavaScriptでREST APIを非同期に呼び出す構成（アプローチ②）」を正式採用しました。

### 現在の状態
- ドキュメント類は `docs/` ディレクトリに整理され、ルート直下はクリーンな状態です。
- 開発方針が「REST API非同期通信（アプローチ②）」に決定したため、次はバックエンド実装とDB環境の構築へ進む準備が整っています。

### 次のステップ
- **データベース環境の構築**: Dockerを利用してローカルにPostgreSQLデータベースを起動し、Spring Bootから接続できるようにします。
- **バックエンド実装**: `openapi.yaml` に基づいたRESTコントローラおよびサービス、リポジトリの実装を開始します。
- **フロントエンド実装**: Thymeleafで画面を構成し、JavaScriptのfetch APIを用いてタスクの非同期操作を実現します。
