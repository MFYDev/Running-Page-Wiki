## 同步你自己的 Nike Run Club 数据

!!! warning
	**当你选择在自己的服务器上部署 Running Page 时，由于 Nike 封锁了部分 IDC 的 IP 频段，您的服务器可能无法正确同步 Nike Run Club 的数据并显示 `403 error`，此时你便不能选择使用此服务器部署。**
	
获取 Nike 的 `refresh_token`

1. 登录 [Nike](https://www.nike.com) 官网
2. 在 Develop -> Application-> Storage -> https:unite.nike.com 中寻找 `refresh_token` 
![image](https://user-images.githubusercontent.com/15976103/94448123-23812b00-01dd-11eb-8143-4b0839c31d90.png)
3. 在 Running Page 根目录运行以下命令：

    ```python
    python3(python) scripts/nike_sync.py ${nike refresh_token}
    ```

    例如：

    ```python
    python3(python) scripts/nike_sync.py eyJhbGciThiMTItNGIw******
    ```

    ![example img](https://raw.githubusercontent.com/shaonianche/gallery/master/running_page/nike_sync_%20example.png)