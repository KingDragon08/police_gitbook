name：批量按列更新摄像头数据

url：/camera/multiEditCamerasByAttr

method：post

params：

* mobile: 手机号
* token: token
* excel: excel文件上传后返回的链接地址
* attrName: "cam_desc"

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/camera/multiEditCamerasByAttr",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    excel:"http://211.103.178.205/upload/test.xlsx",//excel文件名
    attrName: "cam_desc"
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
step1 => 新建excel文件，后缀名为xlsx
step2 => 录入数据，第一列为cam_id值，此值为摄像头在GIS系统中的唯一编号，若需要一次性下载，可在后台管理平台中进行下载
step3 => 上传文件
step4 => 批量更改开始

说明：

1.cam_id进行了parseInt处理，所以有一定的容错能力，但是不能报错
2.数据量较小时可以在管理平台进行单个更改，单个更改的可控性更强，出错率更低


