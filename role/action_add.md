name：添加操作

url：/role/addaction

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* actionName: 操作名称[必须, 且唯一]
* actionUrl: 操作对应url[必须, 且唯一]

返回值：

正确：

* {"code":200,"data":{"status":"success","error":"success","action_id":2}}

错误：

* {"code": 401, "data":{"status":"fail","error":"actionName is null"}} [参数空]actionName为空
* {"code": 401, "data":{"status":"fail","error":"actionUrl is null"}} [参数空]actionUrl为空
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询错误
* {"code": 402, "data":{"status":"fail","error":"action exist"}}[参数问题]操作已经存在
* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
