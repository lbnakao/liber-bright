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

## デザイン更新の反映手順（次回用）
1. Claude Design で「Export → HTML」し、`LIBER BRIGHT LP.html`（画像内蔵の単体ファイル）をダウンロード
2. このフォルダで Claude Code に「ダウンロードした書き出しHTMLを export/ に展開して push して」と依頼
   （中身：`<script type="__bundler/template">` のHTMLと `__bundler/manifest` のbase64画像を `index.html` + `assets/` に分解）
3. `git push origin main` → Render が自動デプロイ（数分）
