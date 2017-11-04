name：获取角色列表

url：/role/getrolelist

method：post

params：

* mobile: 手机号
* token: token
* page: 页数[默认为-1：获取全部设备]
* pageSize: 每页数量[默认20]


返回值：

正确：

{"code":200,"data":{"status":"success","error":"success","rows":[{"role_id":3,"role_name":"测试","addtime":"1509783682132"}],"total":2,"page":1,"pageSize":1}}

错误：

* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询出错
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
