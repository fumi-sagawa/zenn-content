---
title: "Raycastのススメと使い方"
emoji: "🔍"
type: "tech"
topics:
  - "拡張"
  - "raycast"
published: true
published_at: "2022-03-21 15:39"
---

# はじめに
https://www.raycast.com/
なにやら最近人気らしく、自分も早速入れて使ってみました。
これが思ったより快適で既存の便利系ツールを置き換える形になりました。
  
ただ、調べたところ日本語による基本的な使い方の文献があまりない状況です。
せっかく良いツールなので皆さんにも使ってもらいたいなーと思い、使い方を書くことにしました。

# 概要
* Raycastとは：
  * 無料のランチャーツール
* Raycastの良さ：
  * **UI/UXが快適**
  * 機能がコンパクトにまとまっている 
  * 各機能にショートカットが割り当てられる
  * extensionsで機能の追加ができる
  * 設定がImport/Exportできる

# Raycastとは
ランチャーツールです。類似サービスはMac標準の[Spotlight](https://support.apple.com/ja-jp/guide/mac-help/mchlp1008/mac)や有名どころだと[Alfred](https://www.alfredapp.com/)があります。
ショートカットキーを押下してファイル検索など様々なコマンドが実行できるツールですね。

https://support.apple.com/ja-jp/guide/mac-help/mchlp1008/mac
https://www.alfredapp.com/

# Raycastの良さ
とにかく**体験が良い**です。
ランチャーとして使用する時はもちろんですが、ランチャーツールでもっとも睨めっこをする画面というとSettingsやPreferencesだと思います。ここのUIや操作感がとってもしっくり来ました。
マニュアルいらずに設定ができ、１時間足らずで移行が終わった時には「もうお前についてくぜ…！」といった感じでした。とりあえず使ってみて欲しい…！

![](https://storage.googleapis.com/zenn-user-upload/a9e4797a3acc-20220321.png)

また、よく使う機能がコンパクトにまとまっており必要に応じて[Store](https://www.raycast.com/store)から追加できます。
Google TranslateやTodist連携などが便利そうです。DeepL連携出ないかな

さらに「存在しない機能が欲しい」となった際にはReact/Typescriptで自前で用意可能です。
こちらは応用的なので本項では扱いませんが、素敵な記事がありますのでこちらをご覧ください。
https://zenn.dev/potsbo/articles/f7f235ca7c7577

一方で、RaycastにできることはほとんどAlfredでできたりします。
またAlfredのワークフローの方が高機能な側面もありますので一長一短の関係になりそう。
参考までにRaycastに移行された方、Alfredを使い続ける方２つの記事を貼っておきます。
https://motemen.hatenablog.com/entry/2022/02/raycast
https://blog.kyanny.me/entry/2021/12/22/221925

# インストール方法
こちらの`Download for Mac`からダウンロードできます。
https://www.raycast.com/

# 使い方
インストール時に使える機能を網羅していきます。
まず基本的な使い方を扱い、次にPreferencesを扱います。
## Hotkey：起動方法
デフォルトは`option + Space`。
`Preferences > General`から設定でき`Raycast Hotkey`をクリックすると任意で設定できます。

![](https://storage.googleapis.com/zenn-user-upload/b5feb30c2667-20220321.png)

## Search Bar：検索
起動するとコマンドを入力できます。
![](https://storage.googleapis.com/zenn-user-upload/e7738c59c5ae-20220321.png)
主にできることは以下です
* Applications(アプリの検索と起動)
* File Search（ファイルの検索）
* Snippets(スニペットの作成と利用)
* System(システム機能の利用)
* Clipboard History(クリップボード履歴)
* Quicklinks
* Floating Notes
* Window Management(ウィンドウ位置管理・画面分割）

アプリ・ファイル検索などは簡単に扱えるので、
以下特徴的なものを捕捉します。
:::message
これらの機能はPrefereces > Extensionsから一覧できます。
最初はわからないコマンドが多いのでExtensionsを辞書がわりに使うと良いです。
:::

### Snippets
- Create Snippet
- Search Snippet

で作成と利用が可能です。
特徴的な点として、Snippetは登録時に`Keyword`を登録することができます。
これは登録した文字列を入力すれば、Raycastを開くことなく即座にスニペットが展開される機能です。
![](https://storage.googleapis.com/zenn-user-upload/91cb88c427a4-20220612.png)

### System(システム機能の利用)
* `Sleep`
* `Lock Screen`
* `Toggle Mute`

などシステム関連の操作がコマンドで行えます。
特におすすめが`Quit All Application`でして、起動中のアプリを全て落とせて便利です。メモリ解放！

### Quciklinks
好きなwebページを立ち上げられるコマンドです。
`Create Quicklinks` で作成 → title名を`Search Bar`から利用できます。

![](https://storage.googleapis.com/zenn-user-upload/5fd464dfb55e-20220321.png)

特徴が**クエリを設定できる**点です。
インストール時にある`Search Google`を使ってみると
　![](https://storage.googleapis.com/zenn-user-upload/8168f887b849-20220321.png)
 
このようにクエリのプレースホルダが現れます。
ここに任意のテキストを入れてEnterすると、
このようにURLに文字列を反映しリンク先に遷移します。
`https://www.google.com/search?q=ちいかわ`
![](https://storage.googleapis.com/zenn-user-upload/6fc788d9d2fd-20220321.png)

設定方法は
* `Create Quicklinks`時の
* `Link`に
* `{Query(任意のプレースホルダ名)}`を設置

の手順です。

URLパラメータを設定する形とはなりますが、サービスによっては便利そう。
Yahoo!路線情報なんかは相性いいですね。
`https://transit.yahoo.co.jp/search/result?from=東京&to=御茶ノ水`

### Window Management(ウィンドウ位置管理・画面分割）
現在のウィンドウを「画面の左半分に寄せる」、「3分割した真ん中に設置する」など
画面分割が行えるコマンドです。全部で20個ほどあり大体のウィンドウ操作はできるでしょう。
![](https://storage.googleapis.com/zenn-user-upload/d3bc959ce947-20220321.png)

しかし、いちいちコマンド名を覚えるのも打つのすこし冗長です。
後述する`Preferences > Extensions`から**ショートカットを設定し利用する方法**がメインになるかもしれません。
私はこれまでMagnetというアプリを使っていたため、そちらのショートカットを適用しています。

* 左半分：option+ control + ←
* 右半分：option+ control + →

など


## Preferences：設定
設定に移りましょう。重要な`Extensions`と`Advanced`を紹介します。

### Extensions
![](https://storage.googleapis.com/zenn-user-upload/b389c48531e9-20220321.png)
プリインストール・追加した機能の一覧がわかる画面です。辞書がわりに使うと良いと思います。

また
* `Alias`(エイリアスの設定)
* `Hotkey`（ショートカットの設定)
* `Enabled`（有効化）

の設定が可能です。
`Alias`はもちろん`Hotkey`がアツいですよね〜
自分は主に`Snippets`や`Window Management`にショートカットを登録して使っています。
![](https://storage.googleapis.com/zenn-user-upload/f8510cacce4f-20220321.png)
`Quicklinks`でtwitterのショートカットを作ればツイ廃になれそうです。

`Enabled`カラムのチェックボックスによって使わない機能を検索から弾くこともできます。
検索結果の最適化ですね。

最後に、機能を選択すると右カラムにその機能の詳細設定が表示されます。
例えば`Snippets`であれば「クリップボードにコピーするか」「そのまま貼り付けるか」などが選択可能です。
痒い所に手が届くので覗いてみてください。
![](https://storage.googleapis.com/zenn-user-upload/2daa56a84707-20220321.png)

### Advanced
地味に大事な画面です。
![](https://storage.googleapis.com/zenn-user-upload/24d6c1244ab4-20220321.png)

* `Show Raycast on`
* `Auto-switch Input Source`
* `Import/Export`

の紹介をします。

`Show Raycast on`の設定からどこにRaycastを表示するかを選べます。
* Screen Containing Mouse(マウスがある画面)
* Screen with active Window（アクティブなウィンドウがある画面)
* Primary Screen(プライマリスクリーン)

の3択です。

`Auto-switch Input Source`では**Raycast起動時にデフォルトでONになる入力ソースを選べます**。
こちらの選択肢はOSで有効化されている入力ソースが自動で選択肢に現れるようです。
これ結構感動したポイントで、自分がランチャーツール使っていると

> 👨‍💻 「よし！VSCodeたちあげるぞ！」
> 👨‍💻  起動 → 入力 → 「vscおで」
> 👨‍💻 「うあああ〜！」

> 👨‍💻 「よし！Notionたちあげるぞ！」
> 👨‍💻  起動 → 入力 → 「のちおん」
> 👨‍💻 「うあああ〜！」

となることが稀によくあったんです。
それを`Auto-switch Input Source > ABC`などに設定すれば必ず英字入力が可能となります。
この設定を見つけた時、細かい配慮にとっても好きになりました。

`Import/Exoprt`はそのまま設定ファイルが入力/出力できます。
スニペットなども移行できるのがGood。
![](https://storage.googleapis.com/zenn-user-upload/e2d9e50a6e4f-20220321.png)


# おわりに
本記事ではよく使う&重要な機能をお伝えしました。
より詳細な使い方が知りたい方は公式のドキュメントをご覧ください。
https://raycastapp.notion.site/Raycast-Manual-d5c85a7694dc4e4088b8b93557ea6d2d

さらに拡張機能を自作したい方はこちらを
https://developers.raycast.com/

**無料・UXが良い・カスタマイズ性が高い**と、
とても使い勝手が良いランチャーツールですのでぜひ使ってみてください！

# 追記
最近RaycastProが発表されましたね！  
特にRaycastAIが便利ですが、こちらの記事がよくまとまっているためおすすめしておきます！
https://dev.classmethod.jp/articles/raycast_ai_beta_first_touch/