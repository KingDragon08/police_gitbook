name：指定字段获取摄像头列表

url：/camera/pclistbyattr

method：post

params：

* mobile: 手机号[必须]
* token: token[必须]
* attrName: 字段名称[必须]
* attrValue: 字段取值[必须]
* page: 页数[默认为-1：获取全部设备]
* pageSize: 每页数量[默认20]


返回值：

正确：

{"code":200,"data":{"status":"success","error":"success","rows":[{"cam_id":1,"cam_no":"123","cam_name":null,"cam_sta":0,"addtime":"1505725590009","uptime":"1505821404366","user_id":7,"cam_loc_lan":"11.12","cam_loc_lon":"13.13","cam_desc":null,"is_del":0},{"cam_id":2,"cam_no":"1234","cam_name":null,"cam_sta":1,"addtime":"1505725687315","uptime":null,"user_id":7,"cam_loc_lan":"11.11","cam_loc_lon":"12.12","cam_desc":null,"is_del":0},{"cam_id":8,"cam_no":"12","cam_name":null,"cam_sta":0,"addtime":"1505747415564","uptime":"1505747415564","user_id":7,"cam_loc_lan":"11.11","cam_loc_lon":"12.12","cam_desc":null,"is_del":0}],"total":3,"page":1,"pageSize":20}}

错误：

* {"code": 401, "data":{"status":"fail","error":"attrName is invalid"}}[参数错误]attrName参数不合法
* {"code": 401, "data":{"status":"fail","error":"attrValue is null"}}[参数错误]attrValue参数为空
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询出错
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
