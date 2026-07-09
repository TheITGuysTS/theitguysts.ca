# GitHub Pages Setup

Use these steps after uploading this project to the `TheITGuysTS/theitguysts.ca` GitHub repository.

## 1. Upload files

Upload the project files to the repository root. The repository should contain `package.json`, `astro.config.mjs`, `src/`, `public/`, and `.github/` at the top level.

## 2. Enable GitHub Actions deployment

In GitHub:

1. Open the repository.
2. Go to **Settings**.
3. Go to **Pages**.
4. Under **Build and deployment**, set **Source** to **GitHub Actions**.

The included workflow at `.github/workflows/deploy.yml` will build and deploy the site when changes are pushed to `main`.

## 3. Custom domain

In GitHub Pages settings, set the custom domain to:

```text
theitguysts.ca
```

The project also includes `public/CNAME`, which preserves this setting during deployment.

## 4. Cloudflare DNS records for GitHub Pages

Create these DNS records in Cloudflare if they are not already present:

```text
Type: A
Name: @
Content: 185.199.108.153
Proxy status: DNS only

Type: A
Name: @
Content: 185.199.109.153
Proxy status: DNS only

Type: A
Name: @
Content: 185.199.110.153
Proxy status: DNS only

Type: A
Name: @
Content: 185.199.111.153
Proxy status: DNS only

Type: CNAME
Name: www
Content: TheITGuysTS.github.io
Proxy status: DNS only
```

Keep email records unchanged.

## 5. HTTPS

After GitHub verifies the domain, enable **Enforce HTTPS** in GitHub Pages settings.
