## How can I change the font of Running Page?

Related Issue:

[[feat\] chang the font. · Issue #140 · yihong0618/running_page (github.com)](https://github.com/yihong0618/running_page/issues/140)

Answer:

Please follow the steps below:

1. Create `fontface.scss` under the `/src/styles` directory;
2. Please make sure the font you want to use have a direct online link;
3. Make the `fontface.scss` content like this and replace the the font link:
	```css
	@font-face {
	font-family: 'IBM Plex Sans';
	src: url(Your Font Link)  format('woff2'),
	url(Your Font Link)  format('woff');
	font-weight: 500;
	font-style: normal;
	}
	```
	Please note: `font-weight` and `font-style` are not necessary, add them if you need.
4. Edit `/src/style/variables.scss`:
	1. Add `@import './fontface.scss';` to line 1;
	2. Add your font name to the front of `$global-font-family:`, the final content is like this:
	```css
	@import './fontface.scss';
	$global-font-family: 'Your font name', ibm-plex-sans,'Microsoft YaHei', 'Helvetica Neue', Arial, sans-serif;
	```
5. Add `@import '../../styles/variables.scss';` to `/src/components/RunMap/style.module.scss`, and change the value of `font-family:` from `sans-serif;` to `$global-font-family;`. Then final content is like this:
	```css
	@import '../../styles/variables.scss';

    .locationSVG {
      height: 100%;
      width:  100%;
      margin: 1rem 0 0;
      border: 0;
      padding: 0;
    }

    .buttons {
      width: 90%;
      margin: 0 auto;
    }

    .button {
      display: inline-block;
      position: relative;
      cursor: pointer;
      width: 10%;
      padding: 10px;
      margin-top: 1px;
      font-size: 10px;
      text-align: center;
      color: write;
      font-family: $global-font-family;
    }

    .runTitle {
      height: 26px;
      width: 710px;
      position: absolute;
      bottom: 0px;
      left: 120px;
      font-family: $global-font-family;
      cursor: pointer;
    }
	```
6. Done! Enjoy!
