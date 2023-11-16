---
title: "Zotero 日本語設定備忘録"
emoji: "🙌"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: [zotero]
published: true
---

# はじめに
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

# プラグインの追加
Zoteroを便利にするための様々なプラグインが公開されている
プラグインの一覧は[Zoteroの公式サイト](https://www.zotero.org/support/plugins)から確認可能
今回は次のプラグインを使用する

- [ZotFile](http://zotfile.com/)
	- ZoteroをOneDriveで管理するために必要
	- Google DriveやDrop Boxも利用可能(パスが通せればなんでもいい)
	- これがないとZotero公式リポジトリを使うことになる(容量に限界がある)

- [Better BibTeX](https://retorque.re/zotero-better-bibtex/)
	- TeXの参考文献

- [PDF Translate](https://github.com/windingwind/zotero-pdf-translate)
	- ZoteroのPDFリーダーに翻訳機能を追加する
	- ドラッグするだけで翻訳してくれるすごい機能(ただしバグあり)

プラグインはツール(T)\>アドオンでAdd-ons Managerを開き、歯車アイコンにあるInstall add-on From Fileでxpiファイルを開けばいい
# 設定
同期設定は最後にやるのが無難と思われる

## 表示設定
表示\>サブコレクションからアイテムを表示にチェックを入れる

![](/images/zotero/view.png)

## 一般
ここで使用するPDFリーダーを設定できる。今回はZotero内蔵リーダーを使用

![](/images/zotero/standard.png)


## PDF Translate
サイドパネルのTranslateタブを開きながらPDFを読む想定

![](/images/zotero/translate1.png)
![](/images/zotero/translate2.png)

User Interfaceは翻訳画面開きながら調整するとよい
バグで設定が反映されないことが多々ある

## Zotfile
ツール(T)\>Zotfile Preferencesから設定
Custom Locationは上のSource Folderと同じ場所

![](/images/zotero/zotfile.png)

Zotfile周りの設定は以下のサイトが参考になる
https://note.com/sdeso/n/n013952313c1b

タブレットやスマホからでもOneDriveアプリ経由で読める
Tablet settingをしっかりすればもっと読みやすくなるかもしれない


## 詳細\>ファイルとフォルダ
データ・ディレクトリはクラウドにすると深刻なエラーが起こるらしい

![](/images/zotero/folder.png)

## 同期

![](/images/zotero/sync.png)

# まとめ
上記の設定によって、OneDriveを通したファイルの同期、参考文献の作成、翻訳しながらの閲覧が可能になる
Zoteroは設定がめんどくさいが、いろんなことができるので、自分の環境に合わせてやっていくのがいいと思う
