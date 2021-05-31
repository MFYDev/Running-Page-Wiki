## Why the data displays in the Running Page is not mine?

Related Issues:

- [为什么部署成功之后，本年数据是我自己，total里展示的数据是yihong的呢？我用的keep · Issue #132 · yihong0618/running_page (github.com)](https://github.com/yihong0618/running_page/issues/132)
- [本地运行的时候，获取Nike run club的数据的时候，会夹杂着别的人的数据 · Issue #131 · yihong0618/running_page (github.com)](https://github.com/yihong0618/running_page/issues/131)
- [你好，部署到 GitHub Pages的，有些配置的环境变量没有解析出来，是什么地方配置有问题吗？ · Issue #133 · yihong0618/running_page](https://github.com/yihong0618/running_page/issues/133)

Answer:

When this happens, the fastest way to tackle with this  problem is purging `/scripts/data.db` & `/src/static/activities.json`, then run the data sync again.

If it is like issue [#133](https://github.com/yihong0618/running_page/issues/133), you need to ensure that you have set the variables correctly according to the guide in `Delopyment` and run the data sync workflow with no errors before you publish it with Github Pages.

