name：模糊查找地点

url：/address/fuzzysearch

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* info: 查找输入信息[必须]
* size: 获取地点数量[默认20]

返回值：

正确：

* {"code":200,"data":{"status":"success","error":"success","rows":[{"cam_id":2,"cam_no":"1234","cam_name":"cam_name","cam_sta":1,"addtime":"1505725687315","uptime":null,"user_id":7,"cam_loc_lan":"11.11","cam_loc_lon":"12.12","cam_desc":null,"is_del":0,"cam_addr":"test.addr"},{"cam_id":8,"cam_no":"12","cam_name":"cam_name","cam_sta":0,"addtime":"1505747415564","uptime":"1505747415564","user_id":7,"cam_loc_lan":"11.11","cam_loc_lon":"12.12","cam_desc":null,"is_del":0,"cam_addr":"test.addr"}],"total":2}}

错误：

* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询错误
* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
