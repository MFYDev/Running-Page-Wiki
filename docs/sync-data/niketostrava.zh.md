## 将你的 Nike Run Club 数据同步到 Strava

1. 遵循 Nike Run Club 和 Strava 中的指示获得所有必要参数; 
2. 在 Running Page 根目录运行下列命令：
```python
python3(python) scripts/nike_to_strava_sync.py ${nike_refresh_token} ${client_id} ${client_secret} ${strava_refresch_token} 
```
例如：
```python
python3(python) scripts/nike_to_strava_sync.py eyJhbGciThiMTItNGIw******  xxx xxx xxx
```