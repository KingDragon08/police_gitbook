name：根据Id删除PC用户

url：/user/delPCUser

method：post

params：

* mobile=>mobile,当前登陆用户的手机号码
* token=>token
* Id=>删除的目标用户的Id号
返回值：

正确：

* {"code":200,"data":{"status":"success","error":"success"}}



