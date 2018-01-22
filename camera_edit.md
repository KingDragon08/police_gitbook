name：修改摄像头信息

url：/camera/edit

method：post

params：

params：

* mobile: 手机号[必须]
* token: token[必须]
* cam_id: cam_id[必须]
* cam_no: 设备编号[必须]
* cam_name: 设备名称
* cam_desc: 设备描述
* cam_addr: 设备详细地址
* cam_loc_lon: 设备地点经度[必须]
* cam_loc_lan: 设备地点维度[必须]
* cam_sta: 设备状态(取值0/1/2/3, 默认0; 0: 不激活, 1: 激活, 2: 故障)
* cam_extra: 用户自定义属性JSON字符串

ajax：

```
//注意：cam_extra必须是数组的json串
var cam_extra={"attr_new_name":"attr_new_name_value","SBBM":"SBBM","A":"A"}
cam_extra = JSON.stringify(cam_extra);
var settings = {
  "url": "http://127.0.0.1:8080/camera/edit",
  "method": "POST",
  "data":{
    mobile:"13810332931",//手机号码
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",//token
    cam_id:10742,//摄像头Id［必须］
    cam_no: "cam_no",
    cam_name: "cam_name",
    cam_desc: "cam_desc",
    cam_addr: "cam_addr",
    cam_loc_lon: "500145",
    cam_loc_lan: "306148",
    cam_sta: 2,//摄像头类型
    cam_extra: cam_extra//用户自定义属性
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```

返回值：

正确：

{"code": 200, "data":{"status":"success","error":"success"}}

错误：

* {"code": 401, "data":{"status":"fail","error":"cam\_id is null"}}\[参数错误\]cam\_id为空
* {"code": 401, "data":{"status":"fail","error":"camera no is null"}} \[参数空\]cam\_no为空
* {"code": 401, "data":{"status":"fail","error":"cam\_loc\_lon is null"}}\[参数空\]cam\_loc\_lon为空
* {"code": 401, "data":{"status":"fail","error":"cam\_loc\_lan is null"}}\[参数空\]cam\_loc\_lan为空
* {"code": 403, "data":{"status":"fail","error":"editType is illegal"}}\[参数错误\]editType取值错误
* {"code": 501, "data":{"status":"fail","error":err.message}}\[系统错误\]数据库查询出错
* {"code": 404, "data":{"status":"fail","error":"camera not exist"}}\[参数错误\]设备不存在
* {"code": 301, "data":{"status":"fail","error":"user not login"}}\[权限问题\]用户未登录
* {"code": 500, "data":{"status":"fail","error":e.message}}\[系统错误\]未知错误
