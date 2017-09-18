name：根据手机号码获取单个用户信息

url：/user/getUsersByKeyword

method：post

params：

* mobile=&gt;手机号码
* token=&gt;登录后返回的token串
* keyword=&gt;用户名关键字

返回值：

正确：

{"code":200,"data":{"status":"success","data":\[{"Id":7,"name":"UNKNOWN","sex":"M","company":"west","NO":"000000","mobile":"12345678901","lastLoginTime":"1505725195366","lastLoginIP":"0.0.0.0"},{"Id":1,"name":"KingDragon","sex":"M","company":"test","NO":"000001","mobile":"13800000000","lastLoginTime":"1505708350858","lastLoginIP":"0.0.0.0"}\]}}

错误：

* {"code": 300, "data":{"status":"fail","error":"unkown error"}}参数错误
* {"code":300,"data":{"status":"fail","error":"moblie not match password"}}密码和手机号不匹配



