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

&lt;!DOCTYPE html&gt;

&lt;html&gt;

&lt;head&gt;

    &lt;title&gt;test&lt;/title&gt;

&lt;/head&gt;

&lt;body&gt;

    &lt;form id="uploadForm"&gt;

        &lt;p&gt;指定文件名：

            &lt;input type="text" name="filename" value="" /&gt;

        &lt;/p&gt;

        &lt;p&gt;上传文件：

            &lt;input type="file" name="file" /&gt;

         &lt;/ p&gt;

    &lt;/form&gt;

    &lt;button onclick="go\(\)"&gt;TESTTEST&lt;/button&gt;

    &lt;script src="https://apps.bdimg.com/libs/jquery/2.1.4/jquery.min.js"&gt;&lt;/script&gt;

    &lt;script type="text/javascript"&gt;

    function go\(\) {

        var formData = new FormData\($\("\#uploadForm"\)\[0\]\);

        $.ajax\({

            url: 'http://www.xiaofen809.com:8080/file/upload',

            type: 'POST',

            data: formData,

            async: false,

            cache: false,

            contentType: false,

            processData: false,

            success: function\(data\) {

                console.log\(JSON.stringify\(data\)\);

            },

            error: function\(data\) {

                console.log\(data\);

            }

        }\);

    }

    &lt;/script&gt;

&lt;/body&gt;



&lt;/html&gt;

