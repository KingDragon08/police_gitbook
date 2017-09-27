name：判断用户是否拥有指定权限

url：/user/checkUserPermission

method：post

params：

* mobile=&gt;手机号码
* password=&gt;密码明文
* permission=&gt;permission名字

返回值：

正确：

* {"code":200,"data":{"start":"success","data":1}} 拥有权限
* {"code":200,"data":{"start":"success","data":0}} 不拥有权限

错误：

* {"code":300,"data":{"status":"fail","error":"error params"}}参数错误
* {"code":300,"data":{"status":"fail","error":"moblie not match password"}}密码和手机号不匹配

备注（现支持的权限名称）：
* getUserInfo：获取PC用户信息
* editUserInfo：增删PC用户信息
* getAppUserInfo：获取App用户信息
* editAppUserInfo：增删App用户信息
* getCameraInfo：获取摄像头信息
* editCameraInfo：增删摄像头信息
* getInterestPoint：获取兴趣点信息
* editInterestPoint：增删兴趣点信息
* getCarInfo：获取车辆信息
* editCarInfo：增删车辆信息



