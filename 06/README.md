# 6章【メインビジュアルを作ろう】

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
   1. `continuous_exercise_06`というBranchを作成して移動して下さい。
      1. `git checkout -b continuous_exercise_06`
   1. Branchの現在地を確認して下さい。
      1. `git branch` ※`continuous_exercise_06`Branchであれば良い。

**ここまで行ったら教科書に戻り**、読み進みながら、適宜指示のある箇所に関しては、ファイルを編集していきましょう。

教科書を読み終えたら、以下を行ないましょう。
1. ご自身のPC内のローカルリポジトリでの作業
   1. 以下のコマンドを実行し、リモートリポジトリに反映します。
      1. `git add .`
      1. `git commit -m "何かしらのメッセージ"`
         1. 適切なコミットメッセージは学習済みであると思うので、お忘れの方はそちらを復習してみて下さい。
      1. `git push origin continuous_exercise_06`
1. リモートリポジトリ(GitHub)での作業
   1. `continuous_exercise_06`Branchに切り替える。
   1. `master`に向けてPull Requestを作成して下さい。

以上で、継続課題の提出は完了です。


---
## 確認問題
※「解答/解説」を見る前に、1度考えて解答した後、ご自身で解答を確認しながら学んで下さい。
### 問1
背景画像を設定するプロパティは、次のうちどれでしょう。

```css
1. background-position
2. background-size
3. background-image
4. background-color
```

<details>
<summary>解答/解説</summary>
 
```
【解答】
3. background-image

【解説】
背景の設定

HTMLで生成した箱に背景画像を設定するためのプロパティです。
値に url() というものが必要になるので注意してください。()内に画像までのパスを書きます。
```
</details>


### 問2
色を指定する方法は、代表的なものとして3種類あります。すべての指定方法で「赤」を指定してください。

<details>
<summary>解答/解説</summary>
 
```
【解答】
red, #f00(#ff0000), rgb(255, 0, 0)

【解説】
色指定の方法

まず、色を指定する方法は次の3種類あります。
1. 色名
2. 16進数のカラーコード
3. rgbそれぞれの値を設定する

色名
red, green, yellowなど、メジャーな色であればその名称で指定できます。

16進数のカラーコード
#aabbcc のように、16進数で指定された6桁の数字で色が決められます。
最初の2桁がrgbのr、次の2桁がg、最後の2桁がbです。

rgbの値を設定
rgb(255, 0, 0);
rgbの各要素に対応する0～255までの数字を指定します。

```
</details>


### 問3
次の<p>タグに囲まれた文字の書き方で、正しいのはどちらでしょう。
 ```
1.
<p>私の名前はWebCampです。これから</p>
<p>一緒にスキルをより磨きましょう！</p>

2.
<p> 
      私の名前はWebCampです。これから<br>
      一緒にスキルをより磨きましょう！
</p>
```

<details>
<summary>解答/解説</summary>
 
```
【解答】
２

【解説】
段落の使い方(インデント)

<p>タグはparagraph（段落）の頭文字を指します。
そのため、一つのまとまった意味を持つ文章に改行を入れるという目的で複数のp要素を入れることはいいことではありません。
まとまった文章で改行を入れたい場合は<br>タグを使いましょう。

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
<img src="https://user-images.githubusercontent.com/55776672/81088261-b28f5d00-8f35-11ea-9385-7cc448e95a9f.png" alt="sample.png">
</details>

<details>
<summary>演習の指示(guide.png)</summary>
<img src="https://user-images.githubusercontent.com/55776672/81088253-b0c59980-8f35-11ea-8182-6097619e35e0.png" alt="guide.png">
</details>



#### 取り組み方
1. 課題に取り組む用のBrunchを作成します。
   1. ブランチ名は `06_exercise_01` として下さい。
1. 課題に取り組んで下さい。
   1. ディレクトリ [06/exercise_01](./exercise_01) に課題に取り組むファイルを作成して下さい。
      1. ※既に存在する`.gitkeep`というファイルは気にしないで下さい。
      1. 作成するファイルは以下の通り。
         1. `index.html`
         1. `style.css`
      1. 課題に取り組む際に必要な画像ファイルは、既にディレクトリ[06/exercise_01/img](./exercise_01/img)に配置してあります。
   1. ダウンロードしたimg.zipは解答し、imgディレクトリも[06/exercise_01](./exercise_01)直下に配置して下さい。
1. 課題が解き終わったら、Pull Requestを`master`に向けて作成して下さい。
   1. Pull Requestは自動で`master`にMergeされる用に設定されてます。
1. 提出後、[06/exercise_01_answer](./exercise_01_answer)にある解答ファイルを参照し、ご自身で解答を確認して下さい。
