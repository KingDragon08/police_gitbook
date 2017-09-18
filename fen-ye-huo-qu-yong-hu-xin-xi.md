name：分页获取用户信息

url：/user/getUsers

method：post

params：

* mobile=&gt;手机号码
* token=&gt;登录后返回的token串
* page=&gt;页数，从1开始，可不传（默认为1）

返回值：

正确：

{"code":200,"data":{"Id":1,"name":"KingDragon","sex":"M","company":"test","NO":"000001","mobile":"13800000000","lastLoginTime":"1505666219993","lastLoginIP":"1.2.3.4","token":"46eb69812c6d7b41d8a5fd334f073020","status":"success"}}

错误：

* {"code":300,"data":{"status":"fail","error":"moblie error"}}手机号码错误
* {"code":300,"data":{"status":"fail","error":"moblie not match password"}}密码和手机号不匹配



