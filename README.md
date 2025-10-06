# Login Page in Docker (Nginx)

This serves your login/signup HTML with Nginx.

## Build
```bash
docker build -t login-page:latest .
```

## Run (foreground)
```bash
docker run --rm -p 8080:80 login-page:latest
# Open http://localhost:8080
```

## Run (background, recommended)
```bash
docker run -d --name loginapp -p 8080:80 login-page:latest
docker ps
docker logs -f loginapp
docker stop loginapp
```

## Compose
```bash
docker compose up --build
```
