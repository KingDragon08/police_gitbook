name：获取兴趣点

url：/map/interestPoint/addPoint

method：post

params：

* mobile=&gt;手机号码
* token=&gt;token
* type=&gt;获取类型，1:获取全部兴趣点，2分页获取兴趣点，默认type＝1
* page=&gt;页数，当type＝2时有效，默认page＝1
* pageSize=&gt;每页兴趣点个数，当type＝2时有效，默认pageSize＝20

返回值：

正确：

* {"code":200,"data":{"status":"success","data":\[{"Id":2,"name":"first","longitude":"0.0001","latitude":"123.456","desc":"description"},{"Id":1,"name":"unknown","longitude":"0","latitude":"0","desc":"0"}\]}}

错误：

* {"code": 300, "data":{"status":"fail","error":"unknown error"}}获取兴趣点失败
* {"code": 300, "data":{"status":"fail","error":"mobile not match token"}}手机号码与token不匹配



