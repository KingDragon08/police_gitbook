name：单个文件上传

url：/file/upload

method：post

params：

* mobile=&gt;手机号码
* token=&gt;登录后返回的token
* file=&gt;文件

返回值：

正确：

{ "code": 200, "data": { "status": "success", "error": "upload success", "url": url } }

错误：

* {"code":300,"data":{"status":"fail","error":"unknown error"}}上传失败
* {"code":300,"data":{"status":"fail","error":"moblie not match password"}}密码和手机号不匹配

事例 ：

```js
<!DOCTYPE html>
<html>

<head>
    <title>test</title>
</head>

<body>
    <form id="uploadForm">
        <p>指定文件名：
            <input type="text" name="filename" value="" />
        </p>
        <p>上传文件：
            <input type="file" name="file" />
        </ p>
            <input type="hidden" name="mobile" value="" />
            <input type="hidden" name="token" value="" />
    </form>
    <button onclick="go()">TESTTEST</button>
    <script src="https://apps.bdimg.com/libs/jquery/2.1.4/jquery.min.js"></script>
    <script type="text/javascript">
    function go() {
        var formData = new FormData($("#uploadForm")[0]);
        $.ajax({
            url: 'http://localhost:8080/file/upload',
            type: 'POST',
            data: formData,
            async: false,
            cache: false,
            contentType: false,
            processData: false,
            success: function(data) {
                console.log(JSON.stringify(data));
            },
            error: function(data) {
                console.log(data);
            }
        });
    }
    </script>
</body>

</html>
```



