name：分页获取用户信息

url：/user/getUsers

method：post

params：

* mobile=&gt;手机号码
* token=&gt;登录后返回的token串
* page=&gt;页数，从1开始，可不传（默认为1）
* pageSize=&gt;每页数据量，可不传（默认为20）
* type=&gt;用户的类型，1：审核通过的正常用户，0:待审核的用户

返回值：

正确：

{"code":200,"data":{"status":"success","data":\[{"Id":6,"name":"admin","sex":"M","company":"西城公安局","NO":"123456","mobile":"17610891519","lastLoginTime":"1505722458559","lastLoginIP":"0.0.0.0"},{"Id":5,"name":"test","sex":"M","company":"police","NO":"1234","mobile":"13810332931","lastLoginTime":"1505723335875","lastLoginIP":"0.0.0.0"},{"Id":4,"name":"test","sex":"M","company":"police","NO":"000002","mobile":"13888888880","lastLoginTime":"1505717373443","lastLoginIP":null},{"Id":3,"name":"test","sex":"M","company":"police","NO":"000002","mobile":"13888888889","lastLoginTime":"1505717245594","lastLoginIP":null},{"Id":2,"name":"test","sex":"M","company":"police","NO":"000002","mobile":"13888888888","lastLoginTime":"1505715150588","lastLoginIP":null},{"Id":1,"name":"KingDragon","sex":"M","company":"test","NO":"000001","mobile":"13800000000","lastLoginTime":"1505708350858","lastLoginIP":"0.0.0.0"}\]}}

错误：

* {"code": 300, "data":{"status":"fail","error":"unkown error"}}参数错误
* {"code":300,"data":{"status":"fail","error":"moblie not match password"}}密码和手机号不匹配



