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

{"code":200,"data":{"status":"success","error":"success","rows":[{"action_id":483,"action_name":"校验用户权限","addtime":"1511703369","action_url":"/user/checkUserPermission"},{"action_id":484,"action_name":"pc端删除手机用户","addtime":"1511703369","action_url":"/user/delMobileUser"},{"action_id":485,"action_name":"删除pc端用户","addtime":"1511703369","action_url":"/user/delPCUser"},{"action_id":486,"action_name":"获取app用户","addtime":"1511703369","action_url":"/user/getMobileUsers"},{"action_id":487,"action_name":"获取单个用户信息","addtime":"1511703369","action_url":"/user/getSingleUserInfo"},{"action_id":488,"action_name":"根据手机号获取用户信息","addtime":"1511703369","action_url":"/user/getSingleUserInfoByMobile"},{"action_id":489,"action_name":"获取pc端用户","addtime":"1511703369","action_url":"/user/getUsers"},{"action_id":490,"action_name":"根据关键字查找用户","addtime":"1511703369","action_url":"/user/getUsersByKeyword"},{"action_id":491,"action_name":"pc端用户登录","addtime":"1511703369","action_url":"/user/login"},{"action_id":492,"action_name":"pc端用户使用token登录","addtime":"1511703369","action_url":"/user/loginWithToken"},{"action_id":493,"action_name":"pc端用户退出登录","addtime":"1511703369","action_url":"/user/logout"}],"total":92,"page":-1,"pageSize":92}}

错误：

* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询出错
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
