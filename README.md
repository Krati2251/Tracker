# Frontend Docker Run

This frontend is a static site served using Nginx.

## Build image

```bash
docker build -t finance-frontend .
```

## Run container

```bash
docker run --rm -d -p 8080:80 --name finance-frontend finance-frontend
```

Open in browser:

- http://localhost:8080

## Stop container

```bash
docker stop finance-frontend
```
