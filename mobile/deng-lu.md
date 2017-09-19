name：登录

url：/mobile/login

method：post

params：

* mobile=&gt;手机号码
* password=&gt;密码明文
* IP=&gt;IP地址

返回值：

正确：

{"code":200,"data":{"Id":8,"name":"first1","sex":"M","company":"westPolice","NO":"000123","mobile":"13810332932","lastLoginTime":"1505800911215","lastLoginIP":null,"avatar":"\[[http://www.baidu.com","token":"447b2c368f0a4935ce458fcf72dc3fad","status":"success"}}\]\(http://www.baidu.com","token":"447b2c368f0a4935ce458fcf72dc3fad","status":"success"}}](http://www.baidu.com","token":"447b2c368f0a4935ce458fcf72dc3fad","status":"success"}}]%28http://www.baidu.com","token":"447b2c368f0a4935ce458fcf72dc3fad","status":"success"}})\)

错误：

* {"code":300,"data":{"status":"fail","error":"moblie error"}}手机号码错误
* {"code":300,"data":{"status":"fail","error":"moblie not match password"}}密码和手机号不匹配
* { "code": 300, "data": { "status": "fail", "error": "unknown error" } }登录失败



