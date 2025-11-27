# EU Proxy

Lightweight nginx reverse proxy for routing requests through an EU-based server.

## Usage

Pass the target URL in the `X-Proxy-Target` header:

```bash
curl -X POST https://your-proxy-domain/ \
  -H "X-Proxy-Target: https://api.example.com/endpoint" \
  -H "Content-Type: application/json" \
  -d '{"key": "value"}'
```

Works with any target URL.

## Deploy

Deploy via Docker:

```bash
docker build -t eu-proxy .
docker run -p 8080:80 eu-proxy
```

Or deploy to any container platform (Coolify, Railway, Fly.io, etc.).
