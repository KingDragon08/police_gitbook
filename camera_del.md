name：删除摄像头

url：/camera/del

method：post

params：

* mobile: 手机号
* token: token
* cam_id: 设备id
* cam_no: 设备编号

返回值：

正确：

{"code": 200, "data":{"status":"success","error":"success"}}

错误：

* {"code":300,"data":{"status":"fail","error":"moblie error"}}手机号码错误
* {"code":300,"data":{"status":"fail","error":"moblie not match password"}}密码和手机号不匹配
