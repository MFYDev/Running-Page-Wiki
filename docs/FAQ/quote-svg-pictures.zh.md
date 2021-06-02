## 如何在其他网站引用生成的SVG图片？

相关 Issues：

- [不打包 svg 至 js · Issue #106 · yihong0618/running_page (github.com)](https://github.com/yihong0618/running_page/issues/106)

由于某些原因，当您构建静态网站时，SVG 图片不会复制到 `/public` 文件夹，这意味着如果您选择在自己的服务器上托管 Running Page，仅仅`build`则无法引用它。

解决方案很简单。 您只需要将它们从 `/assets` 复制到 `/public/static` 文件夹。

您可以手动完成，也可以使用一个命令行。

例如：

```bash
cp -r ./assets/* ./public/static
```

如果你在使用 Github Pages 部署，参考这个 [feat: add copy svg copy command by Mayandev · Pull Request #130 · yihong0618/running_page (github.com)](https://github.com/yihong0618/running_page/pull/130/commits/f0c0a73fb87d5eda09dbbc7aac85980ea1fc3607) 也是一个不错的解决方法。