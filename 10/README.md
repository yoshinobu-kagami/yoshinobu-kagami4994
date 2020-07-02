# 10章【課題：レスポンシブ対応させよう】

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
   1. `continuous_exercise_10`というBranchを作成して移動して下さい。
      1. `git checkout -b continuous_exercise_10`
   1. Branchの現在地を確認して下さい。
      1. `git branch` ※`continuous_exercise_10`Branchであれば良い。

**ここまで行ったら教科書に戻り**、読み進みながら、適宜指示のある箇所に関しては、ファイルを編集していきましょう。

教科書を読み終えたら、以下を行ないましょう。
1. ご自身のPC内のローカルリポジトリでの作業
   1. 以下のコマンドを実行し、リモートリポジトリに反映します。
      1. `git add .`
      1. `git commit -m "何かしらのメッセージ"`
         1. 適切なコミットメッセージは学習済みであると思うので、お忘れの方はそちらを復習してみて下さい。
      1. `git push origin continuous_exercise_10`
1. リモートリポジトリ(GitHub)での作業
   1. `continuous_exercise_10`Branchに切り替える。
   1. `master`に向けてPull Requestを作成して下さい。

以上で、継続課題の提出は完了です。

---
## 確認問題
※「解答/解説」を見る前に、1度考えて解答した後、ご自身で解答を確認しながら学んで下さい。
### 問1
レスポンシブ対応とは、次のうちのどれを指すでしょう。
```
1. スマートフォン対応
2. タブレット対応
3. プリンター対応
4. テレビ対応
```

<details>
<summary>解答/解説</summary>
 
```
【解答】
1~4全てレスポンシブ対応

【解説】
レスポンシブ対応とは

レスポンシブ対応とは、PC、タブレット、スマートフォンなど、複数の異なる画面サイズをWebサイト表示の判断基準にし、
ページのレイアウト・デザインを柔軟に調整することを指します。
3. プリンター対応
Webページを印刷する際のレイアウト、デザインを調節します。
4. テレビ対応
ディスプレイとしてテレビを使う場合や、テレビでネットサーフィンする際の表示レイアウト、デザインを調整します。

```
</details>

### 問2
viewportの設定に必要なcontent属性値を、次の中から2つ選んでください。
```
1. UTF-8
2. initial-scale=1.0
3. width=device-width
4. minimum-scale=0.7
```

<details>
<summary>解答/解説</summary>
 
```
【解答】
2, 3

【解説】
viewportの設定

viewport設定に必要となるのは2, 3です。

content属性値

viewport設定時に必要となるcontent属性値は
・width=device-width
・initial-scale=1.0
の2つではなく、こちらのどちらか一方です。
上記2点は同じ意味を持つので、片方の記述でviewportの役割を果たします。

```
</details>

### 問3
mediaqueriesの宣言文で正しいのは、次のうちどれでしょう。
```
1. media screen and (max-width: 768px)
2. @media screen and(max-width: 768px)
3. @media screen and (max-width: 768px)
4. @media screen (max-width: 768px)
```

<details>
<summary>解答/解説</summary>
 
```
【解答】
3. @media screen and (max-width: 768px)

【解説】
mediaqueriesの宣言

こちらのmediaqueriesの宣言文はしっかり覚えてください。
また、必ず注意していただきたい点が、
@media screen and () というように、それぞれの単語の間だけでなく、
andと()の間にも半角スペースが空いていることにも気を付けてください。
こちらのスペースを1ヶ所忘れてしまうだけでmediaqueriesの宣言が機能しなくなります。
```
</details>


---
## 演習課題
### 演習1
#### 課題クリア条件
- [ ] Pull Request形式で提出し、メンターのレビューに通過して合格すること
- [ ] メンターからのレビューを受け、修正点があれば修正し、再度提出する

#### 内容
9章の演習問題で作ったサイトを、レスポンシブ対応にしましょう。
パソコン表示では横並びになっているboxを、768px以下では縦並びになるようにしましょう。
※課題で使用する画像は、9章の演習問題と同じものです。
また、レスポンシブ対応の際は、google chromeのデベロッパーツールを用いながら確認しましょう。

<details>
<summary>完成図(sample.png)</summary>
<img src="https://user-images.githubusercontent.com/55776672/81104646-cb0b7180-8f4d-11ea-9870-c00b9a1f720c.png" alt="sample.png">
</details>

<details>
<summary>演習の指示(guide.png)</summary>
<img src="https://user-images.githubusercontent.com/55776672/81104664-cfd02580-8f4d-11ea-89e1-08333afbda2d.png" alt="guide.png">
</details>



#### 取り組み方
1. 課題に取り組む用のBrunchを作成します。
   1. ブランチ名は `10_exercise_01` として下さい。
1. 課題に取り組んで下さい。
   1. ディレクトリ [10/exercise_01](./exercise_01) に課題に取り組むファイルを用意して下さい。
      1. ※既に存在する`.gitkeep`というファイルは気にしないで下さい。
      1. 9章で作成した以下のファイルをコピーして[10/exercise_01](./exercise_01)に配置して下さい。
         1. `index.html`
         1. `style.css`
1. 課題が解き終わったら、Pull Requestを`master`に向けて作成して下さい。

**この課題のPull Requestは自動で`master`にMergeされません。**
**今回はHTML/CSSの最終課題となりますので、解答はご用意しておりません。**

**提出後、メンターが内容をレビュー(確認や指摘)を行ないますので、指摘された部分は修正して、再度提出して下さい。**
