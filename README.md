# 雲南ミニガイド販売セット — 手順

概要：
このリポジトリ／ファイル群は「雲南ミニガイド＋写真パック」を低コストで自動販売するためのテンプレートです。決済と自動配布は Gumroad / Payhip に任せ、静的サイトは GitHub Pages または Netlify でホスティングします。

ステップ（10分〜30分で完了）
1. 商品PDFを作る
   - guide.md をMarkdown→PDFに変換（例：pandoc, Typora, Canva等）
   - 写真パック（ZIP）を作成（使用許諾を明記）

2. Gumroadに登録して商品を作成
   - https://gumroad.com に登録
   - 「New Product」→「Digital Product」→PDFとZIPをアップロード
   - 価格設定（例：¥1,200）
   - 商品ページの公開URLをコピー

3. ランディングページに販売URLを入れる
   - index.html の BUY_LINK を Gumroad の商品URLに差し替え

4. サイトを公開（GitHub Pages または Netlify）
   - GitHub: 新しいリポジトリ作成→index.html と styles.css を push → Settings > Pages で公開
   - Netlify: サイト作成でリポジトリを接続（自動デプロイ）または Drag&Dropで公開

5. テスト購入（自分で1回購入して自動配布を確認）
   - Gumroadはテストツール（または実際に低額で購入）して配布が来ることを確認

6. 宣伝（SNS・ブログ）
   - README 以下の marketing.txt を参考に投稿

コスト
- Gumroad/Payhip: 初期費用0、販売ごとに手数料（プラットフォーム依存）
- Hosting: GitHub Pages / Netlify 無料枠でOK
- ドメイン（任意）: 年間1000〜3000円程度

変更したい点があれば指示してください。Stripeによる自前決済や、S3を使ったワンタイムダウンロード（さらに自動化）へも拡張できます。
