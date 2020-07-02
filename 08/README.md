# 8章【サイドバーを作ろう】

## 課題概要
 - 継続課題 : 1問
 - 確認問題 : 3問
 - 演習課題 : 1問

---
## 継続課題
教科書を読み進める前に、以下の準備を行ないましょう。

1. ご自身のPC内のローカルリポジトリでの作業
   1. まず、ターミナル（WindowsはGit Bash)上でご自身のPC内のローカルリポジトリに移動して下さい。
   1. `git pull`をして下さい。
   1. `master`Branchに移動して下さい。
      1. `git checkout master`
   1. Branchの現在地を確認して下さい。
      1. `git branch` ※`master`Branchであれば良い。
   1. `continuous_exercise_08`というBranchを作成して移動して下さい。
      1. `git checkout -b continuous_exercise_08`
   1. Branchの現在地を確認して下さい。
      1. `git branch` ※`continuous_exercise_08`Branchであれば良い。

**ここまで行ったら教科書に戻り**、読み進みながら、適宜指示のある箇所に関しては、ファイルを編集していきましょう。

教科書を読み終えたら、以下を行ないましょう。
1. ご自身のPC内のローカルリポジトリでの作業
   1. 以下のコマンドを実行し、リモートリポジトリに反映します。
      1. `git add .`
      1. `git commit -m "何かしらのメッセージ"`
         1. 適切なコミットメッセージは学習済みであると思うので、お忘れの方はそちらを復習してみて下さい。
      1. `git push origin continuous_exercise_08`
1. リモートリポジトリ(GitHub)での作業
   1. `continuous_exercise_08`Branchに切り替える。
   1. `master`に向けてPull Requestを作成して下さい。

以上で、継続課題の提出は完了です。

---
## 確認問題
※「解答/解説」を見る前に、1度考えて解答した後、ご自身で解答を確認しながら学んで下さい。

**この確認問題の問3を行うことで、CARAVANサイトの見た目がほとんど完成します。**

**必ずクリアしてください。**
### 問1
CSSにて、idセレクタで「文字色を赤に設定」の場合と、classセレクタで「文字色を青に設定」の場合とでは、どちらの設定が反映されるでしょうか。

```html
<p id="red" class="blue">この文字の色は何色になるでしょう</p>
```
```css
#red {
  color: red;
}
.blue {
  color: blue;
}
```

<details>
<summary>解答/解説</summary>
 
```
【解答】
id名をセレクタに設定したスタイルが適用される

【解説】
詳細度

CSSには詳細度という概念があります。
詳細度とは、スタイルの指定が重複したときにどのスタイルを優先するかという優先度を定量評価したものです。
詳細度の強さは次のように決められています。詳しくは更に多くありますが、ここでは有名なところを提示します。

1. Inline style … (例 <p style="">)
2. IDセレクタ … (例 #red)
3. 疑似クラス … (例 :nth-child(n)、:hover)
4. クラスセレクタ … (例 .blue)
5. タイプセレクタ … (例 p{...}、h1{...})
6. 全称セレクタ … (例 *{...})

詳細度はWebページ内で一定に保つことが適切とされています。
そのため、一番使いやすいクラスセレクタを使うことが一般的です。
これまでに執拗にclass名を付けてくださいと伝えてきたのはこのような理由があります。

```
</details>

### 問2
疑似クラスを書く際に使う記号として正しいものは、次のうちどれでしょう。
```
1. p/nth-child(n)
2. p;nth-child(n)
3. p%nth-child(n)
4. p:nth-child(n)
```

<details>
<summary>解答/解説</summary>
 
```
【解答】
4. p:nth-child(n)

【解説】
疑似クラス

疑似クラスは使い勝手がよく、HTMLにクラス名を追加などしなくてもスタイルを定義できるので、しっかりと確認しましょう。

```
</details>


### 問3
ここまでで、レイアウト調整はほとんど完了です。ただし、見た目と少しずれている箇所があります。
以下の要件に従って、コードを修正してください。
```
【要件】 

headerの上下に、15pxの余白を設定する（すでに余白が設定されている場合は設定不要）
paginationを設定する（下図参照）
index.htmlのdiv.blog-boxの閉じタグの下に、class名paginationの<div>タグを設定する
.paginationに対して、以下の指定を行う
テキストを中央揃えにする
上側に50pxの余白を設定する
.paginationの子要素に<p>タグを7つ設定する
<p>タグそれぞれに、「<<」「<」「1」「2」「3」「>」「>>」と上から順に表示されるように入力する
.paginationの中にある<p>タグに対して、以下の指定を行う。
横幅、高さを、それぞれ30pxにする
inline-block要素に変更する
文字色を白にする
背景色を#acababに設定する
領域の角を3px丸くする
左右に5pxの余白を設定する
行の高さを30pxにする
```
![](https://wals.s3.amazonaws.com/uploads/wals2_content_img/21/108/108_check.png)

<details>
<summary>解答/解説</summary>
 
```
【解答】
以下のようなコードなれば正解です。
```

`index.html`
```html
<section class="blog">
  <h2 class="blog-headline">Recent Blogs</h2>
  <div class="blog-box">
    <div class="blog-item clearfix"> <img class="blog-image" src="img/forest.jpg">
      <section class="blog-text">
        <h3 class="blog-text-headline"> <a href="single.html">
            Hopeful lessons from<br>
            the battle to save<br>
            rainforests
          </a> </h3>
        <p class="blog-date">June 19, 2017</p> <span class="category">Nature</span> </section>
    </div>
    <div class="blog-item clearfix"> <img class="blog-image" src="img/desert.jpg">
      <section class="blog-text">
        <h3 class="blog-text-headline"> <a href="single.html">
            How to fight<br>
            desertification and<br>
            reverse climate change
          </a> </h3>
        <p class="blog-date">June 17, 2017</p> <span class="category">Nature</span> </section>
      <div>
        <div class="blog-item clearfix"> <img class="blog-image" src="img/sunset.jpg">
          <section class="blog-text">
            <h3 class="blog-text-headline"> <a href="single.html">
            Why I'm rowing<br>
            across the Pacific
          </a> </h3>
            <p class="blog-date">June 16, 2017</p> <span class="category">Adventure</span> </section>
        </div>
        <div class="blog-item clearfix"> <img class="blog-image" src="img/italy.jpg">
          <section class="blog-text">
            <h3 class="blog-text-headline"> <a href="single.html">
            Unseen footage,<br>
            untamed nature
          </a> </h3>
            <p class="blog-date">June 15, 2017</p> <span class="category">Nature</span> </section>
        </div>
        <div class="blog-item clearfix"> <img class="blog-image" src="img/asia.jpg">
          <section class="blog-text">
            <h3 class="blog-text-headline"> <a href="single.html">
            The case for<br>
            engineering our food
          </a> </h3>
            <p class="blog-date">June 14, 2017</p> <span class="category">Culture</span> </section>
        </div>
      </div>
      <div class="pagination">
        <p><<</p>
        <p><</p>
        <p>1</p>
        <p>2</p>
        <p>3</p>
        <p>></p>
        <p>>></p>
      </div>
</section>
```

`style.css`
```css
.blog {
	width: 540px;
	float: left;
	margin-right: 30px;
}

.blog-headline {
	border-bottom: 8px solid #f7f7f7;
	text-align: center;
	line-height: 0.6;
}

.blog-box {
	padding-top: 50px;
}

.blog-item {
	padding-bottom: 20px;
	margin-bottom: 20px;
	border-bottom: 1px solid #f7f7f7;
}

.blog-image {
	float: left;
	height: 180px;
}

.blog-text-headline {
	padding-bottom: 15px;
}

.blog-text {
	float: left;
	padding: 30px 0 0 25px;
}

.blog-date {
	display: inline-block;
	font-size: 12px;
}

.category {
	display: inline-block;
	padding: 5px 8px;
	background-color: #acabab;
	border-radius: 3px;
	color: #fff;
	font-size: 11px;
}

.pagination {
	text-align: center;
	padding-top: 50px;
}

.pagination p {
	display: inline-block;
	width: 30px;
	height: 30px;
	margin: 0 5px;
	color: #fff;
	background-color: #acabab;
	border-radius: 3px;
	line-height: 30px;
}
```
</details>




---
## 演習課題
### 演習1
#### 課題クリア条件
- [ ] Pull Request形式で提出すればクリア

#### 内容
HTMLファイルとCSSファイルを作成し、以下を参考にWebページを作ってみましょう。


<details>
<summary>完成図(sample.png)</summary>
<img src="https://user-images.githubusercontent.com/55776672/81095481-04d57b80-8f40-11ea-8a1a-438cfd3926b7.png" alt="sample.png">
</details>

<details>
<summary>演習の指示(guide.png)</summary>
<img src="https://user-images.githubusercontent.com/55776672/81095476-01da8b00-8f40-11ea-9929-602e2e3c6413.png" alt="guide.png">
</details>



#### 取り組み方
1. 課題に取り組む用のBrunchを作成します。
   1. ブランチ名は `08_exercise_01` として下さい。
1. 課題に取り組んで下さい。
   1. ディレクトリ [08/exercise_01](./exercise_01) に課題に取り組むファイルを作成して下さい。
      1. ※既に存在する`.gitkeep`というファイルは気にしないで下さい。
      1. 作成するファイルは以下の通り。
         1. `index.html`
         1. `style.css`
1. 課題が解き終わったら、Pull Requestを`master`に向けて作成して下さい。
   1. Pull Requestは自動で`master`にMergeされる用に設定されてます。
1. 提出後、[08/exercise_01_answer](./exercise_01_answer)にある解答ファイルを参照し、ご自身で解答を確認して下さい。
