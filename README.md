# LIBER BRIGHT LP

株式会社リベルブライトのランディングページ（Claude Design で作成）。

## 構成
- `export/` … デプロイ用の静的サイト（`index.html` + `assets/`）。**これが公開される中身です。**
- `LIBER BRIGHT LP.dc.html` … Claude Design のソース（編集用）
- `assets/` / `uploads/` / `screenshots/` … 制作素材・元データ
- `render.yaml` … Render（静的サイト）デプロイ設定。公開ディレクトリは `./export`

## デプロイ
Render の Static Site として `export` ディレクトリを公開します。
`render.yaml` により Publish Directory は `./export` に設定済みです。
