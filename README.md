# kaminari

## 参考サイト：導入
http://ruby-rails.hatenadiary.com/entry/20141113/1415874683

## 参考サイト：オプション
http://qiita.com/nysalor/items/77b9d6bc5baa41ea01f3

## 注意点
kaminari導入後にserver再起動しないと適用されない。

## 導入
1. モデルの作成
```
$ rails g scaffold Shop name zipcode address tel
```

2. seedの作成
```
# db/seeds.rb
```

3. マイグレーション
```
rake db:migrate
rake db:seed
```

4. kaminariのインストール
```
# Gemfile
gem 'kaminari'
```
```
$ bundle install
```

5. viewの修正
```
# app/views/shops/index.html.erb
```

6. controllerの修正
```
# app/controllers/shops_controller.rb
```

## Bootstrapの適用
1. bootstrapのインストール
```
# Gemfile
gem 'bootstrap-sass', '3.3.6'
gem 'kaminari-bootstrap', '~> 3.0.1'
```
```
$ bundle install
```

2. cssの設定
```
# app/assets/stylesheets/custom.scss
@import "bootstrap-sprockets";
@import "bootstrap";
```

## 日本語化時の注意点
http://kakakakakku.hatenablog.com/entry/2014/05/01/225207
```
# config/locales/ja.yml
ja:
  views:
    pagination:
      previous: "« 前ページ"
      next: "次ページ »"
      truncate: "..."
```
