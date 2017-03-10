Syslogd (Patched)
===

[ ![Codeship Status for nowhere-cloud/syslogd](https://app.codeship.com/projects/aa6e4590-e816-0134-f3ac-061ac26d127f/status?branch=master)](https://app.codeship.com/projects/207336)

nodejs syslog server, including syslog message parser

Install
---

```sh
npm install syslogd
```

Usage
---

```js
var Syslogd = require('syslogd')
Syslogd(function(info) {
    /*
    info = {
          facility: 22
        , severity: 7
        , tag: 'tag'
        , time: Mon Dec 15 2014 10:58:44 GMT-0800 (PST)
        , hostname: 'hostname'
        , address: '127.0.0.1'
        , family: 'IPv4'
        , port: null
        , size: 39
        , msg: 'info'
    }
    */
}).listen(514, function(err) {
    console.log('start')
})
```

Check parser performance by `npm run performance`, which will run 500000 times


