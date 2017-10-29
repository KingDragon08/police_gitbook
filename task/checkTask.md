name：审核任务

url：/task/checkTask

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* taskId: 任务Id
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
    info:'checkInfo'
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

