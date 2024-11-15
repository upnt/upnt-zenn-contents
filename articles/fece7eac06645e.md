---
title: "Zoteroによる英語論文管理・閲覧"
emoji: "🙌"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: [zotero]
published: true
---

:::message alert
Zotfileは現在ほとんど更新されておらず、最新のZotero 7に対応する可能性はかなり低いです。
そのため、Zotfileは使用しないことをおすすめします。
設定 > 詳細 > 基本ディレクトリを`G:/マイドライブ/Zotero`のように他のストレージサービスに設定することで、ZotfileのようにZotero Storageの節約ができます
:::

## はじめに

Zoteroを使って英語論文などを管理、閲覧するための設定方法を紹介する

- 参考文献の管理めんどくさい
- 英語論文を読むのに翻訳めんどくさい
- 出先や研究室、家でも論文を手早く読みたい

こんなことを思ったことのある方々にはとても便利な設定になるはず。。。
Windows上でしか動作確認していないため注意してほしい

本記事で設定可能な機能は以下のとおり

- 外国語論文を高速に翻訳しながら読む
- 複数PC、タブレット、スマホ上で文書を閲覧
- TeXの参考文献の作成

ほかにも、便利な機能、プラグイン、周辺アプリを見つけたら記事の内容を更新する

特にPDFリーダーはもっといいのがありそう

よかったらコメントください

## プラグインの追加

Zoteroを便利にするための様々なプラグインが公開されている
プラグインの一覧は[Zoteroの公式サイト](https://www.zotero.org/support/plugins)から確認可能
今回は次のプラグインを使用する

- ~~[ZotFile](http://zotfile.com/)~~

  - ~~ZoteroをOneDriveで管理するために必要~~
    - 設定 > 詳細 > 基本ディレクトリを`G:/マイドライブ/Zotero`のように設定して代用可能
  - Google DriveやDrop Boxも利用可能(パスが通せればなんでもいい)
  - これがないとZotero公式リポジトリ(Zotero Storage)を使うことになる(容量に限界がある)

- [Better BibTeX](https://retorque.re/zotero-better-bibtex/)

  - TeXの参考文献
  - Zotero 7上でも動作

- [PDF Translate](https://github.com/windingwind/zotero-pdf-translate)

  - ZoteroのPDFリーダーに翻訳機能を追加する
  - ドラッグするだけで翻訳してくれるすごい機能
  - 最新のRelease v2.0.5はZotero 7で動かせる

プラグインはツール(T)\>アドオンでAdd-ons Managerを開き、歯車アイコンにあるInstall add-on From Fileでxpiファイルを開くとインストールできる。

## 設定

同期設定は最後にやるのが無難と思われる

### 表示設定

表示\>サブコレクションからアイテムを表示にチェックを入れる

![表示設定](/images/zotero/view.png)

### 一般

ここで使用するPDFリーダーを設定できる。今回はZotero内蔵リーダーを使用

![一般](/images/zotero/standard.png)

Zotero 7になってFile Renamingというのが追加された。これを使えばZotFileでよく使われてたファイル名変更をできるかも?(要検証)

### PDF Translate

サイドパネルのTranslateタブを開きながらPDFを読む想定

![Translate1](/images/zotero/translate1.png)
![Translate2](/images/zotero/translate2.png)

User Interfaceは、主にTranslateタブに表示する項目の設定である。翻訳画面を開きながら調整するとよい
バグで設定が反映されないことがある

### ~~Zotfile~~

ツール(T)\>Zotfile Preferencesから設定

Custom Locationは上のSource Folderと同じ場所

General settingは以下の通り
![Zotfile](/images/zotero/zotfile.png)

subfolderを設定すると、保存するファイルをルールに従って分類してくれる。例えば、私は"/%c"に設定しているが、これをするとコレクションでファイルを分類してくれるため、OneDrive上でもファイルを見つけやすくなる

Zotfile周りの設定は以下のサイトが参考になる
<https://note.com/sdeso/n/n013952313c1b>

iPadでは、PDF Expartが便利

PDF ExpartなどのPDF ReaderでOneDriveのファイルを開けばよい

ファイル名が分かりやすいようにRenaming Rulesも変更する

![Renaming Rules](/images/zotero/rename.png)

### 詳細\>ファイルとフォルダ (ZotFileの代用)

データ・ディレクトリはクラウドにすると深刻なエラーが起こるらしい

![ファイルとフォルダ](/images/zotero/folder.png)

ここの基本ディレクトリを設定することでPDFファイルを指定したディレクトリに保存できる(はず...)
例えばGoogleDriveに保存する場合は`G:\マイドライブ\Zotero`とかにすればよい

### 同期

![同期](/images/zotero/sync.png)

## まとめ

上記の設定によって、OneDriveを通したファイルの同期、参考文献の作成、翻訳しながらの閲覧が可能になる
Zoteroは設定がめんどくさいが、いろんなことができるので、自分の環境に合わせてやっていくのがいいと思う
