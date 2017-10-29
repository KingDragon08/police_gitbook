name：获取任务状态App

url：/task/getTaskStatus_App

method：post

params：

* mobile: 手机号[必须]
* token: token[必须]
* cameraId: 摄像头Id

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/task/getTaskStatus_App",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"3d9db3d7a0c3c4ef547422817d396a44",
    cameraId:1
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```

返回值：

正确：

{"code":200,"data":{"status":"success","data":{"taskStatus":0}}}

* taskStatus:
  * 0:未接受
  * 1:进行中
  * 2:审核中
  * 3:已完成
  * 4:审核不通过


错误：

* res.json({ "code": 302, "data": { "status": "fail", "error": "param error1" } }); 参数不全
* res.json({ "code": 302, "data": { "status": "fail", "error": "param error1" } }); 参数不全
* res.json({ "code": 300, "data": { "status": "fail", "error": "mobile not match token" } }); 手机号和token不匹配

