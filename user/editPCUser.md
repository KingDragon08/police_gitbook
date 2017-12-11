name：编辑PC用户

url：/user/editPCUser

method：post

params：

* mobile=>mobile,当前登陆用户的手机号码
* token=>token
* Id=>更改的目标用户的Id号
* name=>新的用户名
* sex=>新的性别，M or F
* NO=>新的编号
* mobilenew=>更改的目标用户的新的手机号码，不可重复
* company=>所属部门的二级部门Id号
* role_id=>角色Id
返回值：

正确：

* {"code":200,"data":{"status":"success","error":"success"}}


