name：获取角色列表

url：/role/getrolelist

method：post

params：

* mobile: 手机号
* token: token
* page: 页数[默认为-1：获取全部设备]
* pageSize: 每页数量[默认20]

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/role/getrolelist",
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

{"code":200,"data":{"status":"success","error":"success","rows":[{"role_id":3,"role_name":"超级管理员","addtime":"1509783682132"},{"role_id":4,"role_name":"角色2","addtime":"1509783695252"},{"role_id":5,"role_name":"角色3","addtime":"1509783695252"},{"role_id":6,"role_name":"角色4","addtime":"1509783695252"}],"total":4,"page":-1,"pageSize":4}}

错误：

* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询出错
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
