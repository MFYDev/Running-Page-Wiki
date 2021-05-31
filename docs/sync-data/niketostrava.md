## Sync Your Own Nike Run Club Data to Strava

1. Follow the steps in Nike and Strava; 
2. Execute in the root directory:
```python
python3(python) scripts/nike_to_strava_sync.py ${nike_refresh_token} ${client_id} ${client_secret} ${strava_refresch_token} 
```
example：
```python
python3(python) scripts/nike_to_strava_sync.py eyJhbGciThiMTItNGIw******  xxx xxx xxx
```