# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|nickname|string|null: false|
### Association
- has_many :posts
- has_many :carenders

## postsテーブル
|Column|Type|Options|
|------|----|-------|
|title|text|null: false|
|content|text|null: false|
|user_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :user

## carenderテーブル
|Column|Type|Options|
|------|----|-------|
|date|text|null: false|
|user_id|integer|null: false, foreign_key: true|
|event_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :user
- has_many: events

## eventテーブル
|Column|Type|Options|
|------|----|-------|
|title|integer|null: false, foreign_key: true|
|start|text|null: false|
|end|text|null: false|
### Association
- belongs_to : carendar


