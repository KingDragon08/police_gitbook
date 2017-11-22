name：手动还原摄像头

url：/camera/restoreCameras

method：post

params：

* mobile: 手机号
* token: token

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/camera/restoreCameras",
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

1.每次还原都会清空摄像头表，这将导致上次备份到还原发生时之间用户进行的添加摄像头属性操作后的所有新属性数据失效
2.这个接口就是给批量上传摄像头出错后擦屁股用的，代价很大

