# 📮 Promise based, message oriented API for _primarily_ JSON over HTTP/HTTPS

```js
const request = require("@tessin/request");

const res = await request({ url: "..." }); // GET ...

console.log(res.statusCode); // number
console.log(res.statusMessage); // string
console.log(res.headers); // {[key: string]: string}

// if "Content-Type" is "application/json" then
// content equals JSON.parse(content)
// otherwise typeof content is "string"
const content = res.content;

console.log(typeof content, content);
```
