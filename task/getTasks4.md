name：App分页按状态获取自己的任务

url：/task/getTaskMobile

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* page: 分页数
* pageSize: 每页数据量，默认20
* userId: 用户Id
* taskStatus:
  * 0:未接受
  * 1:进行中
  * 2:审核中
  * 3:已完成
  * 4:审核不通过

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/task/getTaskMobile",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"3d9db3d7a0c3c4ef547422817d396a44",
    page:1,
    pageSize:10,
    userId:1,
    taskStatus:0
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```

返回值：

正确：

{"code":200,"data":{"status":"success","data":[{"Id":4,"cameraName":"cameraName","cameraLocation":"cameraLocation","taskDescription":"taskDescription","userId":1,"taskNO":"1509266954334","taskStatus":0,"cameraId":1,"rejectInfo":null},{"Id":3,"cameraName":"cameraName","cameraLocation":"cameraLocation","taskDescription":"taskDescription","userId":1,"taskNO":"1509264493188","taskStatus":0,"cameraId":3,"rejectInfo":null}]}}

* Id:任务的Id
* cameraName:摄像头名字
* cameraLocation:摄像头位置信息
* taskDescription:任务描述信息
* userId:任务的userId
* taskNO:任务编号
* taskStatus:任务状态
* cameraId:摄像头Id
* rejectInfo:被拒绝的原因
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

