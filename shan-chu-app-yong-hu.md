name：删除App用户

url：/user/delMobileUser

method：post

params：

* mobile=&gt;操作用户的手机号码
* token=&gt;登录后返回的token
* Id=&gt;删除用户的Id
* type=&gt;1：彻底删除，不可恢复；2：隐藏用户，可恢复

返回值：

正确：

* {"code":200,"data":{"status":"success","error":"success"}}

错误：

* { "code": 300, "data": { "status": "fail", "error": "unkown error" } }删除失败
* { "code": 300, "data": { "status": "fail", "error": "mobile not match token" } }手机号码和token不匹配

备注 ：

删除时无论对应Id的App用户是否存在，只要参数正确，都会返回成功

