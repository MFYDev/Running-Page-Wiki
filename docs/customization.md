## Customize Parameters 

## `/gatsby-config.js`

### Site Title and Link

Find the following content, and change it to what you want.

```javascript
siteMetadata: {
  title: 'Running page',
  siteUrl: 'https://mfydev.run',
  description: 'MFYDev Running Page',
},
```

## `/src/utils/const.js`

### Language

Switch between Chinese and English by modifying `IS_CHINESE` (`true` or `false`) parameter.

### Mapbox Token

> Suggested changing to your own [Mapbox token](https://www.mapbox.com/)

```javascript
const MAPBOX_TOKEN = 'Your Own Mapbox Token';
```

### Avatar

Modify `export const AVATAR = 'Your Avatar link';`

Replace it with the image link you want.

### NAV Bar

Change `NAVS`  to the links you want, just like:

```javascript
export const NAVS = [
  { text: 'Running', link: 'https://mfydev.run' },
  { text: 'About', link: 'https://github.com/mfydev' },
];
```

You can add more links, just like the above.
