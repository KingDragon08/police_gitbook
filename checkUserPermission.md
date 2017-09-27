name：判断用户是否拥有指定权限

url：/user/checkUserPermission

method：post

params：

* mobile=&gt;手机号码
* password=&gt;密码明文
* permission=&gt;permission名字

返回值：

正确：

{"code":200,"data":{"start":"success","data":1}} 拥有权限
{"code":200,"data":{"start":"success","data":0}} 不拥有权限

错误：

* {"code":300,"data":{"status":"fail","error":"error params"}}参数错误
* {"code":300,"data":{"status":"fail","error":"moblie not match password"}}密码和手机号不匹配



