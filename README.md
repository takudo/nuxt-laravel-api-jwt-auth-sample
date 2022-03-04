# ポイント

- ユーザー登録、ログインの流れは割愛
- ログイン後に、認証情報を使ってAPI を叩いている箇所
    - front: `jwt-frontend/pages/index.vue` のボタン部分。APIの呼び出し後に結果をconsole出力しているので、何が返ってきているのかわかる。
    - backend: `jwt-backend/app/Http/Controllers/AuthController.php` の `me` アクション。この中でログインユーザーの情報を取得している。
