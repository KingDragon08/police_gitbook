name：删除摄像头类别

url：/camera/delCameraTypes

method：post

params：

* mobile: 手机号
* token: token
* Id:类别Id


> 删除摄像头类别将会删除对应类别的摄像头数据，请谨慎操作

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8081/camera/delCameraTypes",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    Id:1
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```


返回值：

正确：

{"code":200,"data":{"status":"success","error":"success"}}

错误：

* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询出错
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
