name：添加App用户

url：/user/addMobileUser

method：post

params：

* name=&gt;用户名
* password=&gt;密码明文
* sex=&gt;性别，F＝女，M＝男
* NO=&gt;警员编号
* mobile=&gt;手机号码
* company=&gt;所属单位
* avatar=&gt;头像
* userMobile=&gt;操作用户的手机号码
* token=&gt;登录后返回的token

返回值：

正确：

* {"code":200,"data":{"status":"success","error":"success"}}

错误：

* { "code": 300, "data": { "status": "fail", "error": "unkown error" } }添加失败
* {"code": 300, "data":{"status":"fail","error":"sex must be F or M"}}性别参数错误
* {"code": 300, "data":{"status":"fail","error":"mobile already exist"}}手机号码已经存在
* { "code": 300, "data": { "status": "fail", "error": "mobile not match token" } }手机号码和token不匹配



