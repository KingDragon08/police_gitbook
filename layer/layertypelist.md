name：获取图层类型列表

url：/layer/layertypelist

method：post

params：

* mobile: 手机号[必须]
* token: token[必须]
* page: 页码[默认为1，-1全部]
* pageSize: 每页大小

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/layer/layertypelist",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
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

{"code":200,"data":{"status":"success","error":"success","rows":[{"type_id":5,"type_name":"光纤","user_id":53,"addtime":"1514884972751","img_path":null},{"type_id":4,"type_name":"重点人员","user_id":53,"addtime":"1514884972751","img_path":null},{"type_id":3,"type_name":"管道","user_id":53,"addtime":"1514884972751","img_path":null},{"type_id":2,"type_name":"车辆","user_id":53,"addtime":"1514884972751","img_path":null},{"type_id":1,"type_name":"摄像头","user_id":53,"addtime":"1514884972751","img_path":"http://211.103.178.205:8081/upload/1513100508342.jpg"}],"total":5,"page":1,"pageSize":20}}

错误：

* {"code": 401, "data":{"status":"fail","error":"request param is invalid"}} [参数问题]请求参数为空或者不合法
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询错误
* {"code": 402, "data":{"status":"fail","error":"camera exist"}}[参数问题]设备已经存在
* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
