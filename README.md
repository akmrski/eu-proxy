# Universal Proxy

Simple nginx reverse proxy for requests from Bulgarian IP.

## Usage

Pass the target URL in the `X-Proxy-Target` header:

```bash
curl -X POST https://your-proxy-domain/ \
  -H "X-Proxy-Target: https://api.speedy.bg/v1/client/contract/" \
  -H "Content-Type: application/json" \
  -d '{"userName": "...", "password": "..."}'
```

Works with any target URL - just set the header.
