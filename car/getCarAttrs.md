name：获取摄像头所有属性

url：/camera/getCarAttrs

method：post

params：

* mobile: 手机号
* token: token
* type 1=>获取用户自定义属性;-1=>获取所有属性;默认－1

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/camera/getCarAttrs",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    type:-1
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```


返回值：

正确：




错误：

* {"code": 501, "data":{"status":"fail","error":err.message}}[系统错误]数据库查询出错
* {"code": 500, "data":{"status":"fail","error":e.message}}[系统错误]未知错误

备注：

车辆信息不归咱们维护,咱们只是调用别人的接口而已,所以这些属性都很鸡肋,还是说车辆信息也由我们维护，只是位置信息从甲方获取？这样子的话就需要将camera对应的代码复制一份,改一下表名就可以使用了 


