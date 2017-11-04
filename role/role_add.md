name：添加角色

url：/role/addrole

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* roleName: 角色名称[必须, 且唯一]

返回值：

正确：

* {"code":200,"data":{"status":"success","error":"success","role_id":2}}

错误：

* {"code": 401, "data":{"status":"fail","error":"roleName is null"}} [参数空]roleName为空
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询错误
* {"code": 402, "data":{"status":"fail","error":"role exist"}}[参数问题]角色已经存在
* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
