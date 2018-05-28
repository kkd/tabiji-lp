# tabiji-lp
Tabijiのランディングページです。

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


