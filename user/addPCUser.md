name：添加PC用户

url：/user/addPCUser

method：post

params：

* mobile=>mobile,当前登陆用户的手机号码
* token=>token
* name=>用户名
* password=>密码
* sex=>性别,M or F
* NO=>编号
* mobilenew=>添加的目标PC用户的手机号码
* company=>用户所属二级部门id号
* role_id=>用户角色id号

返回值：

正确：

* {"code":200,"data":{"status":"success","error":"success"}}


