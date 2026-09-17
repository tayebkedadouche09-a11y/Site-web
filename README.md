# NUMI V1

Cinematic digital showroom for finished website systems.

This repository was bootstrapped from the NUMI V1 project. The final hardening pass adds repository-local cinematic assets, product gallery/FAQ presentation, and a self-contained visual layer instead of relying on WebDev/Manus storage for storefront media.

## External configuration still required

- Stripe: `STRIPE_SECRET_KEY`, `VITE_STRIPE_PUBLISHABLE_KEY`, `STRIPE_WEBHOOK_SECRET`, `PUBLIC_APP_URL`
- Automatic customer provisioning: `PROVISIONING_API_URL`, `PROVISIONING_API_KEY`
- Real product demo URLs must be configured per product; the UI never fabricates a live demo.

## Validation

Run:

```bash
pnpm install --frozen-lockfile
pnpm check
pnpm test
pnpm build
```

The uploaded source snapshot was already validated in its original environment before this portability hardening. The current container does not have pnpm/dependencies installed, so a fresh dependency install is required before local CI commands can be rerun here.
