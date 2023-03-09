# 管理ボット0（QD）
### This is *QuestDragon Mk-2*, the next generation account of QuestDragon. 
### *～次世代のクエストドラゴンアカウント～*

## このドキュメントについて
本ドキュメントでは管理ボット0の使い方をまとめています。helpコマンドを搭載していない代わりとして作成しています。使用方法が分からなくなった際などにご活用ください。

<この記号でくくられた引数は任意引数です。入力しなくてもコマンドが動作します。「:」の後に書かれている内容は未入力時のデフォルト値です。>

［この記号でくくられた引数は必須引数です。未入力にするとエラーを返します。］

## プレフィックスについて
本ボットは未だにスラッシュコマンドが実装できていません。※早いところ実装したいんですけどね

そのため、実行はテキストコマンドとなります。接頭辞は「メンション」になります。

@を入力し、本ボットの名前を選択してください。メンションの後に自動で半角スペースが入ります。**追加でスペースを入れないでください。**コマンドが機能しません。

## ロール操作（一部サーバーでのみ有効）
### 参加者全員が管理者のため、逆に色々制限されてしまっているサーバー向けに、本ボットを使用してお好きなロールを管理者ロールと本ボットロールの下であればどの位置でも作成できるようにしました。以下に使い方を記述します。
#### ロールを作成して付与：
##### rolenew <ロール:新しいロール> <優先順位:1> <オンラインメンバーとは別にロールメンバーを表示する:True>
新しくロールを作成し、コマンド送信者に付与します。

ロール名はお好きな名前をどうぞ。優先順位は管理者ロール、本ボットロールから何番目かを指定します。

1と指定すると、本ボットのロールから1つ下に作成、という意味になります。

「オンラインメンバーとは別にロールメンバーを表示する」には`True`または`False`と入力して指定してください。

実行すると、ロールの色を聞かれますので、メッセージの候補にあるプリセットカラー、もしくは0xから始まる16進数で指定してください。

**色指定を間違えると実行がキャンセルされます**ので、間違えた場合はもう一度コマンドを実行し直してください。
#### 既存のロールを付与：
##### roleset ［ロールID］
既存のロールをコマンド送信者に付与します。
#### ロールを剥奪：
##### rolerem ［ロールID］
コマンド送信者に付与されているロールを剥奪します。
###### ※ロールIDは20桁からなる数字で構成されています。ロールIDを取得するには、ロールの名前の上で右クリックし、IDをコピーを選択するとコピーできます。
###### IDをコピーが表示されていない場合は、 Discordユーザー設定＞詳細設定＞開発者ツール をオンにすると表示されます。

## 音楽操作
### MEE6や本業のJockie Musicのほうが安定していますが、英語が嫌いな方は簡易的に本ボットでYouTubeからのコンテンツを音声で再生できます。よければご利用ください。
### なお、本ボットに搭載されている音楽再生機能は不安定であり、一部コンテンツは利用できない場合があります。音楽特化ボットもご用意しておりますので、頻繁にご利用になる場合は以下のボットの導入をご検討ください。なお、いずれも24時間稼働には現状対応しておりません。
[管理ボット1（ミュージック）](https://discord.com/api/oauth2/authorize?client_id=827701046964256769&permissions=275216844864&scope=applications.commands%20bot) 

[管理ボット2（音楽）](https://discord.com/api/oauth2/authorize?client_id=827742139093221377&permissions=274948418624&scope=applications.commands%20bot)
#### VC参加：
##### join
まずVCに参加させないと動作しないのでVCに参加させてください。
#### VC退出：
##### leave
実行しなくても誰もいなくなれば勝手に抜けてくれます。

もう必要ない場合は実行してください。
#### ダウンロード再生：
##### play*または*p ［URLまたはキーワード］
コンテンツをダウンロードしてから再生します。

多分…一度ダウンロードすれば安定して再生できる…んですかね？（デベロッパーなのにわかっていないという）

まあ…待ち時間がかかるので基本的には次項のQuickplayを使用することをおすすめします。
#### ストリーミング再生：
##### quickplay*または*qp ［URLまたはキーワード］
コンテンツをストリーミング再生します。

待ち時間が短く、公開されている音楽Botと同じようにすぐに再生が開始されます。

playと比べても音質が変わるとか、途切れにくいとか、違いが殆どないので基本的にはこちらを使用することをおすすめいたします。
###### キュー予約スロットが10個まで用意されています。次に再生したいコンテンツを10個まで指定できます。予約するには再生操作をしていただければ自動で予約されます。
#### スキップ：
##### skip*または*s
再生しているコンテンツをスキップします。
#### 一時停止：
##### pause*または*stop*または*st
再生を一時停止します。
#### 再開：
##### resume*または*r
一時停止していたコンテンツの再生を再開します。
#### 繰り返し：
##### repeat*または*loop*または*l
同じコンテンツの繰り返し再生機能を切り替えられます。
#### 予約全削除：
##### clear
キュー予約スロットに予約していたコンテンツを全て削除します。

## ゲーム操作
### 簡易的なカジノゲームや、占い、カウントゲーム、ロシアンゲームを用意しています。ご興味がございましたらぜひ。
#### 占い：
##### fortune
1日1回、占い師ステム（「占いシステム」とかけているだけですｗ）が占ってくれます。複数回実行できますが、結果は変わりません。

また、その日最初の1回だけラッキーカラーも表示します。（Embedメッセージの色がラッキーカラーです。もしかしたら2回目以降もラッキーカラーを表示できるようになるかも…）
### 【カジノ】カジノが楽しめる機能をご用意しています。カジノに使用されるデータは「アカウント名」をもとにして作成されます。つまり、**アカウント名を変更するとカジノのデータがリセットされます。**引き継ぎを行いたい場合はデベロッパーまでご相談ください。
#### 【カジノ】ブラックジャック：
##### bj ＜start＞
最大4人まで同時にブラックジャックが楽しめます。

ディーラーよりも手札を21に近づけるゲームです。ただし、21を超えてはいけません。

※本当のブラックジャックはもっと細かいルールがあるのですが、デベロッパーの技術とやる気の関係上、21に近づけるというルールのみでしか作成できませんでした。すみません…。

勝利で掛け金の2倍が返ってきます。

引き分けは掛け金が返ってきます。

負けると掛け金は返ってきません。

（小ネタ：掛け金はなくてもプレイできます。その場合は0と入力してください。）
#### 【カジノ】デイリーボーナス：
##### bj bonus
1日1回、デイリーボーナスを1,000チップ受け取れます。
#### 【カジノ】ヘルプ：
##### bj help
カジノに関するヘルプを表示します。
#### 【カジノ】残高照会：
##### chips*または*score*または*cash*または*coin
現在のチップ残高を確認できます。
#### 【カジノ】スロット：
##### slot <掛け金:10>
スロットで遊べます。Embedメッセージに表示される画像に当たりの組み合わせとペイアウト金額一覧が書かれています。

当たれば画像に表示された分の掛け金が戻ります。ハズレの場合、掛け金は戻りません。
#### 【カジノ】デベロッパーツール：
##### cdev
デベロッパー専用 - 保有チップの操作や、アカウントリセットの操作が行なえます。
#### カウントゲーム：
##### count
カウントゲームで遊べます。1からスタートし、誰かが空気をうまく読みながら1ずつカウントしてください。

正しくカウントできている場合はボットからグッドリアクションがつきます。

既にカウントしてある数字を送信してしまったり、次にカウントする数字を間違えると失敗です。

ちなみに、次にカウントする数字を間違えても、1回までは許してくれます。

既にカウントしてある数字を送信すると一発アウトです。
#### ロシアンゲームシリーズ：
##### russian ［ゲームID］ <掛け金:10>
ロシアンゲームシリーズをプレイできます。現在ロシアンルーレットとロシアンハイアンドローが収録されています。
###### ～ゲームIDについて～
1を指定するとロシアンルーレットをプレイできます。6発入る銃に1発だけ実弾が入っています。空撃ちで掛け金x2,x4,x8…、実弾発射で報酬0。

完全に運なので、自分の直感を信じて大金目指して頑張ってください。

2を指定するとロシアンハイアンドローをプレイできます。めくられていないカードの情報を参考に、以前のカードと比較対象のカードを比べ、比較対象のカードは以前のカードと比べて数字が高いか低いかを予想して当てるゲームです。当たると0.1xずつ報酬が上がります。

わからない場合はパスも可能です。パスすると正解を表示して次に進めます。ただし連続して使用はできません。パス後は必ずハイ、またはローを答える必要があります。

なお、どちらのゲームもVCに参加させてプレイするとSEを聞きながらプレイできます。
#### じゃんけんゲーム：
##### janken <掛け金:10>
ジャンケンで勝つと掛け金の2倍の報酬がもらえます。あいこで掛け金返却。負けると掛け金没収です。

Botと対戦する他、他プレイヤーさんとも勝負できます。

## ChatGPT操作
### OpenAIが開発するAIを使って会話ができます。暇つぶしなどにぜひ。
#### コマンド：
##### gpt <引数>
コマンド名は「gpt」です。

設定などは引数を入れて実行します。

###### 引数一覧:
**引数なし**→GPTのオンオフを切り替えます。チャンネル別、ユーザーごとに切り替えできます。

**!ch**→送信したチャンネルのGPT機能を全員分無効化します。チャンネル管理権限を持っていないユーザーが実行した場合は、そのチャンネルで有効化したユーザー全員からのコマンド実行による投票が必要です。

**!all**→全てのチャンネルのGPT機能を全員分無効化します。チャンネル管理権限を持っていないユーザーが実行した場合は、GPT機能を有効化したユーザー全員からのコマンド実行による投票が必要です。

**!status**→サーバーでGPTが有効化されているチャンネルと有効化したユーザーの一覧を表示します。

**!model**→AIのエンジンを選択できます。サーバー別、チャンネルごとに選択できます。（ユーザー別には選択できません）

**!temp** [値]→サーバーごとに文章の多様性を設定できます。（いつかチャンネル別にするかも）範囲は0.0から2.0、デフォルトでは1.0が設定されています。低くすると単調な文面が、高くすると多様性のある文面が返ってきます。

**!reset**→GPT3.5シリーズにおいて、対話履歴を削除して新しく会話を開始できます。

**その他文章など**→コマンド実行時だけGPT機能を使用できます。1回だけ使いたい時などにご使用ください。

## その他操作
### 上記のいずれにも分類されないコマンドです。
#### テストコマンド（プレフィックス含む）：
##### !qds test
テスト用コマンドです。基本的にはデベロッパー以外実行しないでください。
#### 顔文字コマンド（プレフィックス含む）：
##### !qds washi
コマンドが実行されたチャンネルに以下のメッセージを送信します。

(◜◡‾)

## 最後に
本ボットにはカジノ以外のヘルプコマンドがありません。ご不明な点はデベロッパーまでご相談ください。

なお、24時間稼働はしておりません。私のPCが起動している間のみ本ボットは利用可能です。

24時間稼働（ダウンタイムありの無料枠、ダウンタイムなしのWindows Server契約タイプ）をご希望の際はデベロッパーまでご相談ください。

なお、コストの掛からない24時間稼働の方法も鋭意模索中です。

[𝘘𝘶𝘦𝘴𝘵𝘋𝘳𝘢𝘨𝘰𝘯 𝘔𝘬-2#8472](https://discord.com/api/oauth2/authorize?client_id=900361708143542272&permissions=8&scope=applications.commands%20bot) をよろしくお願いいたします。
