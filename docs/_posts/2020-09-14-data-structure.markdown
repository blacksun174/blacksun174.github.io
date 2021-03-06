---
layout: post
title:  "プログラミングするときのデータ構造について"
date:   2020-09-14 09:36:00 +0900
categories: datastructure
---
プログラミングをする時にデータ構造を意識することが全くありませんでした。実装したい機能、処理ができれば、１つのグループのデータがバラバラにあっても問題がないと思っていました。
しかし、これはコードがわかりにくくなるのと、処理を追いにくくする要員です。
例えば、pandasのdataframeのカラムを新しい順番と名前にマッピングする時に、次のデータがあります。
```
- 前後のカラムマップ： from_: 'userId', to_: 'user_id'
- データ型： 'integer'
- ハッシュするカラム名：　['user_id', 'user_name']
```
上のデータを３つの変数に入れていましたが、実はこれは１つのデータにすることができます。
```json
[
    { "from_": "userId", "to_": "user_id", "data_type": "integer", "is_masked": false },
    { "from_": "userName", "to_": "user_name", "data_type": "integer", "is_masked": true }
]
```
このようにデータ構造についても勉強したいと思ったきっかけです。
データ構造がすっきりすると、コードもすっきりしてくると思います。
（プログラムはデータと処理だけでできているからですかね）
(2020/09/14)
