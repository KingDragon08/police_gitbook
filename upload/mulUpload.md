name：多文件上传

url：/file/mulUpload

method：post

params：

* mobile=&gt;手机号码
* token=&gt;登录后返回的token
* file0=&gt;第一个文件
* filen=&gt;第n个文件

返回值：

正确：

{"code":200,"data":{"status":"success","error":"upload success","urls":["http://www.xiaofen809.com:8080/upload/1506658845134.jpg","http://www.xiaofen809.com:8080/upload/1506658845135.jpg"]}}

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
        <p>上传文件：
            <input type="file" name="file" id="file" multiple="multiple" />
    </form>
    <button onclick="go()">TESTTEST</button>
    <script src="https://apps.bdimg.com/libs/jquery/2.1.4/jquery.min.js"></script>
    <script type="text/javascript">
    function go() {
        var formData = new FormData();
        formData.append("mobile","13810332931");
        formData.append("token","3d9db3d7a0c3c4ef547422817d396a44")
        for(var k=0;k<document.getElementById("file").files.length;k++)
        {
          formData.append("file"+k, document.getElementById("file").files[k]);//第一个参数是文件实例名，可以再后台作为files的引用来遍历所有文件,第二个是文件实例
        }
        $.ajax({
            url: 'http://localhost:8080/file/mulUpload',
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



