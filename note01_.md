# WebSocket
https://qiita.com/south37/items/6f92d4268fe676347160

Webにおいて双方向通信を低コストで行う為の仕組み。  

HTTP(厳密にはそれをwebsocketにupgradeしたもの)でクライアントとサーバー間で情報をやり取りしてコネクション確立  
確立されたコネクション上で、低コストな双方向通信  


______________________________________________________________________________________________________________
## LaravelでWebSocketを実装する方法
２種類存在する

 * Pusherという外部サービスを使う方法
 * socket.io + RedisのPUB/SUBで、WebSocketの部分をブリッジする方法

https://qiita.com/nishinoshake/items/1be777f1d5f4f36ebe09  

 
外部サービスを使う事を前提にするなら、Laravel 関係なくない？
と思ったが、「Laravel から簡単に Pusher を使う方法」が提供されているみたい。

⇒ 他にも、「Laravel Websockets」を使い方法があった。

https://beyondco.de/docs/laravel-websockets/getting-started/introduction

こっちの方が主流っぽい？

______________________________________________________________________________________________________________
# Pusher
https://pusher.com/

プッシャーは、簡単かつ安全にウェブやモバイルアプリ、または他の任意のインターネット接続デバイスにWebSocketを介して、リアルタイムの双方向機能を統合し、迅速にするためのシンプルなホストされているAPI  

WebSocketを使ってリアルタイムかつ両方向の通信機能をWebサイトやモバイルアプリに組み込むサービス  

　⇒　外部サービスとなるため、出来る限りこれを使わない方向を模索する

### Laravel Echo
LaravelとWebSocketを手軽に連携できるようにしてくれる、クライアントライブラリ。フロントのJavaScriptから使う。  
https://github.com/laravel/echo

### Laravel Echo Server
Node.js+Socket.io.のサーバー。Laravelの公式ではないが、ドキュメントに記載があるので、推されている模様。  
これ使えば、Node.js のコードは書かなくてもよい。
https://github.com/tlaverdure/laravel-echo-server

　⇒　ただし、node.js のインストールは必要

______________________________________________________________________________________________________________
# Predis
A flexible and feature-complete Redis client for PHP 7.2 and newer.
https://github.com/predis/predis


PHPのRedisクライアント  

どちらの方法を使うにしても、こちらは必須っぽい。  

______________________________________________________________________________________________________________
# predis/predis

## LaravelでWebSocketを使って、チャット機能を作る
https://qiita.com/NkawaK/items/5ba2cb1c2ef6fb03042d

______________________________________________________________________________________________________________
# predis +  laravel-echo

## LaravelでWebSocketを使って、チャット機能を作る
https://qiita.com/NkawaK/items/5ba2cb1c2ef6fb03042d  

composer require predis/predis
npm install --save laravel-echo


## マグロと寿司とWebSocket。Laravel+Vue.jsで簡易的なチャットを作る。
https://qiita.com/nishinoshake/items/1be777f1d5f4f36ebe09


______________________________________________________________________________________________________________
# laravel-websockets

## laravelで動くWebSocketsサーバ
https://qiita.com/zdjjs/items/5677358067994975abf6

pusher 不要。


## Laravel+Vueでリアルタイム・チャットをつくる（ダウンロード可）
https://blog.capilano-fw.com/?p=1418

　⇒ Pusher というサービスへのへの登録が必要

## Laravel WebSockets


______________________________________________________________________________________________________________
______________________________________________________________________________________________________________
______________________________________________________________________________________________________________
## Complete guide to achieving WebSocket real-time communication with Laravel Broadcast using Pusher, Laravel echo & Web socket 
https://dev.to/ankitmpatel/complete-guide-to-achieving-websocket-real-time-communication-with-laravel-broadcast-using-pusher-laravel-echo-web-socket-m29

ここでも必要とされる pusher





