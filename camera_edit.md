name：修改摄像头信息

url：/camera/edit

method：post

params：

* mobile: 手机号
* token: token
* cam_id: 设备id
* cam_no: 设备编号
* cam_name: 设备名称
* cam_loc: 设备地点
* cam_sta: 设备状态(取值0/1/2, 默认0; 0: 不激活, 1: 激活, 2: 故障)

返回值：

正确：

{"code": 200, "data":{"status":"success","error":"success"}}

错误：

* {"code":300,"data":{"status":"fail","error":"moblie error"}}手机号码错误
* {"code":300,"data":{"status":"fail","error":"moblie not match password"}}密码和手机号不匹配
