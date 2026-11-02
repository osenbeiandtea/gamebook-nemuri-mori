# 眠りの森の王子(FILWEN TALES)

ゲームブック風のアプリです。`index.html` を開くと遊べます。

## フォルダの中身
- `index.html` … アプリ本体
- `images/` … 挿絵(WebP)と、動画の再生前の表紙(`poster_番号.webp`)
- `videos/` … 動画(mp4)。28、37〜41の6本と、ボーナス映像(`bonus.mp4`)
- `favicon.svg` / `favicon.ico` / `favicon-32.png` / `favicon-192.png` / `apple-touch-icon.png` … ブラウザのタブやホーム画面に出るアイコン

## 公開のしかた(GitHub Pages)
1. GitHubで新しいリポジトリを作る(Publicにする。無料のPagesはPublicのみ)
2. zipを解凍し、**中身**(フォルダそのものではなく)を「Add file」→「Upload files」でドラッグする
3. 「Commit changes」を押す
4. 「Settings」→「Pages」→ Source を「Deploy from a branch」、Branch を `main` / `(root)` にして Save
5. 1〜2分待つと、`https://osenbeiandtea.github.io/gamebook-nemuri-mori/` で開ける

すでに公開しているときは、同じ手順で上書きアップロードします(変わったファイルだけでも大丈夫)。
アイコンが前のままのときは、ブラウザのキャッシュが残っています。タブを閉じて開き直すか、強制再読み込みしてください。

## 制作者用: テスト表示
公開版では、テスト表示(空の挿絵枠、パズルのスキップ、現在の状態の表示)は隠れています。
確認したいときだけ、アドレスの末尾に `?test=1` を付けて開くと、「テスト表示」の切り替えが現れます。
テスト表示のあいだは、結末を5つ集めていなくても、ボーナス映像のボタンが出ます。

## ボーナス映像
結末を5つ集めると、表紙の「結末の記録」の下に「ボーナス映像を見る」ボタンが出ます。
動画は `videos/bonus.mp4`、再生前の表紙は `images/poster_bonus.webp` です。

## 動画を差し替える・足すとき
1. mp4(10MB以下)を `videos/` に入れる
2. `index.html` の `const VIDEOS = {` のあたりで、該当の行の `url` を `'videos/ファイル名.mp4'` にする
3. 再生前の表紙にしたい絵は `images/` に入れて、`VIDEO_POSTER` に `番号: "images/ファイル名.webp"` を足す
