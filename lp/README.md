# にこの家 LP（3種）設置・編集ガイド

## 構成

```
lp/
├── lp1_large-dogs.html   … 大型犬向けLP
├── lp2_multi-pets.html   … 多頭飼い向けLP
├── lp3_all-pets.html     … 犬以外のあらゆるペット向けLP
└── assets/
    ├── img/              … 写真（28ファイル）
    └── video/floor.mp4   … 床材の動画
sitemap.xml               … ★リポジトリのルート（index.htmlと同じ階層）に置く
robots.txt                … ★同上（下記の注意参照）
```

## 設置手順

1. `lp/` フォルダの中身を、リポジトリ nicoshouse の `lp/` フォルダへそのままアップロード
2. `sitemap.xml` と `robots.txt` はリポジトリのルート（index.html と同じ場所）へ
3. 公開URL:
   - https://nikonote04.github.io/nicoshouse/lp/lp1_large-dogs.html
   - https://nikonote04.github.io/nicoshouse/lp/lp2_multi-pets.html
   - https://nikonote04.github.io/nicoshouse/lp/lp3_all-pets.html
4. 公開後、Google Search Console に `https://nikonote04.github.io/nicoshouse/sitemap.xml` を登録

## 編集の基本ルール

- **文言修正**: HTMLをテキストエディタで開き、該当の日本語を直接編集
- **写真差し替え**: `assets/img/` に新しい画像を追加し、HTML内の `src="assets/img/xxx.jpg"` を書き換える
  - 推奨サイズ: カルーセル用 幅560px / 魅力セクション用 幅800px / ヒーロー用 幅1300px（JPEG品質70〜80）
- **3LPで共通の箇所**（施設ギャラリー・秩父カルーセル・地図・FAQの共通3問）を変更する場合は、**必ず3ファイルすべてに同じ変更**を入れること
- 予約リンクはすべて `https://nicoshouse.airhost.co/ja`（変更時は全ファイル一括置換）

## まだ残っている写真プレースホルダー

`<div class="ph">写真：〇〇</div>` という灰色の枠が残っている箇所は撮影・差し替え待ち。
枠内のテキストが「どんな写真を入れるべきか」の指定になっている。

- LP1: 魅力01（リビングでくつろぐ大型犬）
- LP2: ヒーロー3枚、魅力01・02・05
- LP3: ヒーロー3枚、魅力01・02

## 注意事項

- **robots.txt の制約**: GitHub Pages のプロジェクトサイトでは robots.txt がドメイン直下に置けないため、クローラーへの効力は限定的。SEO上の実害は小さく、sitemap の Search Console 登録で代替できる
- **地図・所要時間ボタン**: HTTPS 環境でのみ位置情報が動作する（GitHub Pages は標準で HTTPS のため問題なし）
- 未対応のTODO: OGP（SNSシェア画像）、GA4 / Search Console タグ設置、独自ドメイン化（広告開始時）
