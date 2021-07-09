# DB定義書
## ER図
[ER図はこちら]( https://github.com/Aso2001019/2021sys-design/blob/main/dai23.md )

# DBテーブルカラム詳細一覧

# データベース詳細

|和名|属性名|型|PK|NN|FK|
|---|------|--|--|--|--|
|オーダーID|order_id|bigint(20)|〇|〇|〇|
|顧客コード|customer_code|varchar(50)|-|〇|-|
|購入日|purchase_date|date|-|〇|-|
|総額|total_price|int(11)|-|〇|-|

購入テーブル詳細
|和名|属性名|型|PK|NN|FK|
|---|------|--|--|--|--|
||detail_id|bigint(20)|〇|〇|〇|
||order_id|bigint(20)|〇|〇|-|
||item_code|int(11)|-|〇|-|
||price|int(11)|-|〇|-|
||num|int(11)|-|〇|-|

ユーザー（顧客）テーブル 
|和名|属性名|型|PK|NN|FK|
|---|------|--|--|--|--|
||customer_code|varchar(50)|〇|〇|-|
||pass|varchar(50)|-|〇|-|
||name|varchar(20)|-|〇|-|
||address|varchar(100)|-|〇|-|
||tel|varchar(20)|-|〇|-|
||mail|varchar(100)|-|〇|-|
||del_flag|int(1)|-|-|-|
||reg_date|date|-|〇|-|

カテゴリテーブル
|和名|属性名|型|PK|NN|FK|
|---|------|--|--|--|--|
||category_id|int(11)|〇|〇|〇|
||name|varchar(20)|-|〇|-|
||reg_date|date|-|〇|-|

商品テーブル
|和名|属性名|型|PK|NN|FK|
|---|------|--|--|--|--|
||item_code|int(11)|-|〇|-|
||item_name|varchar(50)|-|〇|-|
||price|int(11)|-|〇|-|
||category_id|int(11)|〇|〇|〇|
||image|varchar(200)|-|〇|-|
||detail|varchar(500)|-|-|-|
||del_flag|int(11)|-|-|-|
||reg_date|date|-|〇|-|

