# watch-that
## create image
```
docker build -t watch-that -f docker/Dockerfile .
```
## run container (example)
```
docker run --rm -e SCRAPE_URL="https://example.com" -e ELEMENT_SELECTOR="h1" -e CRON_EXPRESSION="*/1 * * * *" watch-that
```
### run container (detached mode and naming)
Flag ```-d``` for detached mode

Name the container with ```--name```
```
docker run --rm -d --name watch-that-1 -e SCRAPE_URL="https://example.com" -e ELEMENT_SELECTOR="h1" -e CRON_EXPRESSION="*/1 * * * *" watch-that
```
Check your running containers with ```ps```
```
docker ps
```
Bring your container back to the front
```
docker attach watch-that-1
```
