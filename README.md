# README

## users_table
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|name|string|null: false|
### Association
- has_many :group_users
- has_many :groups,thorough: :groups_users
- has_many :messages
## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### association
- belongs_to :group
- belongs_to :user

## groups_table
|Column|Type|Options|
|------|----|-------|
|name|integer|null: false, foreign_key: true|

### association
- has_many :group_users
- has_many :users, thorough: :group users
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
- belongs_to :user



