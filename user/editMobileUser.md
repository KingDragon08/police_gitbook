name：编辑app用户

url：/user/editMobileUser

method：post

params：

* mobile=>mobile,当前登陆用户的手机号码
* token=>token
* Id=>更改的目标用户的Id
* name=>新的用户名
* sex=>新的性别，M or F
* NO=>新的编号
* mobile=>新的手机号码，不可重复
* company=>新的二级部门Id
* avatar=>新的头像
返回值：

正确：

* {"code":200,"data":{"status":"success","error":"success"}}


