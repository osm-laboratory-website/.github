# ユーザー情報取得API(複数)

## 概要
ユーザー情報を複数取得する。

## エンドポイント
```
GET http://127.0.0.1:8000/api/users/
```

## パラメーター
なし

## レスポンス
複数のデータが配列として1つのレスポンスで返ってくる。
### レスポンスデータ
|名称|型|サイズ|必須|内容|
|:---|:---|:---|:---|:---|
|id|数値||◯|主キー|
|username|文字列||◯||ユーザー名|
|password|文字列||✗|パスワード|
|hashed_password|文字列||◯|ハッシュ化されたパスワード|
|created_at|年月日時分秒||◯|登録日時|
|updated_at|年月日時分秒||✗|更新日時|
|deleted_at|年月日時分秒||✗|削除日時|
### 例
```
[
  {
    "created_at": "2023-01-16T08:16:11.212615",
    "updated_at": null,
    "deleted_at": null,
    "id": 1,
    "username": "test1",
    "password": null,
    "hashed_password": "$5$rounds=535000$Au3PH41Q0dkeEPDo$tkBIaNOx7hAFPjdmemeIfEwFQiL38tfxlPueLQSm9B8"
  },
  {
    "created_at": "2023-01-16T08:16:11.216423",
    "updated_at": null,
    "deleted_at": null,
    "id": 2,
    "username": "test2",
    "password": null,
    "hashed_password": "$5$rounds=535000$Au3PH41Q0dkeEPDo$tkBIaNOx7hAFPjdmemeIfEwFQiL38tfxlPueLQSm9B8"
  }
]
```
### メッセージ
|ステータス|メッセージ内容|
|:---|:---|
|200||
|401|`Unauthorized`|
|500||