name：用户注册

url：/user/register

method：post

params：

* name=&gt;用户名
* password=&gt;密码明文
* sex=&gt;性别，F＝女，M＝男
* NO=&gt;警员编号
* mobile=&gt;手机号码

返回值：

正确：

* {"code":200,"data":{"status":"success","error":"success"}}

错误：

* {"code": 300, "data":{"status":"fail","error":"register error"}}注册失败
* {"code": 300, "data":{"status":"fail","error":"sex must be F or M"}}性别参数错误
* {"code": 300, "data":{"status":"fail","error":"moblie already exist"}}



