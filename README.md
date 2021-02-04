# README

# テーブル設計

## usersテーブル

| Column   | Type   | Options     |
| -------- | ------ | ----------- |
| name     | string | null: false |
| email    | string | null: false |
| password | string | null: false |

## association
- has_many :lists
- has_one :profile

## lists テーブル

| Column        | Type   | Options                        |
| ------------- | ------ | ------------------------------ |
| category_id   | integer| null: false                    |
| menu          | string | null: false                    |
| set_id        | integer| null: false                    |
| rep_id        | integer| null: false                    |
| user_id       | integer| null: false, foreign_key: true |

## association

- belongs_to :user

## profiles テーブル

| Column        | Type   | Options                       |
| ------------- | ------ | ------------------------------|
| sex_id        | integer| null: false                   |
| age           | integer| null: false                   |
| height        | integer| null: false                   |
| weight        | integer| null: false                   |
| user_id       | integer| null: false, foreign_key: true|

## association

- belongs_to :user