## Generate SVG Total Data Display

### Display Demo Preview：

- [{Your Name} Running](https://mfydev.run/static/github.svg)
- [{Your Name} Running  in Every Year](https://mfydev.run/static/github_2021.svg)
- [Over {Num}KM Running](https://mfydev.run/static/grid.svg)
- [Year Circular SVG](https://mfydev.run/static/year_2021.svg)

### Generate `{Your Name} Running` SVG

```
python scripts/gen_svg.py --from-db --title "${{ env.TITLE }}" --type github --athlete "${{ env.ATHLETE }}" --special-distance 10 --special-distance2 20 --special-color yellow --special-color2 red --output assets/github.svg --use-localtime --min-distance 0.5
```

### Generate  Every Year's `{Your Name} Running` SVG 

```python
python scripts/gen_svg.py --from-db --year $(date +"%Y") --title "$(date +"%Y") Running" --type github --athlete "${{ env.ATHLETE }}" --special-distance 10 --special-distance2 20 --special-color yellow --special-color2 red --output assets/github_$(date +"%Y").svg --use-localtime --min-distance 0.5
```

### Generate `Over {Num}KM Running` SVG

```
python scripts/gen_svg.py --from-db --title "${{ env.TITLE_GRID }}" --type grid --athlete "${{ env.ATHLETE }}"  --output assets/grid.svg --min-distance 10.0 --special-color yellow --special-color2 red --special-distance 20 --special-distance2 40 --use-localtime
```
### Generate Year Circular SVG
```
python3(python) scripts/gen_svg.py --from-db --type circular --use-localtime
```

For more display effects, please refer to:     
https://github.com/flopp/GpxTrackPoster