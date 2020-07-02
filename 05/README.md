# 5章【ヘッダーとフッターを作ろう】

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
   1. `continuous_exercise_05`というBranchを作成して移動して下さい。
      1. `git checkout -b continuous_exercise_05`
   1. Branchの現在地を確認して下さい。
      1. `git branch` ※`continuous_exercise_05`Branchであれば良い。

**ここまで行ったら教科書に戻り**、読み進みながら、適宜指示のある箇所に関しては、ファイルを編集していきましょう。

教科書を読み終えたら、以下を行ないましょう。
1. ご自身のPC内のローカルリポジトリでの作業
   1. 以下のコマンドを実行し、リモートリポジトリに反映します。
      1. `git add .`
      1. `git commit -m "何かしらのメッセージ"`
         1. 適切なコミットメッセージは学習済みであると思うので、お忘れの方はそちらを復習してみて下さい。
      1. `git push origin continuous_exercise_05`
1. リモートリポジトリ(GitHub)での作業
   1. `continuous_exercise_05`Branchに切り替える。
   1. `master`に向けてPull Requestを作成して下さい。
   
以上で、継続課題の提出は完了です。

---
## 確認問題
※「解答/解説」を見る前に、1度考えて解答した後、ご自身で解答を確認しながら学んで下さい。
### 問1
3番目に大きい見出しを表すタグは何タグですか。

<details>
<summary>解答/解説</summary>
 
```
【解答】
<h3>タグ

【解説】
出しを表すタグ

見出しは英語では"headline"ないし"heading"と言われます。
その頭文字をとって、見出しは<h>に1~6の順番が付いたものとなっています。
1が1番大きい見出し、6が1番小さい見出しです。
使い分けていきましょう。

```
</details>


### 問2
ブロック要素の特徴として正しいのは次のうちどれでしょう。

```
1. 横並びになる
2. 上下に余白が取れない
3. 幅と高さが指定できる
4. 要素の順番を簡単に入れ替えられる
```

<details>
<summary>解答/解説</summary>
 
```
【解答】
3. 幅と高さが指定できる

【解説】
ブロック要素の特徴

1. 横並びになる
これはインライン要素、インラインブロック要素の特徴です。

2. 上下に余白が取れない
これはインライン要素の特徴です。

4. 要素の順番を簡単に入れ替えられる
これはここでは学びませんが、フレックスボックス要素の特徴です。
問題の例としてでしか使いません。

```
</details>

### 問3
以下の要件に従ってWebページを作ってください。

```
【要件】
1. <header>タグ、<h1タグ>、<nav>タグ、<ol>タグ、<li>タグを用いる
　　<header>タグの中に<h1>タグ、<nav>タグがあり、<nav>タグの中に<ol>タグ、
　　<ol>タグの中に<li>タグが4つある構成にする
2. <h1>タグの中身は EXAMPLE とする
3. <li>タグの中身はそれぞれ MENU1 , MENU2 , MENU3 , MENU4 とする
4. それぞれclass名は"headline", "nav", "list", "list-item"とする
5. headerのwidth（横幅）は10%にする
6. headlineのfont-size（文字の大きさ）は22pxにする
7. navの中の文字を中央寄せ（text-align）にする
8. class、"list"にはcssでpadding-left:40px;を適用させる。
   ※リセットCSSの適用でブラウザがデフォルトで持っているcssを打ち消したことでolの番号が表示される領域が消えてしまったことを補うため。
```
#### 完成図
![](https://wals.s3.amazonaws.com/uploads/wals2_content_img/21/97/97_practice.png)

<details>
<summary>解答/解説</summary>
 
```
【解答】
HTML/cssは以下の通りです。
まずは1の要件を元にHTMLを記述していきます。
```
```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>EXAMPLE</title>
  <link rel="stylesheet" href="style.css"> </head>
<body>
  <header>
    <h1></h1>
    <nav>
      <ol>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
      </ol>
    </nav>
  </header>
</body>
</html>
```

```
次に2、3に沿ってHTMLそれぞれの要素に文字を追加します。
```

```html
<header>
  <h1>EXAMPLE</h1>
  <nav>
    <ol>
      <li>MENU1</li>
      <li>MENU2</li>
      <li>MENU3</li>
      <li>MENU4</li>
    </ol>
  </nav>
</header>
```

```
続いて4でclass属性と属性値を割り振ります。
```

```html
<header>
  <h1 class="headline">EXAMPLE</h1>
  <nav class="nav">
    <ol class="list">
      <li class="list-item">MENU1</li>
      <li class="list-item">MENU2</li>
      <li class="list-item">MENU3</li>
      <li class="list-item">MENU4</li>
    </ol>
  </nav>
</header>
```

```
ここまででHTMLの記述は終了です。
続いて5の要件からCSSの記述に移ります。
```

```css
* {
	margin: 0;
	padding: 0;
	box-sizing: border-box;
}

header {
	width: 10%;
}
```

```
最後に6、7、8の要件をCSSに記述し、完成図通りになればクリアです。
```

```css
header {
	width: 10%;
}

.headline {
	font-size: 22px;
}

nav {
	text-align: center;
}

.list {
	padding-left: 40px;
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
<img src="https://user-images.githubusercontent.com/55776672/81010926-03e61080-8e92-11ea-802b-ca823b4d73c8.png" alt="sample.png">
</details>

<details>
<summary>演習の指示(guide.png)</summary>
<img src="https://user-images.githubusercontent.com/55776672/81010922-021c4d00-8e92-11ea-8c14-57cfacd421d5.png" alt="guide.png">
</details>

<details>
<summary>カラーコード(colorcode.png)</summary>
<img src="https://user-images.githubusercontent.com/55776672/81010915-ff215c80-8e91-11ea-8777-dca00715399f.png" alt="guide.png">
</details>

#### 取り組み方
1. 課題に取り組む用のBrunchを作成します。
   1. ブランチ名は `05_exercise_01` として下さい。
1. 課題に取り組んで下さい。
   1. ディレクトリ [05/exercise_01](./exercise_01) に課題に取り組むファイルを作成して下さい。
      1. ※既に存在する`.gitkeep`というファイルは気にしないで下さい。
      1. 作成するファイルは以下の通り。
         1. `index.html`
         1. `style.css`
1. 課題が解き終わったら、Pull Requestを`master`に向けて作成して下さい。
   1. Pull Requestは自動で`master`にMergeされる用に設定されてます。
1. 提出後、[04/exercise_01_answer](./exercise_01_answer)にある解答ファイルを参照し、ご自身で解答を確認して下さい。
