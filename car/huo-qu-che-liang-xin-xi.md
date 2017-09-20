name：获取车辆信息

url：/car/getCar

method：post

params：

* mobile=&gt;手机号码
* token=&gt;登录后返回的token
* page=&gt;分页数，－1：获取全部，默认－1
* pageSize=&gt;单页记录条数，默认20
* type=&gt;车辆类型，1：巡逻车，2：环卫车，默认1

返回值：

正确：

* {"code":200,"data":{"status":"success","data":\[{"Id":1,"NO":"京A00001"}\]}}

错误：

* { "code": 300, "data": { "status": "fail", "error": "unkown error" } }获取失败

* { "code": 300, "data": { "status": "fail", "error": "mobile not match token" } }手机号码和token不匹配



