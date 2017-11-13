name：PC按任务用户分页获取任务

url：/task/getUserTask

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* page: 分页数
* pageSize: 每页数据量，默认20
* userId: 用户Id

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/task/getUserTask",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    page:1,
    pageSize:10,
    userId:1
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```

返回值：

正确：

{"code":200,"data":{"status":"success","data":[{"Id":4,"cameraName":"cameraName","cameraLocation":"cameraLocation","taskDescription":"taskDescription","userId":1,"taskNO":"1509266954334","taskStatus":0,"cameraId":1,"rejectInfo":null},{"Id":3,"cameraName":"cameraName","cameraLocation":"cameraLocation","taskDescription":"taskDescription","userId":1,"taskNO":"1509264493188","taskStatus":0,"cameraId":3,"rejectInfo":null},{"Id":2,"cameraName":"cameraName","cameraLocation":"cameraLocation","taskDescription":"taskDescription","userId":1,"taskNO":"1509080264537","taskStatus":1,"cameraId":2,"rejectInfo":null}]},"total":100}

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

*新增total:任务总量

错误：

* res.json({ "code": 302, "data": { "status": "fail", "error": "param error1" } }); 参数不全
* res.json({ "code": 302, "data": { "status": "fail", "error": "param error1" } }); 参数不全
* res.json({ "code": 300, "data": { "status": "fail", "error": "mobile not match token" } }); 手机号和token不匹配

