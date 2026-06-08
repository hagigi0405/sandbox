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

### 次のステップ（詳細TODOリスト）

#### 1. 【ステップ2】DockerによるDB環境構築 🐳
- [ ] プロジェクトのルートに [docker-compose.yml](file:///g:/work/sandbox/docker-compose.yml) を新規作成し、PostgreSQL 16 のコンテナ設定を記述する
- [ ] ターミナルで `docker compose up -d` を実行し、データベースサーバーを起動する
- [ ] データベース接続ツール（VSCodeのDatabase拡張機能やDBeaverなど）から接続テストを行う
- [ ] [src/main/resources/application.properties](file:///g:/work/sandbox/src/main/resources/application.properties) を [application.yml](file:///g:/work/sandbox/src/main/resources/application.yml) に変更し、データソース（URL, ユーザー名, パスワード）および JPA/Hibernate の設定を追加する

#### 2. 【ステップ4】データベース設計とビジネスロジック実装（バックエンド） 💾
- [ ] タスク情報を格納する `tasks` テーブルの定義を行う Entity クラス [Task.java](file:///g:/work/sandbox/src/main/java/com/example/sandbox/domain/Task.java) を作成する
- [ ] Spring Data JPA を利用したリポジトリ [TaskRepository.java](file:///g:/work/sandbox/src/main/java/com/example/sandbox/domain/TaskRepository.java) を作成する
- [ ] ビジネスロジックを処理するサービスインターフェース [TaskService.java](file:///g:/work/sandbox/src/main/java/com/example/sandbox/service/TaskService.java) と、その実装クラス [TaskServiceImpl.java](file:///g:/work/sandbox/src/main/java/com/example/sandbox/service/TaskServiceImpl.java) を作成する
- [ ] REST API エンドポイントを公開する [TaskRestController.java](file:///g:/work/sandbox/src/main/java/com/example/sandbox/controller/TaskRestController.java) を作成する（`openapi.yaml` のパス定義に合わせる）
- [ ] JUnit 5 を用いて、各 API の動作（タスクのCRUD）を検証するテストコードを作成する

#### 3. 【ステップ5】ThymeleafとJSによるフロントエンド実装 🎨
- [ ] メイン画面となる [index.html](file:///g:/work/sandbox/src/main/resources/templates/index.html) を作成する
- [ ] JavaScript [app.js](file:///g:/work/sandbox/src/main/resources/static/js/app.js) を作成し、タスクの登録・完了・削除時に fetch API で Java の API を呼び出す非同期通信処理を実装する
- [ ] CSS を用いて UI をモダンで美しく整える

