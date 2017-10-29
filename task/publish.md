name：反馈摄像头周边信息

url：/camera/fbselflist

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* cameraName: 摄像头名称
* cameraLocation: 摄像头位置信息
* taskDescription：任务描述信息
* userId：任务对象的Id
* cameraId：任务对应的摄像头Id

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/task/publishTask",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    cameraName:"cameraName",
    cameraLocation:"cameraLocation",
    taskDescription:"taskDescription",
    userId:"1",
    cameraId:"1",
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```

返回值：

正确：

res.json({ "code": 200, "data": { "status": "success", "error": "success" } })

错误：

* res.json({ "code": 302, "data": { "status": "fail", "error": "param error1" } }); 参数不全
* res.json({ "code": 302, "data": { "status": "fail", "error": "param error1" } }); 参数不全
* res.json({ "code": 300, "data": { "status": "fail", "error": "mobile not match token" } }); 手机号和token不匹配
* res.json({ "code": 300, "data": { "status": "fail", "error": "cameraId exist in tasks" } }); 摄像头已经发布过任务了 

