name：获取摄像头所有属性-手机用

url：/camera/getCameraAttrs_APP

method：post

params：

* mobile: 手机号
* token: token
* type 1=>获取用户自定义属性;-1=>获取所有属性;默认－1

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/camera/getCameraAttrs_APP",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"3d9db3d7a0c3c4ef547422817d396a44",
    type:-1
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```


返回值：

正确：

{"code":200,"data":{"status":"success","error":"success","rows":[{"Id":1,"attr_name":"cam_id","attr_desc":"摄像头ID"},{"Id":2,"attr_name":"cam_no","attr_desc":"摄像头编号"},{"Id":3,"attr_name":"cam_name","attr_desc":"摄像头名字"},{"Id":4,"attr_name":"cam_sta","attr_desc":"摄像头类别"},{"Id":5,"attr_name":"addtime","attr_desc":"摄像头添加时间"},{"Id":6,"attr_name":"uptime","attr_desc":"摄像头更新时间"},{"Id":7,"attr_name":"user_id","attr_desc":"摄像头采集人ID"},{"Id":8,"attr_name":"cam_loc_lan","attr_desc":"摄像头纬度"},{"Id":9,"attr_name":"cam_loc_lon","attr_desc":"摄像头经度"},{"Id":10,"attr_name":"cam_desc","attr_desc":"摄像头描述信息"},{"Id":11,"attr_name":"is_del","attr_desc":"摄像头是否删除"},{"Id":12,"attr_name":"cam_addr","attr_desc":"摄像头地址"}]}}

错误：

* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询出错
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误


备注：

返回结果新增attr_show字段,0表示不选中,1表示选中

