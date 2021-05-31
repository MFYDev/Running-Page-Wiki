## How can I convert the Running Page's SVG to PNG?

You can use `inkscape`

Install `inkscape`

```bash
sudo add-apt-repository ppa:inkscape.dev/stable
sudo apt-get update
sudo apt install inkscape
```

Then run commands like this:

```bash
inkscape -w `num` -h `num` /path/to/your/svg -o /output/path/of/the/png
```

 For more information about how to use `inkscape`, please refer to:

[Learn | Inkscape](https://inkscape.org/learn/)

