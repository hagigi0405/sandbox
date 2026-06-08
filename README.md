# Sandbox Project

Java 21, Spring Boot 3, PostgreSQL, Thymeleaf の学習用サンドボックスプロジェクトです。
ユーザー（漂泊者）とエイメス（Antigravity）でペアプログラミングを行いながら開発を進めます。

---

## 📌 会話引き継ぎメモ（これまでの経緯）

以前の会話（会話ID: `1674626b-c270-484a-85ab-a907da593543`）から引き継いだ内容です。

1. **技術スタックの選定**
   漂泊者の実務経験（Java、Docker、PL経験等）を考慮し、実践的でモダンな以下の構成に決定しました。
   - **言語**: Java 21
   - **フレームワーク**: Spring Boot 3 (MVC)
   - **データベース**: PostgreSQL
   - **フロントエンド**: Thymeleaf
   - **インフラ/ツール**: Docker, Git

2. **学習ロードマップ**
   - **APIファースト設計**: Swagger（OpenAPI）でJSON形式のAPI仕様を先にFixさせてからSpring Bootの実装に落とし込む流れを学習します。
   - **環境構築**: Dockerを使ってPostgreSQLをローカルに立ち上げ、接続します。
   - **デプロイ・自動ビルド**: 自動ビルドツールやDockerを使ったデプロイ方法について学習します。

3. **現在までの進捗**
   - 新規フォルダ `g:\work\sandbox` を作成し、`git init` でGitリポジトリを初期化しました。
   - Gitのコミットに必要な `user.name` と `user.email` が未設定の状態です。

---

## 🚀 次のステップ

1. **Gitのユーザー情報設定**
   コミットできるように、以下のコマンドでユーザー名とメールアドレスを設定します。
   ```bash
   git config user.name "Your Name"
   git config user.email "your.email@example.com"
   ```
2. **ワークスペースの切り替え**
   この `g:\work\sandbox` フォルダをIDEのワークスペースとして開き直して、本格的な開発をスタートします。
