name：反馈摄像头周边信息

url：/camera/feedback

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* cam_id: 设备id[必须]
* content: 反馈内容[必须]
* fb_loc_lon: 反馈地点经度
* fb_loc_lan: 反馈地点维度
* fb_addr: 反馈地点详细地点
* pics: 反馈图片链接[链接列表]

示例：

```
{"mobile":"18310054013", "token":"890db0ae4ea95013865559fb89a3e109", "cam_id":77, "content":"feedback", "pics":["link1", "link2"]}
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
