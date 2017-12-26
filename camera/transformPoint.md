name：坐标转换

url：/camera/addCameraAttr

method：post

params：

* mobile: 手机号
* token: token
* cam_loc_lan:cam_loc_lan
* cam_loc_lon:cam_loc_lon

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8081/camera/transformPoint",
  "method": "POST",
  "data":{
    mobile:"12345678901",
    token:"1",
    cam_loc_lan:39.907194,
    cam_loc_lon:116.376302,
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```


返回值：

正确：

{"code":200,"data":{"cam_loc_lon":"116.376302","cam_loc_lan":"39.907194","x":501494.0801995288,"y":304417.36149998003,"status":"success","error":"success"}}

错误：

* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询出错
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
