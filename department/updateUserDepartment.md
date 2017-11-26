name：更新用户的部门信息

url：/department/updateDepartment

method：post

params：

* mobile: 当前登陆用户的手机号
* token: 当前登陆用户的token
* targetUserId: 要更改部门的用户Id
* targetDepartmentId: 更改为二级部门的Id


ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/department/updateDepartment",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    targetUserId: 1,
    targetDepartmentId: 2

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

