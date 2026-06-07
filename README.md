# kei487.github.io

https://kei487.github.io

GitHub Pages 用リポジトリ。複数サイトを同居させ、将来それぞれ別リポジトリへ移行できる構成にしています。

## ディレクトリ構成

```
.
├── index.html          # ポータル（ルートのみ）
├── css/portal.css      # ポータル専用 CSS
├── kei487/             # kei487 の個人 HP
│   ├── index.html
│   ├── css/
│   └── assets/
└── demo/               # いさむボーイ（大道芸人）デモ HP
    ├── index.html
    ├── schedule.html
    ├── about.html
    ├── css/
    └── assets/
```

各サイト（`kei487/`、`demo/` など）は **自己完結** しています。CSS・画像はすべてサイト内の相対パスで参照しており、フォルダごと別リポジトリへコピーするだけで移行できます。

## 公開 URL

| サイト | URL |
|--------|-----|
| ポータル | https://kei487.github.io/ |
| kei487 | https://kei487.github.io/kei487/ |
| いさむボーイ（デモ） | https://kei487.github.io/demo/ |

## 別リポジトリへの移行手順

例：`demo/` を新しい GitHub Pages リポジトリへ移す場合

```bash
# 新リポジトリを clone したディレクトリで
cp -r /path/to/kei487.github.io/demo/* .

git add .
git commit -m "Import demo site from kei487.github.io"
git push
```

移行後、`demo/` 内の「ポータルへ戻る」リンク（`../`）は不要になるため削除してください。

## 新しいサイトを追加する

1. ルートに `<サイト名>/` ディレクトリを作成
2. `index.html`、`css/`、`assets/` をその中に配置（すべて相対パス）
3. ルートの `index.html` にリンクを追加
