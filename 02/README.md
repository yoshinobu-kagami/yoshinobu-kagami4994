# 2章【HTML・CSSの基本書式を学ぼう】

## 課題概要
 - 確認問題 : 5問
 - 演習課題 : 1問

---
## 確認問題
※「解答/解説」を見る前に、1度考えて解答した後、ご自身で解答を確認しながら学んで下さい。
### 問1
Webページに表示させたい要素は、`<body>`タグ内、`<head>`タグ内のうち、どちらに記入しますか。
<details>
<summary>解答/解説</summary>
 
```
【解答】
<body>タグ

【解説】
<body>タグ、<head>タグ内の要素の棲み分け
<body>タグ内には、Webページに表示させたい情報を記述します。
ex) <p>タグ、<h1>タグ、<img>タグなど <head>タグ内には、Webページ自体の情報を記述します。
<head>タグ内に記述された情報は、<title>タグを除いては通常ブラウザ上に表示されません。
ex) <meta>タグ、<link>タグなど
```
</details>

### 問2
リンクを飛ばすために用いられるタグと属性は、次のうちどれでしょう。 
```html
1. <a src=""></a>
2. <a content=""></a>
3. <a href=""></a>
4. <a lang=""></a>
```
<details>
<summary>解答/解説</summary>

```
【解答】
3. <a href=""></a>

【解説】
<a>要素
<a>タグは"anchor"（船の錨）の略称で、リンクの出発点と到達点を指定するタグです。
出発点は<a>タグを記述するHTMLファイル、到達点はhref属性の値です。
<a>タグに囲まれた部分をクリックすると、href属性値に移動します。
```

`例`
```html
<a href="https://web-camp.io/">WebCampへのリンク</a>
# 「WebCampへのリンク」という文字をクリックすると "https://web-camp.io/" に移動する
```
</details>

### 問3
文字化けを防ぐために使われる要素は、次のうちどれでしょう。
```html
1. <meta charset="UTF-7">
2. <meta charset="UTF-8">
3. <meta name="description">
4. <meta name="viewport">
```

<details>
<summary>解答/解説</summary>

```
【解答】
2. <meta charset="UTF-8">

【解説】
文字化けを防ぐ要素

<meta>タグは、Webページの情報を定義するためのタグです。
属性は様々なものを持ちますが、ここではcharset属性を使います。
charsetは"charactor set"の略称で、日本語で言うところの「言語設定」という意味を持ちます。
UTF-8属性値は文字コードと呼ばれるもので、コンピュータ上で文字を扱うために個々の文字、記号に割り当てられた固有の番号を指します。
世界で最もポピュラーな文字コードですので、UTF-8だけはしっかりと覚えてください。
```
</details>



### 問4
HTMLとCSSファイルを関連付けるために必要な要素は、次のうちどれでしょう。
```html
1. <link rel="stylesheet" href="">
2. <link rel="stylesheet" src="">
3. <css rel="stylesheet" href="">
4. <css rel="stylesheet" src="">
```

<details>
<summary>解答/解説</summary>

```
【解答】
1. <link rel="stylesheet" href="">

【解説】
HTMLファイルとCSSファイルの紐付け

HTMLファイルと外部ファイルを紐付けるには、<link>タグを用います。
<link>要素は<head>タグ内に含まれます。
主にCSSファイルとの紐付けに用いられる要素ですので、その用途は確実に覚えましょう。
rel属性は現在の文書からみた、リンク先となるリソースの位置づけを表します。
属性値がリソースを表すものなので、CSSをリンク先とする際の属性値は"stylesheet"となります。
```
</details>



### 問5
正しい記述は、次のうちどちらでしょう。
```html
1. 
<div id="content"></div>
<div id="content"></div>
<div id="content"></div>

2.
<div class="content"></div>
<div class="content"></div>
<div class="content"></div>
```

<details>
<summary>解答/解説</summary>

```
【解答】
2. class属性指定

【解説】
id属性とclass属性の使い分け

id属性は、1つのWebページで同じ値を複数持つことができません。
class属性は1つのWebページで同じ値を複数持つことができるので、今回のような<div>タグが3つ並び、同じスタイルを指定したいという場合にはclass属性をつけるのが適切です。
```
</details>

---
## 演習課題
### 演習1
#### 課題クリア条件
- [ ] Pull Request形式で提出すればクリア

#### 内容
HTMLファイルとCSSファイルを作成し、以下の画像を参考にWebページを作ってみましょう。
「sample.png」が完成図、「guide.png」が演習の指示になります。

指示の箇所以外は、ご自身で決めて作られてかまいません。たとえば、今回のaタグの指示ではhrefで設定する内容はお任せいたします。
以降の章における演習課題も同様です。

<details>
<summary>完成図(sample.png)</summary>
<img src="https://user-images.githubusercontent.com/55776672/80409345-adae2600-8903-11ea-9b09-782432fefba0.png" alt="sample.png">
</details>

<details>
<summary>演習の指示(guide.png)</summary>
<img src="https://user-images.githubusercontent.com/55776672/80409339-aab33580-8903-11ea-9ba6-27027804c6e9.png" alt="guide.png">
</details>


#### 取り組み方
1. 課題に取り組む用のBrunchを作成します。
   1. ブランチ名は `02_exercise_01` として下さい。
1. 課題に取り組んで下さい。
   1. ディレクトリ [02/exercise_01](./exercise_01) に課題に取り組むファイルを作成して下さい。
      1. ※既に存在する`.gitkeep`というファイルは気にしないで下さい。
      1. 作成するファイルは以下の通り。
         1. `index.html`
         1. `style.css`
1. 課題が解き終わったら、Pull Requestを`master`に向けて作成して下さい。
   1. Pull Requestは自動で`master`にMergeされる用に設定されてます。
1. 提出後、[02/exercise_01_answer](./exercise_01_answer)にある解答ファイルを参照し、ご自身で解答を確認して下さい。
