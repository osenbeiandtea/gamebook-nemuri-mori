# 眠りの森の王子

ゲームブック風のアプリです。`index.html` を開くと遊べます。

## フォルダの中身
- `index.html` … アプリ本体
- `images/` … 挿絵(WebP)と、動画の再生前の表紙(`poster_番号.webp`)
- `videos/` … 動画(mp4)。28、37、38、39、40、41の6本
- `favicon.svg` / `favicon.ico` / `favicon-32.png` / `favicon-192.png` / `apple-touch-icon.png` … ブラウザのタブやホーム画面に出るアイコン(月と白い花)

## 公開のしかた(GitHub Pages)
1. GitHubで新しいリポジトリを作る(Publicにする。無料のPagesはPublicのみ)
2. 「Add file」→「Upload files」で、このフォルダの中身をそのままドラッグ(`images` と `videos` もフォルダごと)
3. 「Commit changes」を押す
4. 「Settings」→「Pages」→ Source を「Deploy from a branch」、Branch を `main` / `(root)` にして Save
5. 1〜2分待つと、`https://ユーザー名.github.io/リポジトリ名/` で開ける

すでに公開しているときは、同じ手順で `index.html`、アイコン、`images`、`videos` を上書きアップロードします。
アイコンが前のままのときは、ブラウザのキャッシュが残っています。タブを閉じて開き直すか、強制再読み込みしてください。

## 動画を差し替える・足すとき
1. mp4(10MB以下)を `videos/` に入れる
2. `index.html` の `const VIDEOS = {` のあたりで、該当の行の `url` を `'videos/ファイル名.mp4'` にする
3. 再生前の表紙にしたい絵は `images/` に入れて、`VIDEO_POSTER` に `番号: "images/ファイル名.webp"` を足す
