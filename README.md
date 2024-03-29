# CORS Proxy with Websockets and SSL

[![No Maintenance Intended](http://unmaintained.tech/badge.svg)](http://unmaintained.tech/)

## Generate certificates

### MKCert

```bash
mkcert -install # Set CA to trusted store
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

## Chrome/Chromium launch option

You'll need to set `--disable-web-security` flag when launching your Chrome/Chromium browser

## Known limitations

### TUS

This proxy is not compatible with TUS protocol since OPTIONS responses are hardcoded within the proxy.

## Possible improvments

See https://github.com/justsml/ssl-proxy
