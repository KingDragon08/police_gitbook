name：强制用户下线

url：/user/forceLogout

method：post

params：

* mobile=>mobile,当前登陆用户的手机号码
* token=>token
* targetId=>强制下线的目标用户的Id号
* type=>下线的用户类型,1->PC用户,2->手机用户,默认1
返回值：

正确：

* {"code":200,"data":{"status":"success","error":"success"}}



