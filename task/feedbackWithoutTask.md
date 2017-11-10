name：反馈任务信息

url：/task/feedBackWithoutTask

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
  "url": "http://127.0.0.1:8080/task/feedBackWithoutTask",
  "method": "POST",
  "data":{
    mobile:"13810332931",//手机号码
    token:"3d9db3d7a0c3c4ef547422817d396a44",//token
    cameraName:"query.cameraName",//摄像头名字
    cameraLocation:"cameraLocation",//摄像头位置文字描述信息
    cameraLon:"cameraLon",//经度
    cameraLa:"cameraLa",//纬度
    cameraType:1,//摄像头的类型，暂定0=》民用，2=》警用
    userId:1,//派发给的人的Id
    content:"query.content",//反馈信息的文字内容
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