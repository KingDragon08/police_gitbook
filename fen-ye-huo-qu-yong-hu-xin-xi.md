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

{"code":200,"data":{"status":"success","data":[{"Id":19,"name":"zhanghao","sex":"M","company":"hongke","NO":"011111","mobile":"13200000000","lastLoginTime":"1511679815380","lastLoginIP":"0.0.0.0","role_name":"测试角"},{"Id":17,"name":"chendi","sex":"M","company":"hongke","NO":"011111","mobile":"12345678901","lastLoginTime":"1511683504824","lastLoginIP":"0.0.0.0","role_name":"测试角"},{"Id":16,"name":"Baymay","sex":"W","company":"car","NO":"000006","mobile":"18300000000","lastLoginTime":"1511347262803","lastLoginIP":"0.0.0.0","role_name":"测试角"},{"Id":15,"name":"text","sex":"M","company":"text","NO":"000003","mobile":"13322221111","lastLoginTime":"1510898162359","lastLoginIP":"0.0.0.0","role_name":"测试角"},{"Id":14,"name":"aa","sex":"M","company":"text","NO":"000003","mobile":"13300006666","lastLoginTime":"1507360888332","lastLoginIP":"1.2.3.4","role_name":"测试角"},{"Id":13,"name":"text","sex":"M","company":"text","NO":"000003","mobile":"13300001111","lastLoginTime":"1511682502882","lastLoginIP":"0.0.0.0","role_name":"测试角"},{"Id":12,"name":"aa","sex":"M","company":"text","NO":"000003","mobile":"13300003333","lastLoginTime":"1511681032182","lastLoginIP":"0.0.0.0","role_name":"测试角"},{"Id":11,"name":"admin3","sex":"M","company":"西城公安局分局","NO":"123456","mobile":"17600166021","lastLoginTime":"1506395517796","lastLoginIP":"0.0.0.0","role_name":"测试角"},{"Id":10,"name":"UNKNOWN","sex":"M","company":"west","NO":"123456","mobile":"00000000000","lastLoginTime":"1505915542486","lastLoginIP":null,"role_name":"测试"},{"Id":9,"name":"1","sex":"M","company":"1","NO":"123456","mobile":"1","lastLoginTime":"1505915522121","lastLoginIP":null,"role_name":"测试"},{"Id":8,"name":"a","sex":"M","company":"a","NO":"123456","mobile":"13227259629","lastLoginTime":"1505808526943","lastLoginIP":"0.0.0.0","role_name":"测试"},{"Id":7,"name":"UNKNOWN","sex":"M","company":"west","NO":"000000","mobile":"12345678901","lastLoginTime":"1505725195366","lastLoginIP":"0.0.0.0","role_name":"测试"},{"Id":6,"name":"admin","sex":"M","company":"西城公安局","NO":"123456","mobile":"17610891519","lastLoginTime":"1511680932629","lastLoginIP":"0.0.0.0","role_name":"测试"},{"Id":5,"name":"test","sex":"M","company":"police","NO":"1234","mobile":"13810332931","lastLoginTime":"1511351256996","lastLoginIP":"0.0.0.0","role_name":"测试"},{"Id":4,"name":"test","sex":"M","company":"police","NO":"000002","mobile":"13888888880","lastLoginTime":"1511432969400","lastLoginIP":"0.0.0.0","role_name":"测试"},{"Id":3,"name":"test","sex":"M","company":"police","NO":"000002","mobile":"13888888889","lastLoginTime":"1511684079515","lastLoginIP":"0.0.0.0","role_name":"测试"},{"Id":2,"name":"test","sex":"M","company":"police","NO":"000002","mobile":"13888888888","lastLoginTime":"1511399957068","lastLoginIP":"0.0.0.0","role_name":"测试"},{"Id":1,"name":"KingDragon","sex":"M","company":"test","NO":"000001","mobile":"13800000000","lastLoginTime":"1511685826538","lastLoginIP":"0.0.0.0","role_name":"测试"}]}}

错误：

* {"code": 300, "data":{"status":"fail","error":"unkown error"}}参数错误
* {"code":300,"data":{"status":"fail","error":"moblie not match password"}}密码和手机号不匹配

新增：

* 返回值中新增role_name字段


