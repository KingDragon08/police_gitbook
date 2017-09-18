name：删除兴趣点

url：/map/interestPoint/delPoint

method：post

params：

* mobile=&gt;手机号码
* token=&gt;token
* Id=&gt;兴趣点Id

返回值：

正确：

* {"code": 200, "data":{"status":"success","error":"success"}}

错误：

* {"code": 300, "data":{"status":"fail","error":"unknown error"}}删除兴趣点失败
* {"code": 300, "data":{"status":"fail","error":"mobile not match token"}}手机号码与token不匹配

备注 ：

删除成功时无论Id对应兴趣点是否存在都会返回成功

