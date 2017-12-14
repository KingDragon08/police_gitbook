name：获取图层类型列表

url：/layer/layertypelist

method：post

params：

* mobile: 手机号[必须]
* token: token[必须]
* page: 页码[默认为1，-1全部]
* pageSize: 每页大小

ajax：


返回值：

正确：

* ret = {"code": 200, "data": {"status": "success", "error": "success"，"rows": rows, "total": total, "page": page, "pageSize": pageSize}};

错误：

* {"code": 401, "data":{"status":"fail","error":"request param is invalid"}} [参数问题]请求参数为空或者不合法
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询错误
* {"code": 402, "data":{"status":"fail","error":"camera exist"}}[参数问题]设备已经存在
* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
