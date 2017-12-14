name：增加摄像头类别

url：/camera/addCameraTypes

method：post

params：

* mobile: 手机号
* token: token
* name:类别名字,不允许重复
* url:图标路径 


ajax：

```
var settings = {
  "url": "http://127.0.0.1:8081/camera/addCameraTypes",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    name:"name",
    url:"url"
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
