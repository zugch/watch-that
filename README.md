# watch-that
## create image
```
docker build -t watch-that .
```
## run container (example)
```
docker run --rm -e SCRAPE_URL="https://example.com" -e ELEMENT_SELECTOR="h1" -e CRON_EXPRESSION="*/1 * * * *" watch-that
```
