# LinkMe Domain Connect

Domain Connect templates and onboarding assets for LinkMe.

## Templates

- `li-nk.me.custom-domain-cname.json`: Adds a CNAME for a customer subdomain to the LinkMe CNAME target.

Template signing/public-key resolution:

- `syncPubKeyDomain` is `li-nk.me`
- LinkMe request query uses `key=dcv1` (configurable via `DOMAIN_CONNECT_SYNC_KEY_HOST`)
- Publish TXT for `dcv1.li-nk.me` with the signing public key

## Validation

Validate with the official linter:

```bash
go install github.com/Domain-Connect/dc-template-linter@latest
"$(go env GOPATH)/bin/dc-template-linter" -cloudflare ./li-nk.me.custom-domain-cname.json
```

## Security

This repository is public and must not contain private keys or other secrets.
The signing private key is stored only in LinkMe server environment variables.
