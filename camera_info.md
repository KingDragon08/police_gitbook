name：获取单个摄像头信息

url：/camera/info

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* cam_id: 设备id[必须]


返回值：

正确：

{"code":200,"data":{"status":"success","error":"success","rows":[{"cam_id":1,"cam_no":"123","cam_name":null,"cam_sta":0,"addtime":"1505725590009","uptime":"1505821404366","user_id":7,"cam_loc_lan":"11.12","cam_loc_lon":"13.13","cam_desc":null,"is_del":0}],"cam_id":1}}

错误：

* {"code": 401, "data":{"status":"fail","error":"cam_id is null"}}[参数错误]cam_id为空
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询出错
* {"code": 404, "data":{"status":"fail","error":"camera not exist"}}[参数错误]设备不存在
* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
