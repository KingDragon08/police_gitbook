name：获取权限类型列表

url：/role/getactiontypes

method：post

params：

* mobile: 手机号
* token: token

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/role/getactiontypes",
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

{"code":200,"data":{"status":"success","error":"success","rows":[{"id":1,"type_name":"摄像头"},{"id":2,"type_name":"车辆"}]}}

错误：

* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询出错
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
