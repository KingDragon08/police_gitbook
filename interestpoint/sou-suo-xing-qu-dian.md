name：搜索兴趣点

url：/map/interestPoint/searchPoint

method：post

params：

* mobile=&gt;手机号码
* token=&gt;token
* keyword=&gt;关键字

返回值：

正确：

* {"code":200,"data":{"status":"success","data":\[{"Id":2,"name":"first","longitude":"0.0001","latitude":"123.456","desc":"description"},{"Id":1,"name":"first","longitude":"654.321","latitude":"123.456","desc":"description1"}\]}}

错误：

* {"code": 300, "data":{"status":"fail","error":"unknown error"}}搜索兴趣点失败

* {"code": 300, "data":{"status":"fail","error":"mobile not match token"}}手机号码与token不匹配



