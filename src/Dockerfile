ARG CADDY_VERSION=2.10
ARG CADDY_CLOUDFLARE_VERSION=v0.2.1

FROM caddy:${CADDY_VERSION}-builder-alpine AS builder
RUN xcaddy build --with github.com/caddy-dns/cloudflare@${CADDY_CLOUDFLARE_VERSION}

FROM caddy:${CADDY_VERSION}-alpine
RUN apk add --no-cache curl
COPY --from=builder /usr/bin/caddy /usr/bin/caddy
COPY Caddyfile /etc/caddy/Caddyfile
