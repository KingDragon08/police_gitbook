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

{"status":"success","taskData":{"Id":9,"cameraName":"query.cameraName","cameraLocation":"cameraLocation","taskDescription":"taskDescription","userId":1,"taskNO":"1510241863872","taskStatus":2,"cameraId":10737,"rejectInfo":null,"cameraLon":"cameraLon","cameraLa":"cameraLa","addtime":"1510241863872","cameraType":1},"taskFeedBacks":[{"Id":9,"taskId":9,"content":"9query.content","addtime":"1510242034337","cameraLon":"9query.cameraLon","cameraLa":"9query.cameraLa","camera_no":"9query.cameraNo","cameraExtra":"{\"attr_new_name\":\"9attr_new_name_value\"}","pics":3,"taskFeedBackPics":[{"Id":18,"taskFeedBackId":9,"url":"url91","addtime":"1510242034337"},{"Id":19,"taskFeedBackId":9,"url":"url92","addtime":"1510242034337"},{"Id":20,"taskFeedBackId":9,"url":"url93","addtime":"1510242034337"}]},{"Id":14,"taskId":9,"content":"query.content","addtime":"1510307062549","cameraLon":"query.cameraLon","cameraLa":"query.cameraLa","camera_no":"query.cameraNo","cameraExtra":"{\"attr_new_name\":\"attr_new_name_value\"}","pics":1,"taskFeedBackPics":[{"Id":31,"taskFeedBackId":14,"url":"http://www.xiaofen809.com:8080/upload/1510307062524.jpg","addtime":"1510307062549"}]}],"code":200}

错误：

* res.json({ "code": 302, "data": { "status": "fail", "error": "param error1" } }); 参数不全
* res.json({ "code": 302, "data": { "status": "fail", "error": "param error1" } }); 参数不全
* res.json({ "code": 300, "data": { "status": "fail", "error": "mobile not match token" } }); 手机号和token不匹配
* res.json({ "code": 300, "data": { "status": "fail", "error": "cameraId exist in tasks" } }); 摄像头已经发布过任务了 