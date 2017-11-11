name：审核任务

url：/task/checkTask

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* taskId: 任务Id
* cameraLon: 摄像头经度
* cameraLa: 摄像头纬度
* taskStatus: 审核状态，3=>审核通过，4=>审核不通过
* info: 审核不通过的原因，当审核通过时无效

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/task/checkTask",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    taskId:1,
    taskStatus:3,
    info:'checkInfo',
    cameraLon:'cameraLon',
    cameraLa:'cameraLa'
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```

返回值：

正确：

res.json({ "code": 200, "data": { "status": "success", "error": "success" } }); 


错误：

* res.json({ "code": 302, "data": { "status": "fail", "error": "param error1" } }); 参数不全
* res.json({ "code": 302, "data": { "status": "fail", "error": "param error1" } }); 参数不全
* res.json({ "code": 300, "data": { "status": "fail", "error": "mobile not match token" } }); 手机号和token不匹配

备注：

审核时对应的任务可能是采集新摄像头类型的任务，也有可能是对已有摄像头的信息采集
当任务是采集新摄像头时将会创建新的摄像头并添加到摄像头图层上，对已有摄像头信息采集不会增加摄像头

