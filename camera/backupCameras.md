name：批量添加摄像头

url：/camera/backupCameras

method：post

params：

* mobile: 手机号
* token: token

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/camera/backupCameras",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```


返回值：

正确：

{"code":200,"data":{"status":"success","error":"success"}}

错误：

* 错误类型太多，不一一列举了,错误原因都在data.error中


警告：

此操作为高危操作，操作失误可能导致不可控的结果，尽量增加用户使用的确认次数。

说明：

* 1.每次手动备份都会冲洗掉上次的备份内容，所以应谨慎操作
* 2.批量上传摄像头数据时无需调用此借口进行手动备份，没有意义，此项可以在管理平台用户进行手动备份时提示一下


