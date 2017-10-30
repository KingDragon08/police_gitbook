name：pc端获取摄像头反馈信息

url：/camera/pccamfblist

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* camId: 摄像头id[必须]
* page: 页数[默认为-1：获取全部设备]
* pageSize: 每页数量[默认20]

示例：

```
{"mobile":"12345678901", "token":"0a5f4ed005cd36223977e51742598a8c", "camId":77, "page":1}
```

返回值：

正确：

{"code":200,"data":{"status":"success","error":"success","rows":[{"fb_id":1,"cam_id":77,"content":"feedback","addtime":"1505896361748","user_id":10,"fb_loc_lon":"0","fb_loc_lan":"0","fb_addr":"","pics":[]},{"fb_id":2,"cam_id":77,"content":"feedback","addtime":"1505896458105","user_id":10,"fb_loc_lon":"0","fb_loc_lan":"0","fb_addr":"","pics":[]},{"fb_id":3,"cam_id":77,"content":"feedback","addtime":"1505896482898","user_id":10,"fb_loc_lon":"0","fb_loc_lan":"0","fb_addr":"","pics":[]},{"fb_id":4,"cam_id":77,"content":"feedback","addtime":"1505896514005","user_id":10,"fb_loc_lon":"0","fb_loc_lan":"0","fb_addr":"","pics":[]},{"fb_id":5,"cam_id":77,"content":"feedback","addtime":"1505896730864","user_id":10,"fb_loc_lon":"0","fb_loc_lan":"0","fb_addr":"","pics":[{"pic_id":1,"fb_id":5,"pic":"link1","addtime":"1505896730864"},{"pic_id":2,"fb_id":5,"pic":"link2","addtime":"1505896730864"}]}],"total":5,"page":1,"pageSize":20}}

错误：

* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 405, "data":{"status":"fail","error":"cameara not been checked"}}[参数问题]摄像头反馈信息未被审核
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询错误
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
