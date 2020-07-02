# 9章【サイトを仕上げよう】

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
   1. `continuous_exercise_09`というBranchを作成して移動して下さい。
      1. `git checkout -b continuous_exercise_09`
   1. Branchの現在地を確認して下さい。
      1. `git branch` ※`continuous_exercise_09`Branchであれば良い。

**ここまで行ったら教科書に戻り**、読み進みながら、適宜指示のある箇所に関しては、ファイルを編集していきましょう。

教科書を読み終えたら、以下を行ないましょう。
1. ご自身のPC内のローカルリポジトリでの作業
   1. 以下のコマンドを実行し、リモートリポジトリに反映します。
      1. `git add .`
      1. `git commit -m "何かしらのメッセージ"`
         1. 適切なコミットメッセージは学習済みであると思うので、お忘れの方はそちらを復習してみて下さい。
      1. `git push origin continuous_exercise_09`
1. リモートリポジトリ(GitHub)での作業
   1. `continuous_exercise_09`Branchに切り替える。
   1. `master`に向けてPull Requestを作成して下さい。

以上で、継続課題の提出は完了です。

---
## 確認問題
※「解答/解説」を見る前に、1度考えて解答した後、ご自身で解答を確認しながら学んで下さい。

**新しくHTMLファイルとCSSファイルを作成し、以下の問題に解答してください。**
### 問1
Font Awesomeで「Twitter」と「Facebook」のアイコンを挿入し、サイズを32pxに変更してください。

<details>
<summary>解答/解説</summary>
 
```
【解答】
HTML/CSSは以下の通りです。
```

```html
<html>
<head>
  <meta charset="UTF-8">
  <title></title>
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.0.13/css/all.css">
  <link rel="stylesheet" href="style.css"> </head>
<body> <i class="fab fa-twitter"></i> <i class="fab fa-facebook"></i> </body>
</html>
```

```css
.fab {
	font-size: 32px;
}
```

```
【解説】
ここではFont Awesomeの導入にCDNを用いています。

CDNとは

Content Derivery Networkの略称。
Webコンテンツを配信する役割を持ち、ファイルのダウンロードなどが必要ないため、
Webページ自体が軽くなるというメリットがあります。
```
</details>

### 問2
挿入されたFont Awesomeアイコンを囲むように`<div>`タグを設定し、class名をpositionとしてください。
	
※解答/解説は問3の解答/解説とともに載せてますので、そちらでご確認下さい。

### 問3
class名「position」をセレクタとして、「Twitter」と「Facebook」のアイコンを右側から40pxで上側から100pxの場所へpositionを使って移動してください。


<details>
<summary>解答/解説</summary>
 
```
【解答】
HTML/CSSは以下の通りです。
```

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title></title>
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.0.13/css/all.css">
  <link rel="stylesheet" href="style.css"> </head>
<body>
  <div class="position"> <i class="fab fa-twitter"></i> <i class="fab fa-facebook"></i> </div>
</body>
</html>
```

```css
.position {
	position: absolute;
	top: 100px;
	right: 40px;
}
```

```
完成図です。こちらを参考にしてください。
```
![](https://s3-ap-northeast-1.amazonaws.com/wals/uploads/study_confirm/21/122/8_4.png)

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
<img src="https://user-images.githubusercontent.com/55776672/81102080-09069680-8f4a-11ea-84b9-df6e73b5b80a.png" alt="sample.png">
</details>

<details>
<summary>演習の指示(guide.png)</summary>
<img src="https://user-images.githubusercontent.com/55776672/81102075-073cd300-8f4a-11ea-9f62-01d0bb96c19c.png" alt="guide.png">
</details>



#### 取り組み方
1. 課題に取り組む用のBrunchを作成します。
   1. ブランチ名は `09_exercise_01` として下さい。
1. 課題に取り組んで下さい。
   1. ディレクトリ [09/exercise_01](./exercise_01) に課題に取り組むファイルを作成して下さい。
      1. ※既に存在する`.gitkeep`というファイルは気にしないで下さい。
      1. 作成するファイルは以下の通り。
         1. `index.html`
         1. `style.css`
      1. 課題に取り組む際に必要な画像ファイルは、既にディレクトリ[09/exercise_01/img](./exercise_01/img)に配置してあります。
1. 課題が解き終わったら、Pull Requestを`master`に向けて作成して下さい。
   1. Pull Requestは自動で`master`にMergeされる用に設定されてます。
1. 提出後、[09/exercise_01_answer](./exercise_01_answer)にある解答ファイルを参照し、ご自身で解答を確認して下さい。
