name：添加车辆

url：/car/addCar

method：post

params：

* mobile=&gt;手机号码
* token=&gt;登录后返回的token
* NO=&gt;车牌号
* type=&gt;车辆类型，1：巡逻车，2：环卫车，默认1

返回值：

正确：

* {"code":200,"data":{"status":"success","error":"success"}}

错误：

* { "code": 300, "data": { "status": "fail", "error": "unkown error" } }添加失败
* {"code":300,"data":{"status":"fail","error":"params error"}}没有传入车牌号
* { "code": 300, "data": { "status": "fail", "error": "mobile not match token" } }手机号码和token不匹配



