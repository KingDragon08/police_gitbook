name：根据任务Id获取任务的详情及反馈信息(PC)

url：/task/getTaskById

method：post

params：

参见示例代码

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/task/getTaskById",
  "method": "POST",
  "data":{
    mobile:"13810332931",//手机号码
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",//token
    taskId:1,//任务的Id号
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