name：添加摄像头

url：/camera/add

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* cam_no: 设备编号[必须, 且唯一]
* cam_name: 设备名称
* cam_desc: 设备描述
* cam_loc_lon: 设备地点经度[必须]
* cam_loc_lan: 设备地点维度[必须]
* cam_sta: 设备状态(取值0/1/2/3, 默认0; 0: 不激活, 1: 激活, 2: 故障, 3:失效)

返回值：

正确：

* {"code":200,"data":{"status":"success","error":"success","cam_id":2}}

错误：

* {"code": 401, "data":{"status":"fail","error":"camera no is null"}} [参数空]cam_no为空
* {"code": 401, "data":{"status":"fail","error":"cam_loc_lon is null"}}[参数空]cam_loc_lon为空
* {"code": 401, "data":{"status":"fail","error":"cam_loc_lan is null"}}[参数空]cam_loc_lan为空
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询错误
* {"code": 402, "data":{"status":"fail","error":"camera exist"}}[参数问题]设备已经存在
* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
