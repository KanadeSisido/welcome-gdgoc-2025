# GDGoC Welcome Event @ Google Shibuya Office

# 01

Web サイトを作ってみよう
最初は Web サイトのひな型を作る

```

<!DOCTYPE html>

<html>

</html>

```

`!DOCTYPE html`はこのファイルが html ファイルであることを明示する．
表示する要素は`<html>...</html>`などの「タグ」で囲う必要がある．

# 02

ひな型つづき

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

head にはページの設定，body にはページの内容を書く．

# 03

文字を追加しよう

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

リンク・画像を追加しよう

リンク追加

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

画像追加

```
<!DOCTYPE html>

<html>
    <head>
    </head>
    <body>
        <h1>こんにちは！</h1>
        <p>合同新歓に来ました☺️</p>
        <a href="www.google.com">Googleのページへ</a>
        <img src="gdgoc-logo-mark.jpg" />
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

`hello-heading`と書きましたが，これは好きな文字列でも OK です．

CSS のほうでは，以下のように書いていきます．

```
.hello-heading {
    color: #ff0000;
}
```

# 07
