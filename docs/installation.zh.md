## 下载

Clone 或者 fork 这个仓库。

```
git clone https://github.com/yihong0618/running_page.git
```

## 安装必须组件并测试
```
pip3 install -r requirements.txt
yarn install
yarn develop
```
打开你的浏览器，访问此链接： http://localhost:8000/ 

## 生成静态网站

在后续指南中正确设置所有参数后，你就可以构建静态站点。

```bash
yarn build
```

所有静态网站文件都会在 `/public` 文件夹下。