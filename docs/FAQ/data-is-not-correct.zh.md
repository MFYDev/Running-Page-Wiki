## 为什么显示的数据不是我自己的？

相关 Issues：

- [为什么部署成功之后，本年数据是我自己，total里展示的数据是yihong的呢？我用的keep · Issue #132 · yihong0618/running_page (github.com)](https://github.com/yihong0618/running_page/issues/132)
- [本地运行的时候，获取Nike run club的数据的时候，会夹杂着别的人的数据 · Issue #131 · yihong0618/running_page (github.com)](https://github.com/yihong0618/running_page/issues/131)
- [你好，部署到 GitHub Pages的，有些配置的环境变量没有解析出来，是什么地方配置有问题吗？ · Issue #133 · yihong0618/running_page](https://github.com/yihong0618/running_page/issues/133)

回答：

最快的解决方法是删除 `/scripts/data.db` & `/src/static/activities.json`，然后重新运行同步数据。

如果像 issue [#133](https://github.com/yihong0618/running_page/issues/133) 那样， 在使用 Github Pages 发布之前，您需要确保根据`部署`部分的指示正确设置了变量并运行数据同步时没有错误。

