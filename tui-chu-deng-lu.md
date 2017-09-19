name：退出登录

url：/user/logout

method：post

params：

* mobile=&gt;手机号码
* token=&gt;登录时返回的token

返回值：

正确：

{"code":200,"data":{"status":"success","error":"logout success"}}

错误：

* {"code": 300, "data":{"status":"fail","error":"moblie not match token"}}手机号码和token不匹配
* {"code": 300, "data":{"status":"fail","error":"unkown error"}}退出失败



