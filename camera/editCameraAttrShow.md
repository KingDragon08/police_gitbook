name：编辑摄像头属性展示

url：/camera/editCameraAttrShow

method：post

params：

* mobile: 手机号
* token: token
* attrId:属性Id
* attr_show_1:tips是否默认选中展示,0->不选中,1－>选中,默认选中
* attr_show_2:详细信息是否默认选中展示,0->不选中,1－>选中,默认选中
* attr_show_3:列表属性是否默认选中展示,0->不选中,1－>选中,默认选中

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/camera/editCameraAttrShow",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    attrId:13,
    attrNewName:"attrNewName",//字段的新名字
    attrNewDesc:"attr_new_description",//字段的新描述信息
    attrNewComment:"attrNewComment",//字段的新备注信息
    attr_show_1:1,//tips是否默认选中展示
    attr_show_2:1,//详细信息是否默认选中展示
    attr_show_3:1,//列表属性是否默认选中展示
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
