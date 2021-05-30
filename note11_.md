参考動画　　
https://www.youtube.com/watch?v=pIGy7-7gGXI

## Laravel Websockets
https://beyondco.de/docs/laravel-websockets/getting-started/installation



```

composer require beyondcode/laravel-websockets


php artisan vendor:publish --provider="BeyondCode\LaravelWebSockets\WebSocketsServiceProvider" --tag="migrations"



php artisan vendor:publish --provider="BeyondCode\LaravelWebSockets\WebSocketsServiceProvider" --tag="config"


```   


## .env : BROADCAST_DRIVER を修正
```
BROADCAST_DRIVER=log
CACHE_DRIVER=file
QUEUE_CONNECTION=sync
SESSION_DRIVER=file
SESSION_LIFETIME=120
```
　　↓
```
BROADCAST_DRIVER=pusher
CACHE_DRIVER=file
QUEUE_CONNECTION=sync
SESSION_DRIVER=file
SESSION_LIFETIME=120
```

## .env : PUSHER を修正
```
PUSHER_APP_ID=
PUSHER_APP_KEY=
PUSHER_APP_SECRET=
PUSHER_APP_CLUSTER=mt1
```
　　↓
```
PUSHER_APP_ID=12345
PUSHER_APP_KEY=ABCDEFG
PUSHER_APP_SECRET=HIKLMN
PUSHER_APP_CLUSTER=mt1
```

KEY は最大 60文字程度

PHP側で pusher を設定する時は、アプリまたはアプリキーを使用する

クライアント・サーバで、key と secret を


## my-laravel-app\config\websockets.php
ファイルが存在している事を確認
```
```

## ブラウザにて確認可
http://localhost:8000/laravel-websockets


laravel-websockets


## コマンド実行
composer require pusher/pusher-php-server "~3.0"



## my-laravel-app\config\broadcasting.php
```php
    'default' => env('BROADCAST_DRIVER', 'null'),
```


```php
        'pusher' => [
            'driver' => 'pusher',
            'key' => env('PUSHER_APP_KEY'),
            'secret' => env('PUSHER_APP_SECRET'),
            'app_id' => env('PUSHER_APP_ID'),
            'options' => [
                'cluster' => env('PUSHER_APP_CLUSTER'),
                'useTLS' => true,
            ],
        ],
```
　　↓
```php
        'pusher' => [
            'driver' => 'pusher',
            'key' => env('PUSHER_APP_KEY'),
            'secret' => env('PUSHER_APP_SECRET'),
            'app_id' => env('PUSHER_APP_ID'),
            'options' => [
                'cluster' => env('PUSHER_APP_CLUSTER'),
                'useTLS' => true,
                'host' => '127.0.0.1',
                'port' => 6001,
                'scheme' => 'http',
            ],
        ],
```




```
Channels current state is unavailable
```


##
php artisan make:event NewMessage

