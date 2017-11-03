name：删除任务

url：/task/acceptTaskStatus_App

method：post

params：

* mobile: 手机号[必须]
* token: token[必须]
* taskId: 任务Id

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/task/acceptTaskStatus_App",
  "method": "POST",
  "data":{
  	mobile:"13810332931",
  	token:"3d9db3d7a0c3c4ef547422817d396a44",
  	taskId:1
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```

返回值：

正确：

res.json({ "code": 200, "data": { "status": "success", "error": "success" }}); 


错误：

* res.json({ "code": 302, "data": { "status": "fail", "error": "param error1" } }); 参数不全
* res.json({ "code": 302, "data": { "status": "fail", "error": "param error2" } }); 参数不全
* res.json({ "code": 300, "data": { "status": "fail", "error": "mobile not match token" } }); 手机号和token不匹配

