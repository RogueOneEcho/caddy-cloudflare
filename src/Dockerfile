ARG CADDY_VERSION=2.8
ARG CADDY_CLOUDFLARE_VERSION=89f16b99c18ef49c8bb470a82f895bce01cbaece

FROM caddy:${CADDY_VERSION}-builder-alpine AS builder
RUN xcaddy build --with github.com/caddy-dns/cloudflare@${CADDY_CLOUDFLARE_VERSION}

FROM caddy:${CADDY_VERSION}-alpine
RUN apk add --no-cache curl
COPY --from=builder /usr/bin/caddy /usr/bin/caddy
COPY Caddyfile /etc/caddy/Caddyfile
