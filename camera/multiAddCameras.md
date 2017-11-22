name：批量添加摄像头

url：/camera/multiAddCameras

method：post

params：

* mobile: 手机号
* token: token
* excel: excel文件上传后返回的链接地址

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/camera/multiAddCameras",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    excel:"http://211.103.178.205/upload/test.xlsx",//excel文件名
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
使用顺序：
step1 => 管理平台下载最新版本的摄像头模版
step2 => 对下载后的模板进行数据录入
step3 => 上传文件
step4 => 批量导入开始

说明：

1.批量录入时系统会对数据库摄像头相关表格进行一次备份，此次备份会冲洗掉上次备份的数据，因此只有一步回退的能力，需谨慎操作。
2.当数据量较小，人力可为时应尽量采用管理平台中的添加摄像头功能进行逐个添加，这样可以保证数据的完整和一致性，且不会出现不可控的错误。
3.虽然此方法提供一定的数据备份能力，但最保险的还是人工备份数据库，否则可能GG。


