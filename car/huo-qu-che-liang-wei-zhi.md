name：获取车辆位置

url：/car/getCarPosition

method：post

params：

* mobile=&gt;手机号码
* token=&gt;登录后返回的token
* Id=&gt;车辆Id号

返回值：

正确：

* {"code":200,"data":{"status":"success","data":{"longitude":100.52367032386921,"latitude":100.05210268197992}}}

错误：

* { "code": 300, "data": { "status": "fail", "error": "unkown error" } }获取失败
* {"code":300,"data":{"status":"fail","error":"params error"}}没有传入车辆Id号
* { "code": 300, "data": { "status": "fail", "error": "mobile not match token" } }手机号码和token不匹配



