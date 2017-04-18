# Stack2images_ver2.0
The most innovative ImageJ macro for automatic Tiff conversion.

**最新版（ver2.0170330） Download: [Windows](https://raw.githubusercontent.com/TM2320/Stack2images_ver2.0/master/download/Stack2images_ver2.0_Win.txt) , [Mac](https://raw.githubusercontent.com/TM2320/Stack2images_ver2.0/master/download/Stack2images_ver2.0_Mac.txt)　（右クリックでリンク先を保存 or 左クリックで開いてコピペ）**

### 0.目次
* [1.Stack2imagesについて](https://github.com/TM2320/Stack2images_ver2.0/blob/master/README.md#1stack2images%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6)

* [2.使い方（簡易版）](https://github.com/TM2320/Stack2images_ver2.0/blob/master/README.md#2%E4%BD%BF%E3%81%84%E6%96%B9%E7%B0%A1%E6%98%93%E7%89%88)

* [3.仕様](https://github.com/TM2320/Stack2images_ver2.0/blob/master/README.md#3%E4%BB%95%E6%A7%98)

* [4.Update history](https://github.com/TM2320/Stack2images_ver2.0/blob/master/README.md#4update-history)

___
### 1.Stack2imagesについて
	
> Tiff画像変換をもっと楽にしたい。―――
> 
> Stack2imagesはそんな思いから生まれました。輝かしいデビューから1年余り。  
> あのStack2imagesがさらなる進化を遂げて帰ってきました！  
> 新たな機能満載のStack2images ver2.0、満を持しての登場です。
	
**Stack2images_ver2.0**（S2v2）は、ImageJによる
* Tiffの階調設定
* 8bitへの変換
* Stackの分割  
* 分割後の色付け・命名・保存  

これらの作業を、あなたに代わって一括処理してくれる、夢のようなバッチスクリプトです。  
何十枚のTiffだって、これがあればもう恐れる必要はありません。その革新性について、  
ここで長々と語るつもりはありません。まずは使ってみてください。  
きっと、忘れられない体験になるでしょう。
___
### 2.使い方（簡易版）  
※S2v2では便宜上、分割前のTiffを「Tiff」、「Tiff」に含まれる1枚1枚の画像を「Stack」と呼んでいます。  
※詳しい解説（画像付き）は同梱の[pdf](https://github.com/tm2320/Stack2images_ver2.0/blob/master/download/S2v2%E4%BD%BF%E7%94%A8%E6%96%B9%E6%B3%95.pdf)をご覧ください。
1. **起動**  
`ImageJを起動します`

2. **D&D**  
`S2v2をImageJにドラッグアンドドロップします`

3. **実行**  
`メニューバーの [Macros] -> [Run Macro] をクリック`  
`または、S2v2のウィンドウをアクティブにした状態で [Ctrl] + [R]`

4. **フォルダ選択**  
`変換したいTiffが保存されているフォルダを選択します`

5. **枚数の設定**  
`Stack枚数（２～６）を設定します`

6. **名前の設定**  
`各Stackに付ける名前を設定します`

7. **色の設定**  
`各Stackに着ける色を設定します`

8. **完了**  
`保存先は、4.で指定したフォルダの中の「output」フォルダです`
___
### 3.仕様
* リフレッシュ機能：実行前にImageJが開いている画像をすべて閉じます。作業中は注意してください。  
* Stack名の重複チェック機能：複数のStackに同じ名前は付けられません。
* 複数色の同時保存に対応：例えばモノクロ画像とカラー画像を同時に保存できます。  
* 分割後の画像は次の形式で命名、保存されます。「元のTiff名」-「Stack名」 (色名).tif  
* Tiffごとに整理して保存：outputフォルダのなかに、さらにTiff別にフォルダが作られます。  
* 上書き回避機能：output内に同名のフォルダがあった場合、フォルダ名を変更して上書きを回避します。  
* ログ出力：output内にログをテキスト形式で保存します。設定内容を確認することができます。  
* 対応OS：Windows＆Mac
___
### 4.Update history  
* 最新版（ver2.0170330） Download: [Windows](https://raw.githubusercontent.com/TM2320/Stack2images_ver2.0/master/download/Stack2images_ver2.0_Win.txt) , [Mac](https://raw.githubusercontent.com/TM2320/Stack2images_ver2.0/master/download/Stack2images_ver2.0_Mac.txt)　（右クリックでリンク先を保存 or 左クリックで開いてコピペ）
> - 2.0170330
>	- 【機能追加】	ファイル名に使えない文字を除去する機能。
> - 2.0170325
> 	- 【機能削除】	サンプリングモード廃止。（中間産物から階調設定の成否は判断できないと判明したため。）
>	- 【仕様変更】
>		+ 拡張子判定に.tiffを追加。
>		+ ログ画面作成にif文を追加。
>		+ GitHubリポジトリ開設に伴い、本体からUpdate history欄を削除。
> - 2.0170322
>	- 【機能追加】
>		+ 開始宣言から終了宣言までの時間を計測し、ログに出力する。
>		+ サンプリングモード実装。12bitに階調設定した直後の画像を保存する機能。
>	+ 【仕様変更】	上書き処理を挟んでログ画面を編集ロックする。なぜこうなるのかは謎。
> - 2.0170321
>	+ 【機能追加】	ログをoutputにテキストとして出力。
>	+ 【機能削除】	outputフォルダ削除機能廃止。
>	- 【仕様変更】
>		+ ログをより詳細に。ユーザー設定も明示される。
>		+ 部分的なループ展開を実施。大して変わらない？
>		+ 怪しい英文を修正。
> - 2.0170316
>	- 【仕様変更】
>		+ continue文でよりスマートになった。
>		+ ディレクトリはログに残さずスキップする。
>		+ 終わり際にバッチモード解除。
>		+ ログとは別に終了メッセージ表示。
>		+ コメントと体裁の修正。
> - 2.0170314
>	+ 【機能追加】	Stack名の重複チェック。重複あれば命名のやり直しを促す。
> - 2.0170307
>	- 【仕様変更】
>		+ バッチモード有効化により処理速度が大幅にアップ。
>		+ ログにバージョンが表示される。
> - 2.0170301
>	- 【機能追加】
>		+ ダイアログによる対話的ユーザー設定が可能に。各自でソースを編集する必要がなくなった。
>		+ 複数色での保存に対応。代償としてメモリ使用量が大幅にアップ…
> - 2.0170226
>	+ 【機能追加】	何も出力されなかった場合、空のoutputフォルダを自動的に削除する。
>	- 【仕様変更】
>		+ 空フォルダは上書き回避の例外とする。
>		+ 同じ変数を使いまわしてメモリ使用量を削減（？）
>		+ 体裁を整理し可読性アップ。
> - 2.0170225
> 	- 【機能追加】  
>		+ 出力先フォルダが既に存在するか確認し、存在する場合はフォルダ名を変更する。  
>		+ ユーザー設定の整合性チェック。  
>		+ Tiffを読み込んだ直後にStack数の判定を実行。
>		+ 実行前にほかの画像を閉じる。
>	- 【仕様変更】
>		+ 色付け機構：Stackname[i]を参照し条件分岐 -> コマンドStackcolor[i]を実行。
>		+ 保存ファイル名に(色名)を付与。
>		+ ユーザー設定を1,2行目に集約し、簡便性アップ。
>		+ コメントの細かい修正とUpdate history欄の設置。
> - 2.0170223  
> 	+ 【機能追加】    拡張子判定機能追加。「.tif」でないファイルは無視する。  
> 	+ 【仕様変更】    すべてoutputに保存 -> Tiffごとに出力先フォルダを作成し、その中に保存。  
* 初出：2017/02/23  
