name：pc端根据摄像头Id获取摄像头反馈信息

url：/camera/pccamfblist

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* camId: 摄像头id[必须]

ajax:
```
var settings = {
  "url": "http://127.0.0.1:8080/camera/pccamfblist",
  "method": "POST",
  "data":{
    mobile:"13810332931",//手机号码
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",//token
    camId: 10737
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```

返回值：

正确：
```
{"code":200,"status":"success","data":[{"Id":5,"cameraName":"query.cameraName","cameraLocation":"cameraLocation","taskDescription":"taskDescription","userId":1,"taskNO":"1510062011426","taskStatus":2,"cameraId":10737,"rejectInfo":null,"cameraLon":"cameraLon","cameraLa":"cameraLa","addtime":"1510062011426","cameraType":1,"taskFeedBacks":[{"Id":1,"taskId":5,"content":"query.content","addtime":"1510062628616","cameraLon":"query.cameraLon","cameraLa":"query.cameraLa","camera_no":null,"cameraExtra":null,"pics":[{"Id":1,"taskFeedBackId":1,"url":"url1","addtime":"1510062628616"},{"Id":2,"taskFeedBackId":1,"url":"url2","addtime":"1510062628616"},{"Id":3,"taskFeedBackId":1,"url":"url3","addtime":"1510062628616"},{"Id":8,"taskFeedBackId":1,"url":"http://www.xiaofen809.com:8080/upload/1510226765020.jpg","addtime":"1510226765145"}]},{"Id":6,"taskId":5,"content":"query.content","addtime":"1510240477590","cameraLon":"query.cameraLon","cameraLa":"query.cameraLa","camera_no":"query.cameraNo","cameraExtra":"{\"attr_new_name\":\"attr_new_name_value\"}","pics":[{"Id":9,"taskFeedBackId":6,"url":"url1","addtime":"1510240477590"},{"Id":10,"taskFeedBackId":6,"url":"url2","addtime":"1510240477590"},{"Id":11,"taskFeedBackId":6,"url":"url3","addtime":"1510240477590"}]},{"Id":7,"taskId":5,"content":"query.content","addtime":"1510240693451","cameraLon":"query.cameraLon","cameraLa":"query.cameraLa","camera_no":"query.cameraNo","cameraExtra":"{\"attr_new_name\":\"attr_new_name_value\"}","pics":[{"Id":12,"taskFeedBackId":7,"url":"url1","addtime":"1510240693451"},{"Id":13,"taskFeedBackId":7,"url":"url2","addtime":"1510240693451"},{"Id":14,"taskFeedBackId":7,"url":"url3","addtime":"1510240693451"}]},{"Id":8,"taskId":5,"content":"query.content","addtime":"1510241887990","cameraLon":"query.cameraLon","cameraLa":"query.cameraLa","camera_no":"query.cameraNo","cameraExtra":"{\"attr_new_name\":\"attr_new_name_value\"}","pics":[{"Id":15,"taskFeedBackId":8,"url":"url1","addtime":"1510241887990"},{"Id":16,"taskFeedBackId":8,"url":"url2","addtime":"1510241887990"},{"Id":17,"taskFeedBackId":8,"url":"url3","addtime":"1510241887990"}]}]},{"Id":9,"cameraName":"query.cameraName","cameraLocation":"cameraLocation","taskDescription":"taskDescription","userId":1,"taskNO":"1510241863872","taskStatus":3,"cameraId":10737,"rejectInfo":null,"cameraLon":"cameraLon","cameraLa":"cameraLa","addtime":"1510241863872","cameraType":1,"taskFeedBacks":[{"Id":9,"taskId":9,"content":"9query.content","addtime":"1510242034337","cameraLon":"9query.cameraLon","cameraLa":"9query.cameraLa","camera_no":"9query.cameraNo","cameraExtra":"{\"attr_new_name\":\"9attr_new_name_value\"}","pics":[{"Id":18,"taskFeedBackId":9,"url":"url91","addtime":"1510242034337"},{"Id":19,"taskFeedBackId":9,"url":"url92","addtime":"1510242034337"},{"Id":20,"taskFeedBackId":9,"url":"url93","addtime":"1510242034337"}]}]}]}
```

错误：

* {"code": 301, "data":{"status":"fail","error":"user not login"}}[权限问题]用户未登录
* {"code": 405, "data":{"status":"fail","error":"cameara not been checked"}}[参数问题]摄像头反馈信息未被审核
* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询错误
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误
