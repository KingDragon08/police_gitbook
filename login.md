name：登录

url：/user/login

method：post

params：

* mobile=&gt;手机号码
* password=&gt;密码明文
* IP=&gt;IP地址

返回值：

正确：

{"code":200,"data":{"Id":1,"name":"KingDragon","sex":"M","company":"test","NO":"000001","mobile":"13800000000","lastLoginTime":"1511488669567","lastLoginIP":"0.0.0.0","role_name":"测试","token":"f68a6b18da5abd5173fd795f0026ca9d","status":"success"}}

错误：

* {"code":300,"data":{"status":"fail","error":"moblie error"}}手机号码错误
* {"code":300,"data":{"status":"fail","error":"moblie not match password"}}密码和手机号不匹配



