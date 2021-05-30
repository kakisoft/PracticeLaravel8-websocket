## 追加ポート
websocket には、6001ポートが必要。  
 ⇒ dokcer-compose.yml にて、複数ポートのポートフォワーディングの設定は可？（不可能であれば、もう１つセクションが必要）  


これを見る限り、可能っぽい。  
https://qiita.com/prgseek/items/e557a371d7bd1f57b9b1  


```yml
    ports:
      - "80:80"
      - "3000:3000"
```

ポートは生きてるっぽいが、うまく動いてない。  
http://localhost:8000/laravel-websockets

```
Channels current state is unavailable
```


