name：反馈摄像头周边信息

url：/camera/fbselflist

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* page: 页数[默认为-1：获取全部设备]
* pageSize: 每页数量[默认20]

示例：

```
{"mobile":"18310054013", "token":"890db0ae4ea95013865559fb89a3e109", "page":1, "pageSize":20}
```

返回值：

正确：

* {"code":200,"data":{"status":"success","error":"success","fb_id":4}}

错误：

* {"code": 401, "data":{"status":"fail","error":"cam_id is null"}} [参数空]cam_id为空
* {"code": 401, "data":{"status":"fail","error":"content is null"}}[参数空]content
* {"code": 404, "data":{"status":"fail","error":"camera not exist"}}[参数问题]设备不存在
* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询错误
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
