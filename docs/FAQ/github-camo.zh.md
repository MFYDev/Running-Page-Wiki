## 为什么 Github 引用时显示我的 SVG 图像已损坏，而原图片是好的？

请参考 GIthub 官方文档 [About anonymized URLs - GitHub Docs](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/about-anonymized-urls)

如果源文件是好的，你可以通过运行下列命令来[清除 GIthub Camo 对此图片的缓存](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/about-anonymized-urls#removing-an-image-from-camos-cache) ：

```bash
$ curl -X PURGE https://camo.githubusercontent.com/4d04abe0044d94fefcf9af2133223....
> {"status": "ok", "id": "216-8675309-1008701"}
```



