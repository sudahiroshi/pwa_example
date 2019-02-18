# PWA Example

Progressive Web Applicationの雛形を試してみた．

cloneして以下のコマンドを打つとサーバが起動する．

```
ruby -rwebrick -rwebrick/https -e 'WEBrick::HTTPServer.new(:DocumentRoot => "./", :Port => 8000, :SSLEnable => true, :SSLCertName => [["CN", WEBrick::Utils::getservername]] ).start'
```

後はPWAに対応しているWebブラウザで閲覧し，ホームに追加して楽しむ．
ただし，証明書が信用できないとか出て来るので，強引に信頼させるしか無い．

#### 注意事項

manifest.jsonにIPアドレスが直接書かれているので，編集が必要．

## Reference

[PWA入門！JavaScriptで簡単に高速化＆オフライン対応のWebサイト制作チュートリアル！ / paiza開発日誌](https://paiza.hatenablog.com/entry/2018/08/29/PWA%E5%85%A5%E9%96%80%EF%BC%81JavaScript%E3%81%A7%E7%B0%A1%E5%8D%98%E3%81%AB%E9%AB%98%E9%80%9F%E5%8C%96%EF%BC%86%E3%82%AA%E3%83%95%E3%83%A9%E3%82%A4%E3%83%B3%E5%AF%BE%E5%BF%9C%E3%81%AEWeb%E3%82%B5)

[PWA 入門 〜iOS SafariでPWAを体験するまで〜 2018年6月版 / Qiita](https://qiita.com/umamichi/items/0e2b4b1c578e7335ba20)

[ウェブアプリマニフェスト / MDN web docs](https://developer.mozilla.org/ja/docs/Web/Manifest)
