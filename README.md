# SEO・GA4・Search Console設定済みLPサンプル（GitHub Pages）

`index.html` をトップページとして使う、GitHub Pages用のサンプルです。HTMLに基本的なSEOメタ情報、GA4タグ、Search Console所有権確認用タグを入れています。画像とファビコンは `img/` に含まれています。

## 公開前に必ず置き換える項目

1. `index.html` の `G-REPLACE_WITH_YOUR_MEASUREMENT_ID` を、自分のGA4ウェブデータストリームの測定ID（`G-`から始まるID）に置き換えます。コード内の2か所を同じIDにします。
2. `REPLACE_WITH_YOUR_SEARCH_CONSOLE_VERIFICATION_CODE` を、Search Consoleが発行したHTMLタグの `content` の値に置き換えます。`<meta name="google-site-verification" ...>` 全体をSearch Consoleのタグと置き換えても構いません。
3. `title` と `description` を、自分のLPの内容に合わせて書き換えます。現在の文章はサンプルです。
4. `id="application"` セクションのフォームURLを自分のGoogleフォームに置き換えます。

## GA4タグの取得と確認

GA4でウェブデータストリームを作成し、測定IDをコピーします。`index.html` の `<head>` にあるサンプルIDを置き換えてからGitHubにアップロードします。サイト公開後、GA4のリアルタイムレポートやGoogle Tag Assistantでタグの動作を確認します。データがレポートに表示されるまで時間がかかる場合があります。

## Search Consoleの所有権確認

1. Search ConsoleでURLプレフィックスのプロパティを作成し、HTMLタグによる確認方法を選びます。
2. 発行されたメタタグの `content` の値をHTMLに設定します。
3. GitHub Pagesへ公開してから、Search Consoleに戻って「確認」を実行します。

Search ConsoleのHTMLタグ確認には、公開されたトップページの `<head>` に正しいタグがあり、誰でもページを開ける必要があります。タグは確認後も削除しないでください。

## SEOメタ情報の調整

`<title>` と `meta name="description"` は、ページごとに内容を短く正確に表す文章へ変更してください。`robots.txt` は検索エンジンの巡回を許可する設定です。ページ本文の見出しや画像の代替テキスト（alt）も、ページの内容に合わせて調整しましょう。

## GitHub Pagesへのアップロード

1. ZIPを展開します。
2. 展開したフォルダの**中身**をGitHubリポジトリのrootにアップロードしてcommitします。
3. GitHubの **Settings → Pages** で、公開ブランチとrootフォルダを選びます。
4. 公開されたURLを開き、ページ、画像、フォームボタンを確認します。
5. GA4タグとSearch Consoleの所有権確認をそれぞれテストします。

## 含まれるファイル

- `index.html`：GitHub Pagesのトップページ
- `index_google_form_button.html`：同内容の別名HTML
- `style.css`：ページデザイン
- `script.js`：メニューの動作
- `img/`：サンプル画像とファビコン
- `robots.txt`：検索エンジン巡回設定

## 参考（Google公式）

- [GA4のGoogle tag設定](https://support.google.com/analytics/answer/15756615?hl=ja)
- [Search Consoleでサイト所有権を確認](https://support.google.com/webmasters/answer/9008080?hl=ja)

※フォームURLとGA4測定IDはサンプル用です。公開前に必ずご自身の値に変更してください。
