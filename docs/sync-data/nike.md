## Get Your Own Nike Run Club Data

!!! warning
	**When you choose to deploy Running Page on your own server, due to Nike has blocked some IDC's IP band, maybe your server cannot sync Nike Run Club's data correctly and display `403 error`, then you have to change another way to host it.**
	
Get Nike's `refresh_token`

1. Log in to  [Nike](https://www.nike.com) website
2. Look for `refresh_token` in Develop -> Application-> Storage -> https:unite.nike.com
![image](https://user-images.githubusercontent.com/15976103/94448123-23812b00-01dd-11eb-8143-4b0839c31d90.png)
3. Execute in the root directory:

    ```python
    python3(python) scripts/nike_sync.py ${nike refresh_token}
    ```

    example：

    ```python
    python3(python) scripts/nike_sync.py eyJhbGciThiMTItNGIw******
    ```

    ![example img](https://raw.githubusercontent.com/shaonianche/gallery/master/running_page/nike_sync_%20example.png)