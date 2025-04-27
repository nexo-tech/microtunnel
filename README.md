# microtunnel

A simple tunneling solution to expose local services to the internet.

## Configuration

### Server Configuration
```bash
# Required: Domain configuration
export TUNNEL_SERVER_DOMAIN_NAME=
export CADDY_PROXY_PORT=3000
export CF_API_TOKEN=
```

### Examples

```bash
# Server configuration
export TUNNEL_SERVER_DOMAIN_NAME=tunnel.example.com
export CADDY_PROXY_PORT=3000
export CF_API_TOKEN=your_token
```

## Usage

1. Start the server:
```bash
go run main.go --port 3000 --base-domain-name=tunnel.example.com
```

2. Start the client:
```bash
go run main.go --server-url=wss://other-domain.example.com/tunnel --port <local-port>
```

## Features

- Secure WebSocket-based tunneling
- Automatic TLS with Let's Encrypt
- Cloudflare integration for DNS and CDN
- Structured logging for easy debugging
