# railway-docker

Minimal Node.js web app configured for deployment on [Railway](https://railway.app) using Docker.

## Stack

- **Node.js 24** (LTS)
- **Express 5**
- **Alpine Linux 3.23**

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| GET | `/` | Hello response |
| GET | `/health` | Health check |

## Local development

```bash
npm install
npm run dev
```

## Docker

```bash
docker build -t railway-docker-app .
docker run -p 3000:3000 railway-docker-app
```

## Deploy to Railway

```bash
railway login
railway init
railway up
```

Railway injects `PORT` automatically at runtime.
