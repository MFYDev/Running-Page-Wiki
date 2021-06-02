## 自定义参数 

## `/gatsby-config.js`

### 网站标题和链接

找到以下内容，并将其更改为您想要的。

```javascript
siteMetadata: {
    siteTitle: 'MFYDev Running',
    siteUrl: 'https://mfydev.run',
    logo: 'https://yourlogo.com',
    description: 'Running Page',
    navLinks: [
      {
        name: 'Name1',
        url: 'Link1',
      },
      {
        name: 'Name2',
        url: 'Link2',
      },
    ],
  },
```

你可以像上方的格式那样添加更多链接。

## `/src/utils/const.js`

### 语言

切换中英文显示，只需要更改 `IS_CHINESE` (`true` or `false`) 参数即可。

### Mapbox Token

> 强烈建议更换为你自己的 [Mapbox token](https://www.mapbox.com/)

```javascript
const MAPBOX_TOKEN = 'Your Own Mapbox Token';
```
