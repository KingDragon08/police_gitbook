name：圆形框选摄像头

url：/camera/cameraSelectCircle

method：post

params：
* mobile: 手机号[必须]
* token: token[必须]
* centerX: 中心点经度
* centerY: 中心点纬度
* radius: 半径（单位为地图坐标的单位）

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/camera/cameraSelectCircle",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    centerX:"400000",
    centerY:"300000",
    radius:100000,
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```

返回值：

正确：

{"code":200,"data":{"status":"success","data":[{"cam_id":2,"cam_no":"cam_99","cam_name":"cam_99","cam_sta":2,"addtime":"1506414499658","uptime":"1506414499658","user_id":1,"cam_loc_lan":"305352.33888985787","cam_loc_lon":"500241.7567744438","cam_desc":"cam_99_desc","is_del":0,"cam_addr":"cam_99_addr"},{"cam_id":3,"cam_no":"cam_98","cam_name":"cam_98","cam_sta":0,"addtime":"1506414499673","uptime":"1506414499673","user_id":1,"cam_loc_lan":"306493.8044095913","cam_loc_lon":"499650.3555874614","cam_desc":"cam_98_desc","is_del":0,"cam_addr":"cam_98_addr"}]}


错误：

* res.json({ "code": 302, "data": { "status": "fail", "error": "param error1" } }); 参数不全
* res.json({ "code": 302, "data": { "status": "fail", "error": "param error2" } }); 参数不全
* res.json({ "code": 300, "data": { "status": "fail", "error": "mobile not match token" } }); 手机号和token不匹配

