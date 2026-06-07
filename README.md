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
    └── index.html      # ★ この1ファイルだけで完結
```

## デモサイトの更新方法（GitHub Web）

1. [demo/index.html](demo/index.html) を GitHub 上で開く
2. 鉛筆アイコン（Edit）をクリック
3. `▼ 編集エリア ▼` と書いてある部分を書き換える
4. 「Commit changes」で保存

ファイル先頭に編集ガイドのコメントがあります。スケジュールは表の行（`<tr>`）をコピーして追加するだけです。

## 公開 URL

| サイト | URL |
|--------|-----|
| ポータル | https://kei487.github.io/ |
| kei487 | https://kei487.github.io/kei487/ |
| いさむボーイ（デモ） | https://kei487.github.io/demo/ |

## 別リポジトリへの移行手順

```bash
# 新リポジトリを clone したディレクトリで
cp /path/to/kei487.github.io/demo/index.html .

git add index.html
git commit -m "Import demo site from kei487.github.io"
git push
```

移行後、フッターの「ポータルへ戻る」リンクは削除してください。

## 新しいサイトを追加する

1. ルートに `<サイト名>/` ディレクトリを作成
2. サイトファイルをその中に配置（すべて相対パス）
3. ルートの `index.html` にリンクを追加
