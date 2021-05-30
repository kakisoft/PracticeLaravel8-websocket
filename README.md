# PracticeLaravel8-websocket
Laravel8 & websocket で遊ぶ用  

Laravel Framework 8.41.0


## 起動・終了
```
docker-compose up -d
docker-compose down
```

## コンテナに入る
```
docker-compose exec app bash

// NG
docker-compose exec app bash -c "cd my-laravel-app/"  
```


## 終了時にコンテナを削除
```
docker-compose down --rmi all
docker-compose down --rmi all --volumes
```


## 再起動
```
docker-compose restart
```

## コンフィグキャッシュをクリア
```
php artisan config:clear
```


php artisan websockets:serve

_______________________________________________________________________________
_______________________________________________________________________________
_______________________________________________________________________________
# プロジェクト作ったり、モデルを追加したり

## Create Project
```
composer create-project --prefer-dist  "laravel/laravel=8.*" my-laravel-app
```


## migrate
```
php artisan migrate
```

_______________________________________________________________________________________________________________________
_______________________________________________________________________________________________________________________
_______________________________________________________________________________________________________________________
```
root@8092d85e81c9:/var/www/html# composer create-project --prefer-dist laravel/laravel my-laravel-app "8.16.1"
Creating a "laravel/laravel" project at "./my-laravel-app"


  [InvalidArgumentException]
  Could not find package laravel/laravel with version 8.16.1.  
```
_______________________________________________________________________________________________________________________

```
composer create-project --prefer-dist laravel/laravel my-laravel-app "8.*"

composer create-project --prefer-dist  "laravel/laravel=8.*" my-laravel-app
```
