# minecraft_server

``` Shell
docker build --pull --rm -f "Dockerfile" -t minecraft_server:latest "."
docker compose -f "stack\docker-compose.yaml" up -d --build
```
