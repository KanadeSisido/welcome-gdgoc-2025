# GDGoC Japan Welcome Event 2025 @Google Shibuya Office

# 00

Web サイトを作りましょう！

今回のレクチャーではこんな感じのサイトを作ります！
基本的な HTML+CSS を学び，AI の活用方法にも触れていきます！

![完成品](./.readme-images/00.png "完成品")

# 01

さっそく始めましょう！
最初は Web サイトの土台を作ります.

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

`html`タグの中を`head`と`body`という２つのタグで分割します．
`head`にはページの設定，`body`にはページの内容を書いていきます．

# 03

早速文字を追加してみましょう！

## h1 とは

`<h1> ... </h1>`は見出しです．`h1`の他にも`h2`，`h3`，`h4`，……があり，数字が小さいほど，目立つようになっています．

つまり，`<h1>`には一番目立たせたい内容，例えばページのタイトル，章の名前などを書くことがあります．

## p とは

`<p> ... </p>`は段落を表現します．`p`は段落を意味する`"p"aragraph`の略です．

「Lorem」というちょっと長い文章を p タグの中に入れてみましょう．
長い文章でレイアウトを確認する際に使えるダミーテキストです．

```
Lorem, ipsum dolor sit amet consectetur adipisicing elit.
Perspiciatis, illum dolor. Aspernatur magni reiciendis labore totam et
rem, quae voluptates accusantium quas facere sint voluptas cupiditate
maxime nemo inventore numquam?
```

次のようになります．

```

<!DOCTYPE html>

<html>
    <head>
    </head>
    <body>
        <h1>こんにちは！</h1>
        <p>
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            Perspiciatis, illum dolor. Aspernatur magni reiciendis labore totam et
            rem, quae voluptates accusantium quas facere sint voluptas cupiditate
            maxime nemo inventore numquam?
        </p>
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
        <p>
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            Perspiciatis, illum dolor. Aspernatur magni reiciendis labore totam et
            rem, quae voluptates accusantium quas facere sint voluptas cupiditate
            maxime nemo inventore numquam?
        </p>
        <a href="https://x.com/japan">私のXプロフィールへ</a>
    </body>
</html>
```

`href`の設定によっては，フォルダ内の他のページにアクセスさせることもできます．

例えば，フォルダ内に別のページの HTML ファイル`mySubPage.html`がある場合，

※もしこんな感じのファイル構成の場合

```
|   index.html
|   styles.css
|   logo-mark.png
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
        <p>
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            Perspiciatis, illum dolor. Aspernatur magni reiciendis labore totam et
            rem, quae voluptates accusantium quas facere sint voluptas cupiditate
            maxime nemo inventore numquam?
        </p>
        <a href="mySubPage.html">サブページへ</a>
    </body>
</html>
```

## 画像を追加

リンクを追加する際は`<img src="....">`を利用します．
`img`のあとに画像の名前（場所）を書くと，画像を表示できます．

```
<!DOCTYPE html>

<html>
    <head>
    </head>
    <body>
        <img src="logo-mark.png">
        <h1>こんにちは！</h1>
        <p>
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            Perspiciatis, illum dolor. Aspernatur magni reiciendis labore totam et
            rem, quae voluptates accusantium quas facere sint voluptas cupiditate
            maxime nemo inventore numquam?
        </p>
        <a href="https://x.com/japan">私のXプロフィールへ</a>
    </body>
</html>
```

![画像を追加した状態](./.readme-images/04.png "画像を追加した状態")

# 05

<!-- // TODO: <ul>と<li>の使い方を説明（好きな食べ物） -->

次に，自分の好きなものや，情報を列挙できるリストを作成してみましょう．
HTML でリストを作る際には`<ul> ... </ul>`と`<li> ... </li>`を使います．

リストは次のように書きます．

```
<ul>
    <li>リストの１つ目</li>
    <li>リストの２つ目</li>
    <li>リストの３つ目</li>
</ul>
```

上記のコードでこのようなリストができます．

![リスト](./.readme-images/05.png "リスト")

サイトにも自分の好きな食べ物リストを作ってみましょう．

以下のコードを p タグの下に追記します．

```
<h2>好きな食べ物</h2>
<ul>
    <li>うどん</li>
    <li>ラーメン</li>
    <li>ピザ</li>
</ul>
```

コードはこんな感じになります．

```
<!DOCTYPE html>

<html>
    <head>
    </head>
    <body>
        <img src="logo-mark.png">
        <h1>こんにちは！</h1>
        <p>
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            Perspiciatis, illum dolor. Aspernatur magni reiciendis labore totam et
            rem, quae voluptates accusantium quas facere sint voluptas cupiditate
            maxime nemo inventore numquam?
        </p>
        <h2>好きな食べ物</h2>
        <ul>
            <li>うどん</li>
            <li>ラーメン</li>
            <li>ピザ</li>
        </ul>
        <a href="https://x.com/japan">私のXプロフィールへ</a>
    </body>
</html>
```

# 06

<!-- // TODO: CSS に入り，class を使って h1（こんにちは！）に色付けする -->

ここからは，文字に色を付けたり，レイアウトを整えてみましょう！
HTML で作った要素を装飾するには，CSS を利用します．

まずは CSS を利用する設定を始めましょう．
CSS を利用するには`head`タグの中に，`style`タグを書きます！

※CSS を HTML ファイル内に書かず，別のファイルに書く方法もありますが，今回は同じファイルに書いていきます．

```
<!DOCTYPE html>

<html>
    <head>
        <style>

        </style>
    </head>
    <body>
        <img src="logo-mark.png">
        <h1>こんにちは！</h1>
        <p>
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            Perspiciatis, illum dolor. Aspernatur magni reiciendis labore totam et
            rem, quae voluptates accusantium quas facere sint voluptas cupiditate
            maxime nemo inventore numquam?
        </p>
        <h2>好きな食べ物</h2>
        <ul>
            <li>うどん</li>
            <li>ラーメン</li>
            <li>ピザ</li>
        </ul>
        <a href="https://x.com/japan">私のXプロフィールへ</a>
    </body>
</html>
```

これで CSS の準備は OK です．
早速，「こんにちは！」に色をつけてみましょう．

HTML では class を使って，要素に名前をつけられます．その名前を用いて，CSS で見た目を整えます．

装飾したい要素に`class="..."`を追記しましょう．

こんな感じに追記します．

```
<h1 class="hello-heading">こんにちは！</h1>
```

コードはこんな感じになります．

```
<!DOCTYPE html>

<html>
    <head>
        <style>

        </style>
    </head>
    <body>
        <img src="logo-mark.png">
        <h1 class="hello-heading">こんにちは！</h1>
        <p>
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            Perspiciatis, illum dolor. Aspernatur magni reiciendis labore totam et
            rem, quae voluptates accusantium quas facere sint voluptas cupiditate
            maxime nemo inventore numquam?
        </p>
        <h2>好きな食べ物</h2>
        <ul>
            <li>うどん</li>
            <li>ラーメン</li>
            <li>ピザ</li>
        </ul>
        <a href="https://x.com/japan">私のXプロフィールへ</a>
    </body>
</html>
```

class 名として`hello-heading`と書きましたが，これは好きな文字列でも OK です．

次に，`<styles> ... </styles>`の中に以下のコードを書いてください．

```
.hello-heading {
    color: #ff0000;
}
```

`color`は文字の色を変更させるプロパティで，まずは文字を赤くしてみます．

コードはこんな感じになります．

```
<!DOCTYPE html>

<html>
    <head>
        <style>
            .hello-heading {
                color: #ff0000;
            }
        </style>
    </head>
    <body>
        <img src="logo-mark.png">
        <h1 class="hello-heading">こんにちは！</h1>
        <p>
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            Perspiciatis, illum dolor. Aspernatur magni reiciendis labore totam et
            rem, quae voluptates accusantium quas facere sint voluptas cupiditate
            maxime nemo inventore numquam?
        </p>
        <h2>好きな食べ物</h2>
        <ul>
            <li>うどん</li>
            <li>ラーメン</li>
            <li>ピザ</li>
        </ul>
        <a href="https://x.com/japan">私のXプロフィールへ</a>
    </body>
</html>
```

もし，class 名を好きな文字列にした場合は，CSS の`hello-heading`の部分は自分がつけた class 名に書き換えてください．

すると，このように文字に色がつきます！

![赤色になった「こんにちは！」の文字](./.readme-images/06.png "赤い文字")

# 07

今度はロゴマークを小さくしてみましょう．

img タグに適当な class をつけます．

こんな感じにつけます．

```
<img src="logo-mark.png" class="logo-mark">
```

コードはこんな感じになります．

```
<!DOCTYPE html>

<html>
    <head>
        <style>
            .hello-heading {
                color: #ff0000;
            }
        </style>
    </head>
    <body>
        <img src="logo-mark.png" class="logo-mark">
        <h1 class="hello-heading">こんにちは！</h1>
        <p>
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            Perspiciatis, illum dolor. Aspernatur magni reiciendis labore totam et
            rem, quae voluptates accusantium quas facere sint voluptas cupiditate
            maxime nemo inventore numquam?
        </p>
        <h2>好きな食べ物</h2>
        <ul>
            <li>うどん</li>
            <li>ラーメン</li>
            <li>ピザ</li>
        </ul>
        <a href="https://x.com/japan">私のXプロフィールへ</a>
    </body>
</html>
```

ここでは class を`logo-mark`としましたが，好きな文字列でも OK です．

次に，CSS に以下のコードを追記します．（既存のコードの上でも下でも大丈夫です！）

```
.logo-mark {
    width: 100px;  /* "width"は幅を指定するプロパティ*/
}
```

もし，class 名を好きな文字列にした場合は，CSS の`logo-mark`の部分は自分がつけた class 名に書き換えてください．

コードはこんな感じになります．

```
<!DOCTYPE html>

<html>
    <head>
        <style>
            .hello-heading {
                color: #ff0000;
            }

            .logo-mark {
                width: 100px;  /* "width"は幅を指定するプロパティ*/
            }
        </style>
    </head>
    <body>
        <img src="logo-mark.png" class="logo-mark">
        <h1 class="hello-heading">こんにちは！</h1>
        <p>
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            Perspiciatis, illum dolor. Aspernatur magni reiciendis labore totam et
            rem, quae voluptates accusantium quas facere sint voluptas cupiditate
            maxime nemo inventore numquam?
        </p>
        <h2>好きな食べ物</h2>
        <ul>
            <li>うどん</li>
            <li>ラーメン</li>
            <li>ピザ</li>
        </ul>
        <a href="https://x.com/japan">私のXプロフィールへ</a>
    </body>
</html>
```

再度ページを確認すると，このようにロゴマークの大きさが変わります！

![ロゴマークが縮小したサイトの画像](./.readme-images/07.png "縮小したロゴマーク")

コードはこんな感じです！

```
<!DOCTYPE html>

<html>
	<head>
		<style>
			body {
				background-color: #f0f0f0;
			}

			.hello-heading {
				color: #ff0000;
			}

			.logo-mark {
				width: 100px;
				border-radius: 999px;
				border: #999 2px solid;
			}
		</style>
	</head>
	<body>
		<img src="logo-mark.png" class="logo-mark" />
		<h1 class="hello-heading">こんにちは！</h1>
		<p>
			Lorem, ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis,
			illum dolor. Aspernatur magni reiciendis labore totam et rem, quae
			voluptates accusantium quas facere sint voluptas cupiditate maxime nemo
			inventore numquam?
		</p>
		<h2>好きな食べ物</h2>
		<ul>
			<li>うどん</li>
			<li>ラーメン</li>
			<li>ピザ</li>
		</ul>
		<a href="https://x.com/japan">私のXプロフィールへ</a>
	</body>
</html>

```

# 08

ここからは，HTML と CSS を使って，見た目を変えていきましょう 👀

まずは背景色を変更します．

CSS で背景色を変更する場合は`background-color`プロパティを利用します．

✅️ 文字色を変えるのが`color`で，背景色を変えるのが`background-color`です！

画面全体に背景色を入れたいので，`body`タグにスタイルを適用します．

以下のコードを`style`タグの中に入れてください．

```
body {
    background-color: #f0f0f0;
}
```

※今回は`.body`じゃなく`body`になっていることにお気づきでしょうか．class を使う場合は`.(ドット)`を使い，単にタグ名で指定する場合は`body`のようにそのまま書きます．

コードは以下のようになります．

```
<!DOCTYPE html>

<html>
    <head>
        <style>
            body {
                background-color: #f0f0f0;
            }

            .hello-heading {
                color: #ff0000;
            }

            .logo-mark {
                width: 100px;  /* "width"は幅を指定するプロパティ*/
            }

        </style>
    </head>
    <body>
        <img src="logo-mark.png" class="logo-mark">
        <h1 class="hello-heading">こんにちは！</h1>
        <p>
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            Perspiciatis, illum dolor. Aspernatur magni reiciendis labore totam et
            rem, quae voluptates accusantium quas facere sint voluptas cupiditate
            maxime nemo inventore numquam?
        </p>
        <h2>好きな食べ物</h2>
        <ul>
            <li>うどん</li>
            <li>ラーメン</li>
            <li>ピザ</li>
        </ul>
        <a href="https://x.com/japan">私のXプロフィールへ</a>
    </body>
</html>
```

# 09

<!-- ロゴを丸くする方法を解説し(border-radius)，ボーダをつける（border）方法を解説する -->

ロゴに枠線をつけて，丸く切り取ってみましょう！

## 枠線をつける

要素に枠線をつけるには`border`プロパティを使います．

今回はロゴに灰色の枠線をつけてみます．次のように追記してください！

```
.logo-mark {
    width: 100px;
    border: #999 2px solid;
}
```

![borderがついたサイトの画像](./.readme-images/09-0.png "borderがつく")

ここでは，灰色（`#999`）で，枠線のサイズが`2px`の枠線をつけています．

## 丸く切り取る

要素を丸く切り取るには`border-radius`プロパティを使います．

もともと`border-radius`プロパティは，角を丸めるプロパティですが，丸める度合いを大きくすると，円に切り取ることができます．

以下のように追記してみましょう！

```
.logo-mark {
    width: 100px;
    border: #999 2px solid;
    border-radius: 20px;
}
```

こんな感じに角が丸くなります．

![少しロゴの角が丸くなったサイトの画像](./.readme-images/09-1.png "少し角が丸くなる")

丸める度合いを非常に大きな値，`999px`にしてみましょう．

```
.logo-mark {
    width: 100px;
    border: #999 2px solid;
    border-radius: 999px;
}
```

すると，円になります！

![ロゴが丸くなったサイトの画像](./.readme-images/09-2.png "ロゴが丸くなる")

# 10

<!-- top-image（shibuya.webp）を入れる．すると，サイズが良くないので，以下のCSSを適用する -->

ページにメイン画像を追加しましょう！

画像の追加には`<img>`を使います．
まずは以下のコードのように，そのまま追加しましょう．

```
<img src="shibuya.webp">
```

`.webp`は画像フォーマット「WebP」の拡張子です．

以下のように，img タグを追加します．また，このあとのために class として`top-image`を追加しておきます．

```
<!DOCTYPE html>

<html>
    <head>

         ...(コード略)

    </head>
    <body>
        <img src="shibuya.webp" class="top-image">
        <img src="logo-mark.png" class="logo-mark">
        <h1 class="hello-heading">こんにちは！</h1>
        <p>
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            Perspiciatis, illum dolor. Aspernatur magni reiciendis labore totam et
            rem, quae voluptates accusantium quas facere sint voluptas cupiditate
            maxime nemo inventore numquam?
        </p>
        <h2>好きな食べ物</h2>
        <ul>
            <li>うどん</li>
            <li>ラーメン</li>
            <li>ピザ</li>
        </ul>
        <a href="https://x.com/japan">私のXプロフィールへ</a>
    </body>
</html>
```

![Shibuya画像を追加したサイトの画像](./.readme-images/10-0.png "shibuya画像追加")

画像が追加されました 🙌

しかし，少し幅が足りないので，横幅を画面いっぱいにします．
また，高さも`500px`にします．

その際は，以下のような CSS を`style`の中に追記します．

```
.top-image {
    width: 100%;
    height: 500px;
}
```

今の状況を見てみましょう．

![引き伸ばされたShibuya画像が表示されたサイトの画像](./.readme-images/10-1.png "引き伸ばされたshibuya画像")

見た目はいい感じですが，実は横に引き伸ばされてしまっています．

そのため，いい感じに調整します．調整には`object-fit: cover;`というプロパティを用います．

<!-- しかしこれではアスペクト比が良くないので，次のようにする． -->

こんな感じに CSS の`top-image`に追記します．

```
.top-image {
    width: 100%;
    height: 500px;
    object-fit: cover;
}
```

![アスペクト比がちょうどいいShibuya画像が表示されたサイトの画像](./.readme-images/10-2.png "アスペクト比がちょうどいいshibuya画像")

少し分かりづらいですが，縦横比が画像の拡大により，ちょうどいい状態になっていることがわかります．

# 11

<!-- 多分上下左右に余白ができてしまうと思う．

ここで，AIを使う．プロンプトは以下のとおり．
```
HTML+CSSで画像を横100%，縦500pxに表示させたいのですが，端っこに余白ができてしまいます．どうすれば余白を消せますか？

<!DOCTYPE html>

<html>
	<head>
		<style>
			body {
				background-color: #f0f0f0;
			}

			.top-image {
				width: 100%;
				height: 500px;
				object-fit: cover;
			}

			.hello-heading {
				color: #ff0000;
			}
			.logo-mark {
				width: 100px;
				border-radius: 999px;
				border: #999 2px solid;
			}
		</style>
	</head>
	<body>
		<img src="shibuya.webp" class="top-image" />
				<img src="logo-mark.png" class="logo-mark" />
				<h1 class="hello-heading">こんにちは！</h1>
				<p>
					Lorem, ipsum dolor sit amet consectetur adipisicing elit.
					Perspiciatis, illum dolor. Aspernatur magni reiciendis labore totam et
					rem, quae voluptates accusantium quas facere sint voluptas cupiditate
					maxime nemo inventore numquam?
				</p>
				<h2>好きなたべもの</h2>
				<ul>
					<li>うどん</li>
					<li>ラーメン</li>
					<li>ピザ</li>
				</ul>
			<a href="https://x.com/japan" class="my-profile-link"
				>私のXプロフィールへ</a
			>
			<a href="#" class="gradation-link-button">オレンジピール</a>
	</body>
</html>


```

返答は以下のとおり．

```
画像を横幅いっぱいに表示しようとしたときに余白ができてしまうのですね。原因として考えられるのは、<body> や <img> タグにデフォルトで設定されているマージンやパディングです。

以下のいずれかの方法を試してみてください。

方法1: body のマージンを削除する
CSSに以下の記述を追加することで、body 要素のデフォルトのマージンをなくし、画像の端がブラウザの端にぴったりとくっつくようにできます。

CSS
body {
  background-color: #f0f0f0;
  margin: 0; /* 追加 */
}

...

```

これを利用して，解決する．
margin: 0;で解決する見込み
-->

```
body {
    margin: 0;

    background-color: #f0f0f0;
}
```

# 12

<!-- divによるwrappingを説明する．以下のcontents-wrapperやcontentのように，構造化して扱いやすいタグの構造にすることを説明する -->

```
<div class="contents-wrapper">
    <div class="content">
        <img src="logo-mark.png" class="logo-mark" />
        <h1 class="hello-heading">こんにちは！</h1>
        <p>
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            Perspiciatis, illum dolor. Aspernatur magni reiciendis labore totam et
            rem, quae voluptates accusantium quas facere sint voluptas cupiditate
            maxime nemo inventore numquam?
        </p>
    </div>
    <div class="content">
        <h2>好きなたべもの</h2>
        <ul>
            <li>うどん</li>
            <li>ラーメン</li>
            <li>ピザ</li>
        </ul>
    </div>
    <a href="https://x.com/japan" class="my-profile-link"
        >私のXプロフィールへ</a
    >
</div>
```

# 13

<!-- 適切な余白をつける方法を解説する，margin，paddingについて説明．
contents-wrapperは，中の要素について余白を開けるので`padding`を使う．
また，paddingのオプションは -->

```
padding: <上> <右> <下> <左>
```

<!-- になっていることを説明する，忘れたらAIに聞くのもいいよね，って話もする -->

```
.contents-wrapper {
    padding: 0 150px 150px 150px;
}
```

<!-- でコンテンツをいい感じに中央がわに持って行く

好きなたべものやloremの文の余白は以下のCSSで開ける -->

```
.content {
    margin: 50px 0;
}
```

<!-- この時点での制作物はこんな感じ -->

```
<!DOCTYPE html>

<html lang="jp">
	<head>
		<meta charset="utf-8" />
		<title>Hello | MyWebSite</title>
		<style>
			body {
				margin: 0;
				padding: 0;

				background-color: #f0f0f0;
			}

			.top-image {
				width: 100%;
				height: 500px;
				object-fit: cover;
			}

			.contents-wrapper {
				padding: 0 150px 150px 150px;
			}

			.hello-heading {
				color: cadetblue;
			}
			.logo-mark {
				width: 100px;
				border-radius: 999px;
				border: #999 2px solid;
			}

			.content {
				margin: 50px 0;
			}
		</style>
	</head>
	<body>
		<img src="shibuya.webp" class="top-image" />
		<div class="contents-wrapper">
			<div class="content">
				<img src="logo-mark.png" class="logo-mark" />
				<h1 class="hello-heading">こんにちは！</h1>
				<p>
					Lorem, ipsum dolor sit amet consectetur adipisicing elit.
					Perspiciatis, illum dolor. Aspernatur magni reiciendis labore totam et
					rem, quae voluptates accusantium quas facere sint voluptas cupiditate
					maxime nemo inventore numquam?
				</p>
			</div>
			<div class="content">
				<h2>好きなたべもの</h2>
				<ul>
					<li>うどん</li>
					<li>ラーメン</li>
					<li>ピザ</li>
				</ul>
			</div>
			<a href="https://x.com/japan" class="my-profile-link"
				>私のXプロフィールへ</a
			>
		</div>
	</body>
</html>

```

# 14

<!--

テンプレートの使い方を説明する． 今回はButton/RoundedButtonの「オレンジピール」を使う．
HTMLとCSSをコピペしてみる（１つ目のコード）

これを修正して，「オレンジピール」を「私のXプロフィールへ」に変更，URLも変更する．

-->

```
<!DOCTYPE html>

<html lang="jp">
	<head>
		<meta charset="utf-8" />
		<title>Hello | MyWebSite</title>
		<style>
			body {
				margin: 0;
				padding: 0;

				background-color: #f0f0f0;
			}

			.top-image {
				width: 100%;
				height: 500px;
				object-fit: cover;
			}

			.contents-wrapper {
				padding: 0 150px 150px 150px;
			}

			.hello-heading {
				color: cadetblue;
			}
			.logo-mark {
				width: 100px;
				border-radius: 999px;
				border: #999 2px solid;
			}

			.content {
				margin: 50px 0;
			}

            .gradation-link-button {
                /* reset default */
                text-decoration: none;
                outline: none;

                /* layout + shape */
                padding: 10px 20px;
                border-radius: 9999px;
                display: inline-block;

                /* color + design */
                background: linear-gradient(135deg, #ea8800, #ff0077);
                color: #fff;

                /* font */
                font-weight: 500;
                font-size: 16px;
                line-height: 2em;
            }

            .gradation-link-button:hover {
                background: linear-gradient(135deg, #d7a967, #ff6aaf);
            }

		</style>
	</head>
	<body>
		<img src="shibuya.webp" class="top-image" />
		<div class="contents-wrapper">
			<div class="content">
				<img src="logo-mark.png" class="logo-mark" />
				<h1 class="hello-heading">こんにちは！</h1>
				<p>
					Lorem, ipsum dolor sit amet consectetur adipisicing elit.
					Perspiciatis, illum dolor. Aspernatur magni reiciendis labore totam et
					rem, quae voluptates accusantium quas facere sint voluptas cupiditate
					maxime nemo inventore numquam?
				</p>
			</div>
			<div class="content">
				<h2>好きなたべもの</h2>
				<ul>
					<li>うどん</li>
					<li>ラーメン</li>
					<li>ピザ</li>
				</ul>
			</div>
			<a href="https://x.com/japan" class="my-profile-link"
				>私のXプロフィールへ</a
			>
            <a href="#" class="gradation-link-button">オレンジピール</a>
		</div>
	</body>
</html>

```

# 15

<!--

AIと作る方法を説明する

- わからないこと，やりたい表現をAIと相談する　（top画像の中央に文字を入れたい）
- ほしいデザインを作ってもらう（かわいいボタンを作って）
- エラー，バグを相談する（画像に謎の余白が………）


 -->
