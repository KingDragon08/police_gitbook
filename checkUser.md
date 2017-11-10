name：审核用户

url：/user/checkUser

method：post

params：

* mobile: 手机号[必须]
* token: toke[必须]
* Id: 审核用户的Id
* type: 1:审核通过,0:审核不通过,将会删除该用户的注册信息

ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/user/checkUser",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    Id:1,
    type:1
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```

返回值：

正确：

res.json({ "code": 200, "data": {"error": "success" } }); 


错误：

* res.json({ "code": 302, "data": { "status": "fail", "error": "param error1" } }); 参数不全
* res.json({ "code": 302, "data": { "status": "fail", "error": "param error1" } }); 参数不全
* res.json({ "code": 300, "data": { "status": "fail", "error": "mobile not match token" } }); 手机号和token不匹配
