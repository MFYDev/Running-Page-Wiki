## Why Github displays my SVG images as broken when they are quoted, while the origin is fine?

Please refer to [About anonymized URLs - GitHub Docs](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/about-anonymized-urls)

If the origin is fine, you can [Removing an image from Camo's cache](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/about-anonymized-urls#removing-an-image-from-camos-cache) by running the following command:

```bash
$ curl -X PURGE https://camo.githubusercontent.com/4d04abe0044d94fefcf9af2133223....
> {"status": "ok", "id": "216-8675309-1008701"}
```



