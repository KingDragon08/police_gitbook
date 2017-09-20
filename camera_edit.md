name：修改摄像头信息

url：/camera/edit

method：post

params：

1. 修改摄像头状态

2. mobile: 手机号\[必须\]

3. token: toke\[必须\]
4. cam\_id: 设备id\[必须\]
5. editType: status\[必须\]
6. cam\_sta: 设备状态\(取值0/1/2, 默认0; 0: 不激活, 1: 激活, 2: 故障\)

1. 修改摄像头信息

2. mobile: 手机号\[必须\]

3. token: toke\[必须\]
4. cam\_id: 设备id\[必须\]
5. editType: all\[必须\]
6. cam\_no: 设备编号\[必须, 且唯一\]
7. cam\_name: 设备名称
8. cam\_desc: 设备描述
9. cam\_loc\_lon: 设备地点经度\[必须\]
10. cam\_loc\_lan: 设备地点维度\[必须\]
11. cam\_sta: 设备状态\(取值0/1/2/3, 默认0; 0: 不激活, 1: 激活, 2: 故障\)

> editType: 修改信息\[必须\] \(取值status/all; status: 修改状态, all: 修改全部信息\)

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



