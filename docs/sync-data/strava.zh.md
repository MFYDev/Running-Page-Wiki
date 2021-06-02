## 同步你自己的 Strava 数据

1. 登录到 [Strava](https://www.strava.com/) ;
2. 访问 [Strava Developers](http://developers.strava.com) -> [Create & Manage Your App](https://strava.com/settings/api)
3. 创建 `My API Application`： 输入所需信息

	!!! warning
		红框中的是必填项。 并且 `Authorization Callback Domain` 必须是 `localhost` 。
	![My API Application](https://raw.githubusercontent.com/shaonianche/gallery/master/running_page/strava_settings_api.png)
	创建成功如下图所示：
	![](https://raw.githubusercontent.com/shaonianche/gallery/master/running_page/created_successfully_1.png)

4. 使用下面的链接来获得请求权限： 把链接中的 `${your_id}` 换成你自己的 `My API Application` Client ID 
```
https://www.strava.com/oauth/authorize?client_id=${your_id}&response_type=code&redirect_uri=http://localhost/exchange_token&approval_prompt=force&scope=read_all,profile:read_all,activity:read_all,profile:write,activity:write
```
![get_all_permissions](https://raw.githubusercontent.com/shaonianche/gallery/master/running_page/get_all_permissions.png)

5. 在以下链接中得到 `code` 值；
例如：
```
http://localhost/exchange_token?state=&code=1dab37edd9970971fb502c9efdd087f4f3471e6e&scope=read,activity:write,activity:read_all,profile:write,profile:read_all,read_all
```
`code` 值是：

```
1dab37edd9970971fb502c9efdd087f4f3471e6
```
![get_code](https://raw.githubusercontent.com/shaonianche/gallery/master/running_page/get_code.png)

6. 使用 `Client_id`、`Client_secret`、`Code` 获得 `refresch_token`：在你的终端中运行下列命令
```
curl -X POST https://www.strava.com/oauth/token \
-F client_id=${Your Client ID} \
-F client_secret=${Your Client Secret} \
-F code=${Your Code} \
-F grant_type=authorization_code
```
例如：
```
curl -X POST https://www.strava.com/oauth/token \
-F client_id=12345 \
-F client_secret=b21******d0bfb377998ed1ac3b0 \
-F code=d09******b58abface48003 \
-F grant_type=authorization_code
```
![get_refresch_token](https://raw.githubusercontent.com/shaonianche/gallery/master/running_page/get_refresch_token.png)

7. 同步 `Strava` 数据
```python
python3(python) scripts/strava_sync.py ${client_id} ${client_secret} ${refresch_token}
```
## 参考
https://developers.strava.com/docs/getting-started   
https://github.com/barrald/strava-uploader   
https://github.com/strava/go.strava  