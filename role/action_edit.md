name：编辑操作

url：/role/editaction

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* actionName: 操作名称[必须, 且唯一]
* actionShortName: 操作简称[必须, 且唯一]

返回值：

正确：

{"code": 200, "data":{"status":"success","error":"success"}}

错误：

* {"code": 401, "data":{"status":"fail","error":"actionName is null"}} [参数空]actionName为空
* {"code": 401, "data":{"status":"fail","error":"actionShortName is null"}} [参数空]actionShortName为空
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询错误
* {"code": 402, "data":{"status":"fail","error":"action exist"}}[参数问题]操作已经存在
* {"code": 404, "data":{"status":"fail","error":"action not exist"}}[参数错误]操作不存在
* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
