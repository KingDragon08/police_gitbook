name：删除图层属性

url：/layer/delattr

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* extId: 图层id属性[必须]

> 删除图层属性会删除图层数据、图层相关字段，谨慎操作

返回值：

```
var settings = {
  "url": "http://127.0.0.1:8080/layer/delattr",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    extId:13,//图层自定义属性id
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```

正确：

* {"code":200,"data":{"status":"success","error":"success"}}

错误：

* {"code": 401, "data":{"status":"fail","error":"request param is invalid"}} [参数问题]请求参数为空或者不合法
* {"code": 404, "data":{"status":"fail","error":"layer not exist"}} [参数问题]请求图层不存在
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询错误
* {"code": 402, "data":{"status":"fail","error":"camera exist"}}[参数问题]设备已经存在
* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
