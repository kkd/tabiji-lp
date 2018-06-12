# tabiji-lp
Tabijiのランディングページです。

# 公開手順

Github Pagesの設定で、ソースを"master branch /docs folder" を選択すると、docsフォルダ以下を公開するようになります。

以降は以下の手順で変更を反映します。

1. ファイルを変更する
2. ローカルで確認する
3. 変更ファイルおよびdocsフォルダをコミット＆プッシュする
4. Githu Pages上で確認する

# i18n対応概要

[jekyll-multiple-language-plugin](https://github.com/Anthony-Gaudino/jekyll-multiple-languages-plugin#51-translating-strings)を使っています

プラグインをインストールするにはGemfileがあるのを確認し下記を実行する。

```
bundle install
```

bundleがみつからない場合は下記を実行する。

```
gem install bundler
```

対応言語を_config.ymlのlanguagesに設定する（最初の言語がデフォルト言語となる）

_i18n配下に言語毎のymlファイルを作成しそこに設定する。
    - [YAML入門](http://magazine.rubyist.net/articles/0009/0009-YAML.html)

YAMLのバリデーションを実施する

```
$ rake yamllint
Running YamlLint...
Checking 2 files
Excluding 0 files
YamlLint found no errors
```

エラーがなければOK。


