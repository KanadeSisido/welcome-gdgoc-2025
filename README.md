# GDGoC Welcome Event @ Google Shibuya Office

# 01

Web サイトを作りましょう！
最初は Web サイトの土台を作ります

```

<!DOCTYPE html>

<html>

</html>

```

`!DOCTYPE html`はこのファイルが html ファイルであることを明示しています．

Web サイトで表示する要素は`<html>...</html>`などの「タグ」で囲う必要があります！

# 02

土台のつづき

```
<!DOCTYPE html>

<html>
    <head>
        /* ページの設定などを書く */
    </head>
    <body>
        /* ページの内容を書く */
    </body>
</html>
```

head にはページの設定，body にはページの内容を書いていきます．

# 03

早速文字を追加してみましょう！

## h1 とは

`<h1> ... </h1>`は見出しです．`h1`の他にも`h2`，`h3`，`h4`，……があり，数字が小さいほど，目立つようになっています．

つまり，`<h1>`には一番目立たせたい内容，例えばページのタイトル，章の名前などを書くことがあります．

## p とは

`<p> ... </p>`は段落を表現します．`p`は段落を意味する`"p"aragraph`の略です．

```

<!DOCTYPE html>

<html>
    <head>
    </head>
    <body>
        <h1>こんにちは！</h1>
        <p>合同新歓に来ました☺️</p>
    </body>
</html>

```

# 04

リンク・画像を追加しましょう！

## リンクを追加

リンクを追加する際は`<a href="...."> ... </a>`を利用します．
`href`のあとにリンク先の URL を書くと，クリックしたときにページ遷移させることができます．

```
<!DOCTYPE html>

<html>
    <head>
    </head>
    <body>
        <h1>こんにちは！</h1>
        <p>合同新歓に来ました☺️</p>
        <a href="www.google.com">Googleのページへ</a>
    </body>
</html>
```

`href`の設定によっては，フォルダ内の他のページにアクセスさせることもできます．

例えば，フォルダ内に別のページの HTML ファイル`mySubPage.html`がある場合，

※こんな感じのフォルダの場合

```
|   index.html
|   styles.css
|   gdgoc-logo-mark.jpg
|   mySubPage.html
```

次のように書くとサブページへのリンクが作れます！

```
<!DOCTYPE html>

<html>
    <head>
    </head>
    <body>
        <h1>こんにちは！</h1>
        <p>合同新歓に来ました☺️</p>
        <a href="mySubPage.html">サブページへ</a>
    </body>
</html>
```

## 画像を追加

```
<!DOCTYPE html>

<html>
    <head>
    </head>
    <body>
        <img src="gdgoc-logo-mark.jpg" />
        <h1>こんにちは！</h1>
        <p>合同新歓に来ました☺️</p>
        <a href="www.google.com">Googleのページへ</a>
    </body>
</html>
```

同じフォルダに画像を入れてください

# 05

文字に色を付けたり，レイアウトを整えてみましょう！
CSS を利用します．

CSS を利用する設定を始めましょう．
まずは，フォルダに CSS ファイルを作成します．

```
style.css
gdgoc-logo-mark.jpg
index.html
```

css にはまだ何も書かなくて大丈夫です．

次に，この CSS を HTML とつなげましょう．

```
<!DOCTYPE html>

<html>
    <head>
        <link rel="stylesheet" href=style.css" />
    </head>
    <body>
        <h1>こんにちは！</h1>
        <p>合同新歓に来ました☺️</p>
        <a href="www.google.com">Googleのページへ</a>
        <img src="gdgoc-logo-mark.jpg" />
    </body>
</html>
```

1 行追加すれば，CSS の準備は OK です．

# 06

早速，「こんにちは！」に色をつけてみましょう．

HTML では class を使って，要素に名前をつけられます．その名前を用いて，CSS で見た目を整えます．

```
<!DOCTYPE html>

<html>
    <head>
        <link rel="stylesheet" href=style.css" />
    </head>
    <body>
        <h1 class="hello-heading">こんにちは！</h1>
        <p>合同新歓に来ました☺️</p>
        <a href="www.google.com">Googleのページへ</a>
        <img src="gdgoc-logo-mark.jpg" />
    </body>
</html>
```

class 名として`hello-heading`と書きましたが，これは好きな文字列でも OK です．

次に，CSS に以下のコードを書いてください．

```
.hello-heading {
    color: #ff0000;
}
```

もし，class 名を好きな文字列にした場合は，CSS の`hello-heading`の部分は自分がつけた class 名に書き換えてください．

すると，このように文字に色がつきます！

![赤色になった「こんにちは！」の文字](./.readme-images/06.png "赤い文字")

# 07

今度は GDGoC のロゴマークを小さくしてみましょう．

img タグに適当な class をつけます．

```
<!DOCTYPE html>

<html>
    <head>
        <link rel="stylesheet" href=style.css" />
    </head>
    <body>
        <h1 class="hello-heading">こんにちは！</h1>
        <p>合同新歓に来ました☺️</p>
        <a href="www.google.com">Googleのページへ</a>
        <img src="gdgoc-logo-mark.jpg" class="gdgoc-logo"/>
    </body>
</html>
```

ここでは class を`gdgoc-logo`としましたが，好きな文字列でも OK です．

次に，CSS に以下のコードを追記します．（既存のコードの上でも下でも大丈夫です！）

```
.gdgoc-logo {
    width: 100px;  /* "width"は幅を指定するプロパティ*/
}
```

もし，class 名を好きな文字列にした場合は，CSS の`gdgoc-logo`の部分は自分がつけた class 名に書き換えてください．

再度ページを確認すると，このようにロゴマークの大きさが変わります！

![ロゴマークが縮小したサイトの画像](./.readme-images/07.png "縮小したロゴマーク")
