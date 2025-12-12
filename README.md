
# Kestra dbt Sample

Kestraでdbtワークフローをオーケストレーションするサンプルプロジェクト

## 前提条件

- Docker & Docker Compose
- MotherDuckのトークン

## セットアップ

1. `.env`ファイルを作成してMotherDuckトークンを設定
  * MotherDuckからトークンを取得し、base64エンコードして`.env`に設定します。


2. 起動

```bash
docker-compose up -d
```

3. アクセス

- Kestra UI: http://localhost:8080

## ワークフロー実行

1. Kestra UIで `Flows` → `com.example.dbt` → `dbt_build` に移動
2. `Execute` をクリック

## プロジェクト構成

```
workflow/          # Kestraワークフロー定義
kestra_dbt/        # dbtプロジェクト
  ├── models/      # dbtモデル
  └── seeds/       # サンプルデータ
```

## 参考

- [Kestra Docs](https://kestra.io/docs)
- [dbt Docs](https://docs.getdbt.com/)