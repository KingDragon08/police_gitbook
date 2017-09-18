name：添加兴趣点

url：/map/interestPoint/addPoint

method：post

params：

* mobile=&gt;手机号码
* token=&gt;token
* name=&gt;兴趣点名称
* longitude=&gt;兴趣点经度坐标
* latitude=&gt;兴趣点纬度坐标
* desc=&gt;兴趣点描述文字

返回值：

正确：

* {"code": 200, "data":{"status":"success","error":"success"}}

错误：

* {"code": 300, "data":{"status":"fail","error":"unknown error"}}添加兴趣点失败
* {"code": 300, "data":{"status":"fail","error":"mobile not match token"}}手机号码与token不匹配



