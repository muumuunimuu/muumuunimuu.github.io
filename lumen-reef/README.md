# Lumen Reef

画像・3Dモデル・外部ライブラリを使わずに海底を生成する、単一HTMLファイルのWebGL2デモです。

## 起動

`index.html` をChrome・EdgeなどのWebGL2対応ブラウザで開いてください。ネット接続なしでも動作します。

## 操作

- PC: W/A/S/D 移動、マウス 視点、Space/E 浮上、C/Q 潜水、Shift 加速、1〜3 視点切替。
- スマホ: 左の円を操作して移動、画面スワイプで視点移動、右の上下ボタンで浮上・潜水。
- 右下のボタン: 画質切替、Web Audioによる環境音、視点リセット。

地形、岩、海藻、珊瑚、魚、マンタ、粒子は起動時にJavaScriptの計算で生成します。WebGL2でリアルタイム描画します。単体HTMLにすべてのCSS・JavaScript・シェーダーが含まれています。

## Cloudflare Pages に公開する

Cloudflare Dashboard → **Workers & Pages** → **Create application** → **Pages** → **Connect to Git** を選び、リポジトリ `muumuunimuu/muumuunimuu.github.io` を接続します。

- Production branch: `main`
- Framework preset: `None`
- Build command: `exit 0` （または空欄）
- Build output directory: `lumen-reef`
- Root directory: リポジトリのルート（変更なし）

**Save and Deploy** 後に Cloudflare が固有の `*.pages.dev` URL を発行します。以後はGitHubへのpushで自動更新されます。

元記事の [Abyssal Garden](https://github.com/Noniv/abyssal-garden) から発想を得た、別実装のオリジナルデモです。
