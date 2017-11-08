name：发布任务-采集新摄像头

url：/task/publishTaskWithoutCamera

method：post

params：

参见示例代码

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/task/publishTaskWithoutCamera",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    cameraName:"query.cameraName",//摄像头名字
    cameraLocation:"cameraLocation",//摄像头位置文字描述信息
    cameraLon:"cameraLon",//经度
    cameraLa:"cameraLa",//纬度
    taskDescription:"taskDescription",//任务的文字描述信息下,
    cameraType:1,//摄像头的类型，暂定0=》民用，2=》警用
    userId:1//派发给的人的Id
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

