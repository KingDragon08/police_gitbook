name：添加一级部门

url：/department/add1

method：post

params：

* mobile: 手机号
* token: token
* name: 一级部门名字[不可重复]


ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/department/add1",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    name:"测试"
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```


返回值：

正确：

{"code":200,"data":{"status":"success","error":"success"}}

错误：

* 错误信息在返回之中有说明，直接展示data.error即可

