# pomelo-cocos-creator
pomelo client in cocos creator , author by @gjh1987 .

Original Project :
https://github.com/gjh1987/cccGame

## How to use
copy js file in your project , and you can get it in window.pomelo

Example :
``` js
let pomelo = window.pomelo;

let username = "test";
let rid = "1";

pomelo.init({
    host: "127.0.0.1",
    port: "3150",
    log: true
}, function() {
    var route = "connector.entryHandler.enter";
    pomelo.request(route, {
        username: username,
        rid: rid
    }, function(data) {
        if(data.error) {
            showError(DUPLICATE_ERROR);
            return;
        }
        cc.log("data: ", data);
    });
});
```
