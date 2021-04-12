
##users テーブル
has_many :customer
has_many :record

| Column              | Type    | Option     |
| ------------------- | ------- | ---------- |
| nickname            | string  | null:false |
| encrypted_password  | string  | null:false |

##customer
belongs_to :user
has_one :record

| Column        | Type       | Option           |
| ------------- | ---------- | ---------------- |
| user          | references | foreign_key:true |
| costomername  | string     | null:false       |
| god_id        | integer    | null:false       |
| fate_id       | integer    | null:false       |

##record
belongs_to :customer

| Column  | Type    | Option     |
| ------- | ------- | ---------- |
| date    | string  | null:false |
| text    | string  | null:false |