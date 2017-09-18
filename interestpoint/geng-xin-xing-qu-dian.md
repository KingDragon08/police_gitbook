name：更新兴趣点

url：/map/interestPoint/updatePoint

method：post

params：

* mobile=&gt;手机号码
* token=&gt;token
* Id=&gt;兴趣点Id号
* name=&gt;兴趣点名称
* longitude=&gt;兴趣点经度坐标
* latitude=&gt;兴趣点纬度坐标
* desc=&gt;兴趣点描述文字

返回值：

正确：

* {"code": 200, "data":{"status":"success","error":"success"}}

错误：

* {"code": 300, "data":{"status":"fail","error":"unknown error"}}更新兴趣点失败
* {"code": 300, "data":{"status":"fail","error":"params error"}}未传入Id号
* {"code": 300, "data":{"status":"fail","error":"mobile not match token"}}手机号码与token不匹配



