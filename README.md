# LinkMe Domain Connect

Domain Connect templates and onboarding assets for LinkMe.

## Templates

- `li-nk.me.custom-domain-cname.json`: Adds a CNAME for a customer subdomain to the LinkMe CNAME target.

## Validation

Validate with the official linter:

```bash
go install github.com/Domain-Connect/dc-template-linter@latest
"$(go env GOPATH)/bin/dc-template-linter" -cloudflare ./li-nk.me.custom-domain-cname.json
```

## Security

This repository is public and must not contain private keys or other secrets.
The signing private key is stored only in LinkMe server environment variables.
