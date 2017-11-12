name：编辑摄像头属性

url：/camera/editCameraAttr

method：post

params：

* mobile: 手机号
* token: token
* attrId:属性Id［必须大于12，12以内的属性不允许编辑］
* attrNewName:属性新名字
* attrNewDesc:属性新描述信息
* attrNewComment:字段的新备注信息
* attrShow:前台是否默认选中展示,0->不默认展示,1->默认展示,默认值1.

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/camera/editCameraAttr",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    attrId:13,
    attrNewName:"attrNewName",//字段的新名字
    attrNewDesc:"attr_new_description",//字段的新描述信息
    attrNewComment:"attrNewComment",//字段的新备注信息
    attrShow:1//前台是否默认选中展示
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
