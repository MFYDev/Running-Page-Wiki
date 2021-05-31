## How can I quote the generated SVG pictures in other webistes?

Related Issues:

- [不打包 svg 至 js · Issue #106 · yihong0618/running_page (github.com)](https://github.com/yihong0618/running_page/issues/106)

Due to some reasons, when you build the static websites, the SVG pictures won't be copied to the `/public` folder, which means that if you chose to host Running Page on your own server, it is impossible to quote it.

The Solution is quite simple. You just need to copy them from `/assets` to `/public/static` folder.

You can do it manually, or using one command line.

Example:

```bash
cp -r ./assets/* ./public/static
```

If you are using Github Pages, follow this [feat: add copy svg copy command by Mayandev · Pull Request #130 · yihong0618/running_page (github.com)](https://github.com/yihong0618/running_page/pull/130/commits/f0c0a73fb87d5eda09dbbc7aac85980ea1fc3607) is also a great way.