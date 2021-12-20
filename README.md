# Narou.rb の対応サイトを追加する YAML ファイル置き場

## 概要

[Narou.rb](https://github.com/whiteleaf7/narou) の対応サイトは、「webnovel」フォルダ下の YAML ファイルにて追加が可能です。  
ここでは、私的に作成した webnovel ファイルを配布しています。

----

## 対応サイト
個人的に読みたい小説のあるサイトに、気が向いたら対応します。

- [ノベルバ](https://novelba.com/) https://novelba.com/

## 連絡先
配布ファイルに問題がある場合は、[Twitter/@ginlime](https://twitter.com/ginlime) までご連絡ください。  
なお、「個人的に読みたい小説のあるサイトに、気が向いたら対応」の方針のため、対応サイト追加の要望にはお応えできません。  
悪しからずご了承ください。

----

## webnovel ファイルを自分で作成してみたい人向けの、作成時の注意事項

- YAMLファイルを追加する場合は問題が起きてもファイルを削除すれば済みますが、既存のYAMLを編集するのはプログラミングに慣れた人でない場合はお勧めしません。

- 各項目の記載方法は既存のYAMLファイルを参考にすると良いでしょう。  
`kakuyomu.jp.yaml` を参考にするのがわかりやすくてお勧めです。

- 各項目の記載内容は、Rubyの正規表現と捉えてください。  
名前付きキャプチャが活用されています。

- 目次（subtitles）や本文（body_pattern）など、HTMLから取得する箇所の記述は、正規表現なのでDOMをセレクタで取得するようなものではありません。  
インデントも含めたベタなHTMLを正規表現で引っかける必要があります（`kakuyomu.jp.yaml` の `subtitles` を参照してください）。  
サイトによってはインデントをタブ文字で行っている場合もあり、これは '\s+' などでキャプチャできます。