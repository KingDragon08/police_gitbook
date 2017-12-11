name：删除一级部门

url：department/delete1

method：post

params：

* mobile=>mobile,当前登陆用户的手机号码
* token=>token
* id=>一级部门Id
返回值：

正确：
* {"code":200,"data":{"status":"success","error":"success"}}

错误：
* errMessage(res,301,"该部门下有子部门，请勿删除");


