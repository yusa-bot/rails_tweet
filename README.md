# Tweet
Ruby on rails を使用して文章を呟けるSNSを実装しました。

## version
ruby : 3.2.7
Rails : 8.0.2

## エンドポイント | 機能
```bash
|    エンドポイント   |     画面名    |
| -------------- | ------------- |
| "/"            | TOP画面　　　　 |
| "/about"       | アプリ説明画面　|
| "/posts/index" | 投稿一覧画面　　|
| "/posts/:id"   | 投稿詳細画面　　|
| "/posts/new"   | 新規投稿画面　　|
```

## 実行
clone
```bash
git clone <URL> Tweet
```

migrationファイル(データベースへの変更を指示するファイル)をデータベースに反映。
```bash
rails db:migrate
```

サーバー起動
```bash
rails s(デフォルトポート番号)
rails s -p <ポート番号>(ポート番号指定)
```

## 主要ファイル構成
```bash
Tweet/
 ├── app/
     ├── models/
     └── controllers/ 
          └── application_controller.rb
          └── home_controller.rb
          └── posts_controller.rb   
     └── views/    
          ├── assets/ 
          └── layouts/
               └── application.html.erb
          └── home/
               └── about.html.erb
               └── top.html.erb
          └── posts/
               └── index.html.erb
               └── new.html.erb
               └── show.html.erb
 └── config/           
     └── routes.rb   
 ├──db/
 ├──public/    
 ├── test/              
 ├── log/                
 ├── tmp/               
 ├── .gitignore          
 ├── Dockerfile         
 ├── Gemfile            
 ├── Gemfile.lock        
 ├── Rakefile           
 ├── README.md           
 └── config.ru          
```
