name：添加图层数据属性

url：/layer/addlayerdata

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* layerId: 图层id[必须]
* locLan: 维度[必须]
* locLon: 经度[必须]
* extData: 额外属性[json格式，kv形式]

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/layer/addlayerdata",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    layerId:13,//图层类型id
    locLan:"locLan",//图层数据点维度
    locLon:"locLon",//图层数据点经度
    extData:"extData",//图层数据其他属性值
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```

返回值：

正确：

* ret = {"code": 200, "data": {"status": "success", "error": "success"}};

错误：

* {"code": 401, "data":{"status":"fail","error":"request param is invalid"}} [参数问题]请求参数为空或者不合法
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询错误
* {"code": 402, "data":{"status":"fail","error":"camera exist"}}[参数问题]设备已经存在
* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
