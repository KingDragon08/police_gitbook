name：反馈任务信息

url：/task/taskFeedBack

method：post

params：

参见示例代码

ajax：

```
//注意：pics必须是数组的json串
var pics=['url1','url2','url3'];
pics = JSON.stringify(pics);
//注意： cameraExtra必须是数组的JSON串,且数组元素名字与摄像头自定义属性一致
var cameraExtra={"attr_new_name":"attr_new_name_value"}
cameraExtra = JSON.stringify(cameraExtra);

var settings = {
  "url": "http://127.0.0.1:8080/task/taskFeedBack",
  "method": "POST",
  "data":{
    mobile:"13810332931",//手机号码
    token:"3d9db3d7a0c3c4ef547422817d396a44",//token
    taskId:5,//任务的Id号
    content:"query.content",//反馈信息的文字内容
    cameraLon:"query.cameraLon",//反馈地点的经度
    cameraLa:"query.cameraLa",//反馈地点的纬度
    cameraNo:"query.cameraNo",//摄像头编号
    cameraExtra:cameraExtra,//摄像头自定义属性
    pics:pics//图片数组JSON字符串
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