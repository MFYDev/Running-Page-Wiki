## 怎样才能把 Matomo 的访客分析代码加入到 Running Page?

你可以在这里找到 Gatsby Matomo 插件： [gatsby-plugin-matomo | Gatsby (gatsbyjs.com)](https://www.gatsbyjs.com/plugins/gatsby-plugin-matomo/?=matomo)

这是此插件的 Github 仓库：[kremalicious/gatsby-plugin-matomo: 🥂 Gatsby plugin to add Matomo (formerly Piwik) onto a site. (github.com)](https://github.com/kremalicious/gatsby-plugin-matomo)

根据 `Usage` 的指引，你需要在 Running Page 根目录中安装此插件：

```bash
cd yourproject/
npm i gatsby-plugin-matomo
```

然后在 `/gatsby-config.js` 中加载此插件并添加必要信息：

!!! 警告
	您应该将这些代码添加到 `plugins` 的末尾。 如果需要，请不要忘记添加逗号。

```bash
plugins: [
  {
    resolve: 'gatsby-plugin-matomo',
    options: {
      siteId: 'YOUR_SITE_ID',
      matomoUrl: 'https://YOUR_MATOMO_URL.COM',
      siteUrl: 'https://YOUR_LIVE_SITE_URL.COM'
    }
  }
]
```

 	