# <p style="text-align: center">caddy-cloudflare</p>

<p align="center">
  <a href="https://github.com/RogueOneEcho/caddy-cloudflare/actions/workflows/ci-on-push.yml"><img alt="CI status" src="https://img.shields.io/github/actions/workflow/status/RogueOneEcho/caddy-cloudflare/ci-on-push.yml"></a>
  <a href="https://github.com/RogueOneEcho/caddy-cloudflare/releases"><img alt="Latest release" src="https://img.shields.io/github/v/release/RogueOneEcho/caddy-cloudflare"></a>
  <a href="LICENSE.md"><img alt="License" src="https://img.shields.io/github/license/RogueOneEcho/caddy-cloudflare"></a>
</p>

Caddy with the Cloudflare DNS module for automatic TLS.

```bash
docker pull ghcr.io/rogueoneecho/caddy-cloudflare
```

## Features

- Custom Caddy build with [caddy-dns/cloudflare](https://github.com/caddy-dns/cloudflare) module
- Automatic TLS certificates via Cloudflare DNS challenge
- Healthcheck endpoint at `/healthcheck`
- Catch-all 421 response for unmatched hosts

## Build

- amd64 and arm64 images available on [GHCR](https://github.com/RogueOneEcho/caddy-cloudflare/pkgs/container/caddy-cloudflare)
- Signed with [Cosign](https://github.com/sigstore/cosign) via keyless Sigstore OIDC
- SBOM attestation in CycloneDX format
- Vulnerability scanned with [Grype](https://github.com/anchore/grype)

## Usage

See [docker-compose.yml](docker-compose.yml) for an example.

## Releases and Changes

Releases and a full changelog are available via [GitHub Releases](https://github.com/RogueOneEcho/caddy-cloudflare/releases).
