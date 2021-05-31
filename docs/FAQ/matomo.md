## How to add Matomo Analytics code to the header of Running Page?

You can find Gatsby Matomo Plugin here: [gatsby-plugin-matomo | Gatsby (gatsbyjs.com)](https://www.gatsbyjs.com/plugins/gatsby-plugin-matomo/?=matomo)

Here is the Github Repo of this plugin: [kremalicious/gatsby-plugin-matomo: 🥂 Gatsby plugin to add Matomo (formerly Piwik) onto a site. (github.com)](https://github.com/kremalicious/gatsby-plugin-matomo)

According to the `Usage` section, you should install this plugin to your project's root:

```bash
cd yourproject/
npm i gatsby-plugin-matomo
```

 Then load the plugin from `/gatsby-config.js` and set the required variables:
 
!!! warning
	You should add these code to the end of the `plugins` block. Please do not forget to add comma if you need.
 
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

 	