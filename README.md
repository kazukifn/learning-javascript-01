# learning-javascript-01

テクノロジー（藤原）JavaScriptの練習 (1)

## Q1の回答「コメントを解除したことで、どう変化しましたか？」

ポップアップが出てきた　コンソールで「おはよう」が表示された

## Q2の回答「エラーの原因は何でしょうか？（調べてみましょう）」

Windowが定義されていない
Node.jsはサーバーサイドでありクライアントサイドでないためNode.jsの中の"window.alert("Hello!");"というブラウザで動くコードが原因であると考えられる。
## Chromeデベロッパーツール：Consoleの実行結果

```
おはよう！
index.html:56 Live reload enabled.
index.html:18 おはよう！
Navigated to http://127.0.0.1:5500/index.html
index.html:52 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
socket.onmessage @ index.html:52
Navigated to http://127.0.0.1:5500/index.html
index.html:18 おはよう！
index.html:1 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
Navigated to http://127.0.0.1:5500/index.html
index.html:18 おはよう！
index.html:52 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
socket.onmessage @ index.html:52
Navigated to http://127.0.0.1:5500/index.html
VM29 main.js:4 Good morning.
index.html:18 おはよう！
index.html:1 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
Navigated to http://127.0.0.1:5500/index.html
VM33 main.js:4 Good morning.
index.html:18 おはよう！
index.html:1 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
Navigated to http://127.0.0.1:5500/index.html
VM37 main.js:4 Good morning.
index.html:18 おはよう！
const prefList = ["北海道", "青森"];
undefined
prefList
(2) ["北海道", "青森"]
prefList[0,1]
"青森"
prefList[ 0]
"北海道"
document.body
<body>​<h1>​テクノロジー（藤原）JavaScript練習用ページ​</h1>​<!-- 外部ファイルのJavaScript（js/main.js）を読み込む --><script src=​"js/​main.js">​</script>​<!-- JavaScriptをHTMLに直接書く --><script>​…​</script>​<!-- 以下は触らない（タブを閉じるときに警告を出すためのコード） --><script>​…​</script>​<!-- Code injected by live-server --><script type=​"text/​javascript">​…​</script>​</body>​
window.outerWidth
110
console.log
ƒ log() { [native code] }
Navigated to http://127.0.0.1:5500/index.html
main.js:4 Good morning.
index.html:18 おはよう！
```

## ターミナルの実行結果

```
oonishiikkinoMacBook-Pro:learning-javascript-01 kazuki$ node node-main.js
-bash: node: command not found
oonishiikkinoMacBook-Pro:learning-javascript-01 kazuki$ node node-main.js
-bash: node: command not found
oonishiikkinoMacBook-Pro:learning-javascript-01 kazuki$ node node-main.js
-bash: node: command not found
oonishiikkinoMacBook-Pro:learning-javascript-01 kazuki$ echo "export PATH=$HOME/.nodebrew/current/bin:$PATH" >> ~/.bashrc
oonishiikkinoMacBook-Pro:learning-javascript-01 kazuki$ source ~/.bashrc
oonishiikkinoMacBook-Pro:learning-javascript-01 kazuki$ node node-main.js
/Users/kazuki/Documents/fujiwara/learning-javascript-01/node-main.js:1
window.alert("Hello, Node.js!!");
^

ReferenceError: window is not defined
    at Object.<anonymous> (/Users/kazuki/Documents/fujiwara/learning-javascript-01/node-main.js:1:1)
    at Module._compile (internal/modules/cjs/loader.js:774:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:785:10)
    at Module.load (internal/modules/cjs/loader.js:641:32)
    at Function.Module._load (internal/modules/cjs/loader.js:556:12)
    at Function.Module.runMain (internal/modules/cjs/loader.js:837:10)
    at internal/main/run_main_module.js:17:11
oonishiikkinoMacBook-Pro:learning-javascript-01 kazuki$ node node-main.js
Goodmorning, Node.js!!

```

