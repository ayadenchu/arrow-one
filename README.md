# テーブル設計

## users テーブル
| Column     | Type   | Options     |
| ---------- | ------ | ----------- |
| nickname   | string | null: false |
| family_name| string | null: false |
| fast_name  | string | null: false |
| email      | string | null: false           |
| family_name_kana | string | null: false     |
| first_name_kana  | string | null: false     |
| encrypted_password | string | null: false |

### Association
- has_many :
## mentor テーブル
| Column    | Type       | Options           |
| --------- | ---------- | ----------------- |
| name      | string     | null: false                |
| description | text | null: false                    |
| category_id | integer | null: false                 |
| user | references  | null: false, foreign_key: true |

### Association
- belongs_to :user

## message テーブル
| Column    | Type       | Options                        |
| --------- | ---------- | ------------------------------ |
| text   | text | null:false      |
| user   | references | null: false, foreign_key: true |
### Association
- belongs_to :user