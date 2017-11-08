name：根据任务Id获取任务的详情及反馈信息(APP)

url：/task/getTaskByIdAPP

method：post

params：

参见示例代码

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/task/getTaskByIdAPP",
  "method": "POST",
  "data":{
    mobile:"13810332931",//手机号码
    token:"3d9db3d7a0c3c4ef547422817d396a44",//token
    taskId:1,//任务的Id号
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```

返回值：

正确：

{"code":200,"data":{"status":"success","taskData":{"Id":5,"cameraName":"query.cameraName","cameraLocation":"cameraLocation","taskDescription":"taskDescription","userId":1,"taskNO":"1510062011426","taskStatus":3,"cameraId":10734,"rejectInfo":null,"cameraLon":"cameraLon","cameraLa":"cameraLa","addtime":"1510062011426","cameraType":1},"taskFeedBack":[{"Id":1,"taskId":5,"content":"query.content","addtime":"1510062628616","cameraLon":"query.cameraLon","cameraLa":"query.cameraLa"}],"taskFeedBackPics":[{"Id":1,"taskId":5,"url":"url1","addtime":"1510062628616"},{"Id":2,"taskId":5,"url":"url2","addtime":"1510062628616"},{"Id":3,"taskId":5,"url":"url3","addtime":"1510062628616"}]}}

错误：

* res.json({ "code": 302, "data": { "status": "fail", "error": "param error1" } }); 参数不全
* res.json({ "code": 302, "data": { "status": "fail", "error": "param error1" } }); 参数不全
* res.json({ "code": 300, "data": { "status": "fail", "error": "mobile not match token" } }); 手机号和token不匹配
* res.json({ "code": 300, "data": { "status": "fail", "error": "cameraId exist in tasks" } }); 摄像头已经发布过任务了 