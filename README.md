# ♰ 29hours ♰

Notification specified Twitter application that is running 29 hours everyday.

### ♰ Features ♰

The 29hours works with pluggable Matcher, Notifier, and Linker.

- Matchers
  - KeywordsMatcher
- Notifiers
  - BoxcarNotifier, ImkayacNotifier
- Linker
  - HttpLinker, TweetbotLinker

# ♰ How to use ♰

# Heroku に乗せる
## Heroku で動かすまでのおおまかな手順は以下の通りです。
$ git clone git://github.com/june29/29hours.git

$ cd 29hours/

$ cp settings.yml{.example,}

(settings.yml を適当に編集する)

$ gem update bundler
(Ruby2.0.0 のために bundler を更新する必要があるかも)

$ bundle exec ruby 29hours.rb
(動作を確認する)

$ heroku login

$ heroku create アプリ名

$ git push heroku master

$ heroku config:add SETTINGS_FILE_PATH=http://path/to/your/settings.yml
(Heroku のアプリの管理画面で worker の数を0から1にする)

from http://june29.jp/2013/03/08/29hours/ and modified by hokkai7go
