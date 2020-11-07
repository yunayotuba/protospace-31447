# README

# ProtoSpaceのテーブル

## users テーブル
| Column   | Type   | Options     |
| -------- | ------ | ----------- |
| name     | string | null: false |
| email    | string | null: false |
| password | string | null: false |
| profile  | text   | null: false |
| occupation | text | null: false |
| position | text   | null: false |

### Association

- has_many :titles
- has_many :catch_copy
- has_many :concepts
- has_many :images
- has_many :texts
- has_many :users
- has_many :prototypes


## prototypes　テーブル
| Column     | Type   | Options     |
| --------   | ------ | ----------- |
| title      | string | null: false |
| catch_copy | text   | null: false |
| concept    | text   | null: false |
| user   | references | null: false |

### Association

- has_many :text
- belongs_to :user
- has_many :prototypes


## comments テーブル
| Column    | Type   | Options     |
| --------  | ------ | ----------- |
| text      | string | null: false |
| user      | references |         |
| prototype | references |         |

### Association

- belongs_to :user
- belongs_to :prototype