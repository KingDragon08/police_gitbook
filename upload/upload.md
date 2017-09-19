name：单个文件上传

url：/file/upload

method：post

params：

* mobile=&gt;手机号码
* token=&gt;登录后返回的token
* file=&gt;文件

返回值：

正确：

{ "code": 200, "data": { "status": "success", "error": "upload success", "url": url } }

错误：

* {"code":300,"data":{"status":"fail","error":"unknown error"}}上传失败
* {"code":300,"data":{"status":"fail","error":"moblie not match password"}}密码和手机号不匹配

事例 ：





