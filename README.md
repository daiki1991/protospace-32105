# テーブル設計

## users テーブル

| Column   | Type   | Options     |
| -------- | ------ | ----------- |
| email    | string | null: false |
| password | string | null: false |
| name     | string | null: false |
| profile  | text   | null: false |
|occupation| text   | null: false |
| position | text   | null: false | 

## room_users テーブル

| Column  | Type       | Options                        |
| ------  | ---------- | ------------------------------ |
| text    | text       | null: false                    |
| user    | references |                                |
|prototype| references |                                |

## prototypes テーブル

| Column    | Type       | Options      |
| -------   | ---------- | ------------ |
| title     | string     |              |
| catch_copy| text       | null: false  |
| concept   | text       | null: false  |
| image     |            | ActiveStorage|
| user      | references | null: false  | 