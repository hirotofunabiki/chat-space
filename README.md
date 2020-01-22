# README

## users_table
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|username|string|null: false|
### Association
- has_many :group_users
- has_many :group :thorough :groups_users
- has_many :messages
## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### association
- belongs_to :group
- belongs_to :users

## groupe_table
|Column|Type|Options|
|------|----|-------|
|group_id|integer|null: false, foreign_key: true|

### association
- has_many :group_users
- has_many :group :thorough :groups_users
- has_many :messages


## message_table
|Column|Type|Options|
|------|----|-------|
|img|string|
|taxt|text|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### association
- belongs_to :group
- belongs_to :users



