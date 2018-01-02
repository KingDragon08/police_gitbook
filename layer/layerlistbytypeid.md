name：根据图层类型Id获取图层列表

url：/layer/layerlistbytypeid

method：post

params：

* mobile: 手机号[必须]
* token: token[必须]
* layerTypeId: 图层类型id号
* page: 页码[默认为1，-1全部]
* pageSize: 每页大小

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8081/layer/layerlistbytypeid",
  "method": "POST",
  "data":{
    mobile: "13810332931",
    token: "1",
    layerTypeId: 0,
    page:1,
    pageSize:4
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});

```

返回值：

正确：

{"code":200,"data":{"status":"success","error":"success","rows":[{"layer_id":1,"layer_name":"摄像头","img_path":"http://211.103.178.205:8081/upload/1513100508342.jpg","table_name":"camera","user_id":1,"addtime":"1513103852380","type_id":0},{"layer_id":11,"layer_name":"dsaf","img_path":"http://211.103.178.205:8081/upload/1513103879417.jpg","table_name":"layer_table_151310388547925","user_id":2,"addtime":"1513103885479","type_id":0},{"layer_id":13,"layer_name":"测试图层","img_path":"http://211.103.178.205:8081/upload/1513100508342.jpg","table_name":"layer_table_151313561748168","user_id":6,"addtime":"1513135617481","type_id":0},{"layer_id":15,"layer_name":"ooo","img_path":"http://211.103.178.205:8081/upload/1513140677003.jpg","table_name":"layer_table_151314067702028","user_id":2,"addtime":"1513140677020","type_id":0}],"total":14,"page":"1","pageSize":"4"}}

错误：

* {"code": 401, "data":{"status":"fail","error":"request param is invalid"}} [参数问题]请求参数为空或者不合法
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询错误
* {"code": 402, "data":{"status":"fail","error":"camera exist"}}[参数问题]设备已经存在
* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
