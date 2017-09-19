name：修改摄像头信息

url：/camera/edit

method：post

params：

1. 修改摄像头状态

* mobile: 手机号[必须]
* token: toke[必须]
* cam_id: 设备id[必须]
* editType: status[必须]
* cam_sta: 设备状态(取值0/1/2, 默认0; 0: 不激活, 1: 激活, 2: 故障)


2. 修改摄像头信息

* mobile: 手机号[必须]
* token: toke[必须]
* cam_id: 设备id[必须]
* editType: all[必须]
* cam_no: 设备编号[必须, 且唯一]
* cam_name: 设备名称
* cam_desc: 设备描述
* cam_loc_lon: 设备地点经度[必须]
* cam_loc_lan: 设备地点维度[必须]
* cam_sta: 设备状态(取值0/1/2/3, 默认0; 0: 不激活, 1: 激活, 2: 故障)

> editType: 修改信息[必须] (取值status/all; status: 修改状态, all: 修改全部信息)

返回值：

正确：

{"code": 200, "data":{"status":"success","error":"success"}}

错误：

* {"code": 401, "data":{"status":"fail","error":"cam_id is null"}}[参数错误]cam_id为空
* {"code": 401, "data":{"status":"fail","error":"camera no is null"}} [参数空]cam_no为空
* {"code": 401, "data":{"status":"fail","error":"cam_loc_lon is null"}}[参数空]cam_loc_lon为空
* {"code": 401, "data":{"status":"fail","error":"cam_loc_lan is null"}}[参数空]cam_loc_lan为空
* {"code": 403, "data":{"status":"fail","error":"editType is illegal"}}[参数错误]editType取值错误
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询出错
* {"code": 404, "data":{"status":"fail","error":"camera not exist"}}[参数错误]设备不存在
* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
