name：编辑图层属性

url：/layer/editattr

method：post

params：

* mobile: 手机号[必须]
* token: token[必须]
* extId: 图层属性id[必须]
* extName: 图层属性名称[必须]
* extDesc: 图层属性描述

ajax：


返回值：

正确：

* ret = {"code": 200, "data": {"status": "success", "error": "success"};

错误：

* {"code": 401, "data":{"status":"fail","error":"request param is invalid"}} [参数问题]请求参数为空或者不合法
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询错误
* {"code": 402, "data":{"status":"fail","error":"camera exist"}}[参数问题]设备已经存在
* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
