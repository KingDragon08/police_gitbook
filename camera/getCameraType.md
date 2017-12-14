name：获取摄像头类别

url：/camera/getCameraTypes

method：post

params：

* mobile: 手机号
* token: token


ajax：

```
var settings = {
  "url": "http://127.0.0.1:8081/camera/getCameraTypes",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b"
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```


返回值：

正确：

{"code":200,"data":{"status":"success","error":"success","rows":[{"id":1,"name":"球机","url":""},{"id":2,"name":"枪机","url":""},{"id":3,"name":"高清云台","url":""},{"id":4,"name":"固定枪机","url":""},{"id":5,"name":"云台","url":""},{"id":6,"name":"高清固定","url":""},{"id":7,"name":"固定","url":""},{"id":8,"name":"标清球机","url":""},{"id":9,"name":"标清云台枪机","url":""}]}}

错误：

* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询出错
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
