name：使用token登录

url：/mobile/loginWithToken

method：post

params：

* mobile=&gt;手机号码
* token=&gt;登录接口返回的token串

* IP=&gt;IP地址

返回值：

正确：

{"code":200,"data":{"Id":1,"name":"KingDragon","sex":"M","company":"test","NO":"000001","mobile":"13800000000","lastLoginTime":"1505666219993","lastLoginIP":"1.2.3.4","token":"46eb69812c6d7b41d8a5fd334f073020","status":"success"}}

错误：

* {"code": 300, "data":{"status":"fail","error":"unkown error"}}登录失败
* {"code": 300, "data":{"status":"fail","error":"moblie not match token"}}token和手机号不匹配

备注：

使用token登录后token会更新，需要更新本地缓存的token



