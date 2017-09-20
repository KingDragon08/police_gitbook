name：获取单个车辆信息

url：/car/getSingleCarInfo

method：post

params：

* mobile=&gt;手机号码
* token=&gt;登录后返回的token
* Id=&gt;车辆Id号

返回值：

正确：

* {"code":200,"data":{"status":"success","data":\[{"Id":1,"NO":"京A00001","type":1}\]}}

错误：

* { "code": 300, "data": { "status": "fail", "error": "unkown error" } }删除失败
* {"code":300,"data":{"status":"fail","error":"params error"}}没有传入车辆Id号
* { "code": 300, "data": { "status": "fail", "error": "mobile not match token" } }手机号码和token不匹配



