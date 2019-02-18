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

