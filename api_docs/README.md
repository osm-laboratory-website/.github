# API仕様書

## 概要

### 認証・認可方式
OAuth2

## ユーザーAPI
||メソッド|URI|必要な権限|
|:---|:---|:---|:---|
|[ユーザー情報取得API(複数)](user/get_users.md)|GET|/api/users/|ログイン|
|[ユーザー情報取得API(user_id検索)]()|GET|/api/users/{user_id}|ログイン|
|[ユーザー情報登録API]()|POST|api/users/|ログイン|
|[ユーザー情報更新API]()|PUT|/api/users/{user_id}|ログイン|
|[ユーザー情報論理削除API]()|DELETE|/api/users/{user_id}|ログイン|