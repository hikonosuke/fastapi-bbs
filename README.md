📘 FastAPI BBS — 掲示板アプリ開発テンプレート

このリポジトリは、Web応用演習II（FastAPI） の授業で使用する
掲示板アプリ（BBS：Bulletin Board System） のテンプレートです。

学生はこのリポジトリを clone して、自分の GitHub に push した上で開発を進めます。

🚀 機能（このテンプレートに含まれるもの）

FastAPI の最小構成

Docker / Docker Compose による実行環境

/docs（Swagger UI）による API 確認

空のルーター routers/threads.py

ルーティング登録済み（まだ中身は空）

ここから授業で 1機能ずつ増やしていきます。

📂 ディレクトリ構成（最小版）
project-root/
│  Dockerfile
│  docker-compose.yml
│  requirements.txt
│
└─ app/
    │ main.py
    └─ routers/
         │ __init__.py
         │ threads.py

🐳 実行方法（Docker）

※ Docker Desktop がインストールされている必要があります。

1. イメージのビルド
docker compose build

2. アプリの起動
docker compose up

3. Swagger UI の確認
http://localhost:8000/docs

📝 今後の授業でやること（ロードマップ）

GET /threads の実装（ダミー）

POST /threads の実装（スレッド作成）

Pydantic による型定義（ThreadCreate / ThreadRead）

SQLite + SQLAlchemy の導入

スレッドごとの投稿（/posts）

ページネーション

検索機能

画像アップロード

レスポンスの整形（ModelSerializer 風）

👨‍🏫 学生への開発手順（超重要）
1. 先生のリポジトリを clone
git clone https://github.com/hikonosuke/fastapi-bbs.git
cd fastapi-bbs

2. 自分の GitHub に新しく空のリポジトリを作る

例： fastapi-bbs-yourname

3. remote を付け替える
git remote remove origin
git remote add origin https://github.com/【自分のアカウント】/fastapi-bbs.git

4. 自分の GitHub に push
git push -u origin main


これで 自分専用の開発用リポジトリ が完成します。

📄 ライセンス

授業用テンプレートのため、利用は自由です。
