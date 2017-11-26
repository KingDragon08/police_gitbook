name：获取角色操作列表

url：/role/getroleactionlist

method：post

params：

* mobile: 手机号
* token: token
* role_id: 3//角色的role_id
* page: 页数[默认为-1：获取全部设备]
* pageSize: 每页数量[默认20]

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/role/getroleactionlist",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    role_id:3
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```


返回值：

正确：

{"code":200,"data":{"status":"success","error":"success","rows":[{"id":163,"role_id":3,"action_id":436,"addtime":"1511703369","action_name":"编辑一级部门"},{"id":164,"role_id":3,"action_id":437,"addtime":"1511703369","action_name":"编辑二级部门"},{"id":165,"role_id":3,"action_id":438,"addtime":"1511703369","action_name":"获取一级部门列表"},{"id":166,"role_id":3,"action_id":439,"addtime":"1511703369","action_name":"获取二级部门列表"},{"id":167,"role_id":3,"action_id":440,"addtime":"1511703369","action_name":"更改用户部门"},{"id":168,"role_id":3,"action_id":441,"addtime":"1511703369","action_name":"多文件上传"},{"id":169,"role_id":3,"action_id":442,"addtime":"1511703369","action_name":"单文件上传"},{"id":170,"role_id":3,"action_id":443,"addtime":"1511703369","action_name":"pc单文件上传"}],"total":92,"page":-1,"pageSize":92}}

错误：

* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询出错
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
