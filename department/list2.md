name：获取二级部门

url：/department/list2

method：post

params：

* mobile: 手机号
* token: token


ajax：

```
var settings = {
  "url": "http://127.0.0.1:8080/department/list2",
  "method": "POST",
  "data":{
    mobile:"13810332931",
    token:"6b71a6f40f6df25fcb1dbd1456eb1d5b",
    parentId:1
  }
}
$.ajax(settings).done(function (response) {
  console.log(JSON.stringify(response));
});
```


返回值：

正确：

{"code":200,"data":{"status":"success","data":[{"Id":1,"p_id":1,"name":"交警"},{"Id":2,"p_id":1,"name":"测试"}]}}

错误：

* 错误信息在返回之中有说明，直接展示data.error即可

