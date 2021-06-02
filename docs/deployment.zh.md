## 将你的 Running Page 部署到不同平台中

### Linux 服务器

推荐系统： Ubuntu 20.04 LTS

必要组件：

- Nginx 或者其他 Web 服务器；
- Python 环境 （推荐使用Anaconda）；
- Nodejs (14) 和 Yarn (1.22.10 stable)；

步骤：

1. 把域名指向你的服务器 IP；
2. 在 Nginx 中设定网站目录为 `/public` 文件夹；
3. 用 Anaconda 创建一个属于 Running Page 的环境；
4. 严格遵循`安装` 部分的指导；
5. 完成。赶快享用你的 Running Page 吧！

### Github Pages

1. 如果你在部署到 GitHub Pages 时想要使用自定义域名， 打开这个文件 [/.github/workflows/gh-pages.yml](https://github.com/yihong0618/running_page/blob/master/.github/workflows/gh-pages.yml) ，把 `fqdn` 改成你自己的域名；

2. 更改 `gatsby-config.js` 文件内容， 把 `pathPrefix` 更改为你的 Running Page 所在的域名后缀URL。

   例如：假如你的仓库名称为 `running_page` , 那么此仓库的 Github Pages 的域名就是 https://{yourname}.github.io/running_page，此时 `pathprefix` 的值就应该是 `/running_page`。

3. 更改 [`run_data_sync.yml`](https://github.com/yihong0618/running_page/blob/master/.github/workflows/run_data_sync.yml) 中的变量值：
  1. 把 `env` 改成你自己使用的数据源和信息；
    ![image](https://user-images.githubusercontent.com/15976103/94450124-73f98800-01df-11eb-9b3c-ac1a6224f46f.png)
  2. 在仓库的 Settings > Secrets 中把你自己的 secret 加上 （只加你用到的）；
    ![image](https://user-images.githubusercontent.com/15976103/94450295-aacf9e00-01df-11eb-80b7-a92b9cd1461e.png)
    比如我的是下面这样：
    ![image](https://user-images.githubusercontent.com/15976103/94451037-8922e680-01e0-11eb-9bb9-729f0eadcdb7.png)
  3. 把自己的 [GitHub secret](https://github.com/settings/tokens) 同样也加进去，注意名称保持一致；
    ![image](https://user-images.githubusercontent.com/15976103/94450721-2f222100-01e0-11eb-94a7-ef1f06fc0a59.png)

4. 前往仓库的 `Actions -> Workflows -> All Workflows`, 运行 `Data Sync` ；

5. 运行结束后，在左侧菜单中选择 `Publish GitHub Pages` , 点击 `Run workflow`。确保运行无误，此时 `gh-pages` 分支就创建好了；

6. 前往仓库的 `Settings -> GitHub Pages -> Source`, 选择 `Branch: gh-pages`， 点击`Save`。 一切完成，享受跑步吧！

### Vercel

1. 把 Vercel 连接到你的仓库；
![image](https://user-images.githubusercontent.com/15976103/94452465-2599b880-01e2-11eb-9538-582f0f46c421.png)

2. 导入仓库；
![image](https://user-images.githubusercontent.com/15976103/94452556-3f3b0000-01e2-11eb-97a2-3789c2d60766.png)

3. 等待部署结束；
4. 完成！享受跑步吧！

### Cloudflare Pages

1. 在 `Pages` 中点击 `Create a project` 连接到你的仓库；
2. 点击 `Begin setup` 之后，更改项目的 `Build settings`；
3. 选择 `Framework preset` 为 `Gatsby`;
4. 下滑，选择 `Environment variables`, 输入以下信息；
   > Variable name = `PYTHON_VERSION`, Value = `3.7`
5. 点击 `Save and Deploy`。
