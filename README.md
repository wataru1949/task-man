# task-man
<br><br>
## 概要
- タスク管理アプリです。<br>
- アカウント作成後、リストを作成し、リストごとにカードとしてタスクを管理することができます。<br>
- カードはタイトル、メモ、所属するリストをそれぞれ編集することができます。
<br><br><br>
## バージョン
- Ruby:2.6.3
- Ruby on Rails:5.2.3
<br><br><br>
## 本番環境
- URL: https://guarded-mesa-28035.herokuapp.com/<br>
- テストアカウント:
  - メールアドレス:toto@gmail.com<br>
  - パスワード:toto11
<br><br><br>
## 作成背景
- Ruby on Railsの復習とherokuへのデプロイを目的に、まずは簡単な機能を持ったコピーアプリを作りました。
<br><br><br>
## 使用技術
- 開発環境
  - VScode
  - HTML
  - scss
  - MySQL
  - Ruby on Rails
- 本番環境
  - heroku
  - PostgreSQL
<br><br><br>
## 今後追加する予定の機能
- 各ページのレイアウトをとデザインを整える
- カードのドラッグ＆ドロップ機能
- カードに登録できる内容を充実させる
<br><br><br>
## DB設計
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|email|string|null: false|
|encrypted_password|string|null: false|
### Association
has_many :lists
<br><br>
## listsテーブル
|Column|Type|Options|
|------|----|-------|
|title|string|null: false|
|user|references|foreign_key: true, null: false|
### Association
belongs_to :user
has_many :cards
<br><br>
## cardsテーブル
|Column|Type|Options|
|------|----|-------|
|title|string|null: false|
|memo|text|
|list|references|foreign_key: true, null: false|
### Association
belongs_to :lits


