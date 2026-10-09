# ゲームOK！ 勉強チェック(PWA)

## スマホ・タブレットに入れる方法(GitHub Pages の例)
1. GitHub で新しいリポジトリを作り、このフォルダのファイルを全部アップロードする
2. リポジトリの Settings → Pages で、Branch を `main` / `(root)` にして保存
3. 数分後に表示される URL(https://〜.github.io/〜/)を Android の Chrome で開く
4. メニュー(︙)→「ホーム画面に追加」または「アプリをインストール」

一度開けば、以降はオフラインでも動きます。HTTPS で配信できる場所なら、Netlify や Cloudflare Pages でも同じです。

## ファイル
- index.html … アプリ本体(画面・データ処理・効果音すべて)
- sw.js … オフライン用のキャッシュ
- manifest.webmanifest / icon-*.png … ホーム画面に追加するための情報とアイコン

## 更新するとき
index.html を直したら、sw.js の `CACHE = "gameok-v1"` の数字を上げてからアップロードしてください。端末側で新しい版に切り替わります。

## データについて
データは端末のブラウザ内(IndexedDB)だけに保存されます。設定 → バックアップ から JSON ファイルを書き出せます。端末ごとにデータは別々です。
