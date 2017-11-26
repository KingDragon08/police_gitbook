name：编辑一级部门名字

url：/department/eidt1

method：post

params：

* mobile: 手机号
* token: token
* Id: 一级部门的Id
* name: 一级部门的新名字


ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/department/edit1",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    Id: 1,
    name: 'new name'

  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```


返回值：

正确：

{"code":200,"data":{"status":"success","data":[{"Id":1,"name":"西城公安局"},{"Id":2,"name":"测试"},{"Id":3,"name":"测试1"}]}}

错误：

* 错误信息在返回之中有说明，直接展示data.error即可

