name：根据图层id获取属性列表

url：/layer/attrlistbyid

method：post

params：

* mobile: 手机号[必须]
* token: token[必须]
* layerId: 图层id[必须]

ajax：


返回值：

正确：

* ret = {"code": 200, "data": {"status": "success", "error": "success"，"rows": rows, "layerId": 1};

错误：

* {"code": 401, "data":{"status":"fail","error":"request param is invalid"}} [参数问题]请求参数为空或者不合法
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询错误
* {"code": 402, "data":{"status":"fail","error":"camera exist"}}[参数问题]设备已经存在
* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
