# CORS Proxy with Websockets and SSL

## Generate certificates

### MKCert

```bash
mkcert -install
cd certs
mkcert localhost 127.0.0.1 ::1
```

## Set env vars

```bash
cp .envrc.example .envrc
source .envrc # you could also use direnv
```

## Start proxy

```bash
docker compose up
```

You can now point your frontend to [https://localhost:8443/](https://localhost:8443/).
