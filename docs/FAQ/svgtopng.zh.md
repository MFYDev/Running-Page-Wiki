## 我怎么才能把 Running Page 的 SVG 转换成 PNG？

你可以使用 `inkscape` 

安装 `inkscape` ：

```bash
sudo add-apt-repository ppa:inkscape.dev/stable
sudo apt-get update
sudo apt install inkscape
```

然后像下面这样运行指令：

```bash
inkscape -w `num` -h `num` /path/to/your/svg -o /output/path/of/the/png
```

关于如何使用 `inkscape` 的更多信息，请参考：

[Learn | Inkscape](https://inkscape.org/learn/)

