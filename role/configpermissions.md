name：配置角色权限

url：/role/configrolepermissions

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* role_id: 角色id
* config: 权限配置数组

ajax:

```
var config=[
	{"action_type_id":1,"action_type_check":1},
	{"action_type_id":2,"action_type_check":0},
	{"action_type_id":3,"action_type_check":1},
	{"action_type_id":4,"action_type_check":0},
	{"action_type_id":5,"action_type_check":1},
	{"action_type_id":6,"action_type_check":0},
	{"action_type_id":7,"action_type_check":1},
	{"action_type_id":8,"action_type_check":0},
	{"action_type_id":9,"action_type_check":1},
	{"action_type_id":10,"action_type_check":0},
	{"action_type_id":11,"action_type_check":1},
	{"action_type_id":12,"action_type_check":0},
	{"action_type_id":13,"action_type_check":1},
	{"action_type_id":14,"action_type_check":0},
	{"action_type_id":15,"action_type_check":1},
	{"action_type_id":16,"action_type_check":0},
	{"action_type_id":17,"action_type_check":1},
	{"action_type_id":18,"action_type_check":0},
	{"action_type_id":19,"action_type_check":1},
	{"action_type_id":20,"action_type_check":0}
];
var settings = {
  "url": "http://127.0.0.1:8081/role/configrolepermissions",
  "method": "POST",
  "data":{
    mobile: "13600000000",
    token: "1",
    role_id: 2,
    config: JSON.stringify(config)
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});

```

返回值：

正确：

* {"code":200,"data":{"status":"success","error":"success"}}

错误：

* {"code": 401, "data":{"status":"fail","error":"actionName is null"}} [参数空]actionName为空
* {"code": 401, "data":{"status":"fail","error":"actionUrl is null"}} [参数空]actionUrl为空
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询错误
* {"code": 402, "data":{"status":"fail","error":"action exist"}}[参数问题]操作已经存在
* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
