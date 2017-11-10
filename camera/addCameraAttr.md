name：添加摄像头属性

url：/camera/addCameraAttr

method：post

params：

* mobile: 手机号
* token: token
* attr_name:属性名[仅英文]
* attr_desc:属性描述信息

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/camera/addCameraAttr",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    attr_name:"attrName",//字段名
    attr_desc:"attr_description",//字段描述信息
    attr_comment:"attr_comment"//字段备注信息
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

* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询出错
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
