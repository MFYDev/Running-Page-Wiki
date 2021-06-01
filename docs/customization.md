## Customize Parameters 

## `/gatsby-config.js`

### Site Title and Link

Find the following content, and change it to what you want.

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

You can add more links, just like the above.

## `/src/utils/const.js`

### Language

Switch between Chinese and English by modifying `IS_CHINESE` (`true` or `false`) parameter.

### Mapbox Token

> Suggested changing to your own [Mapbox token](https://www.mapbox.com/)

```javascript
const MAPBOX_TOKEN = 'Your Own Mapbox Token';
```
