name：根据图层id获取图层数据列表

url：/layer/layerdatalistbyid

method：post

params：

* mobile: 手机号[必须]
* token: token[必须]
* layerId: 图层id[必须]
* page: 页码[默认为1，-1全部]
* pageSize: 每页大小

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/layer/layerdatalistbyid",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    layerId:13,//图层id
    page:1,//页码
    pageSize:10,//每页大小
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```

返回值：

正确：

* ret = {"code": 200, "data": {"status": "success", "error": "success"，"rows": rows, "layerId": 1};

错误：

* {"code": 401, "data":{"status":"fail","error":"request param is invalid"}} [参数问题]请求参数为空或者不合法
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询错误
* {"code": 402, "data":{"status":"fail","error":"camera exist"}}[参数问题]设备已经存在
* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
