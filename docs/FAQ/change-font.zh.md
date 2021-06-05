## 我该如何更改 Running Page 显示的字体？

相关 Issue:

[[feat\] chang the font. · Issue #140 · yihong0618/running_page (github.com)](https://github.com/yihong0618/running_page/issues/140)

回答：

请按照以下步骤进行：

1. 在 `/src/styles` 目录下创建 `fontface.scss` ；
2. 请确保你要替换的字体有一个能够直接在线引用的链接；
3. 使`fontface.scss` 的内容和下面类似，并且替换掉 font link；
	```css
	@font-face {
	font-family: 'IBM Plex Sans';
	src: url(Your Font Link)  format('woff2'),
	url(Your Font Link)  format('woff');
	font-weight: 500;
	font-style: normal;
	}
	```
	请注意： `font-weight` 和 `font-style` 不是必要的，如果你需要再添加。
4. 编辑 `/src/style/variables.scss`:
	1. 把 `@import './fontface.scss';` 添加到第一行；
	2. 把你要用的字体名称加到 `$global-font-family:` 的最前面，像下面这样：
	```css
	@import './fontface.scss';
	$global-font-family: 'Your font name', ibm-plex-sans,'Microsoft YaHei', 'Helvetica Neue', Arial, sans-serif;
	```
5. 把 `@import '../../styles/variables.scss';` 加到 `/src/components/RunMap/style.module.scss` 的第一行， 然后更改 `font-family:` 为 `$global-font-family;`。最后像下面这样：
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
6. 搞定！
