# jmpar.com

Support and privacy pages for the jmpar iOS apps, served by GitHub Pages at https://jmpar.com.
Plain HTML and one shared `style.css`; no build step and no third-party scripts, fonts or CDNs.

## Pages

| URL | File | Used for |
|---|---|---|
| https://jmpar.com/ | `index.html` | App list |
| https://jmpar.com/radio-spectrum/ | `radio-spectrum/index.html` | App Store Support URL |
| https://jmpar.com/radio-spectrum/privacy/ | `radio-spectrum/privacy/index.html` | App Store Privacy Policy URL |

Add each new app as `<app>/index.html` and `<app>/privacy/index.html`, plus a card on the home page.
A privacy page must match what the app actually does, so update it if an app starts using the
network, location, analytics or stored data.

## Hosting

- Repo must be public (GitHub Free only serves Pages from public repos).
- Settings → Pages: deploy from branch `main`, folder `/ (root)`. Custom domain `jmpar.com`
  (the `CNAME` file sets it), Enforce HTTPS on.
- Domain registered at Cloudflare. DNS records, all set to **DNS only** (grey cloud):
  - `A` `jmpar.com` → 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
  - `AAAA` `jmpar.com` → 2606:50c0:8000::153, 2606:50c0:8001::153, 2606:50c0:8002::153, 2606:50c0:8003::153
  - `CNAME` `www` → `mikep63.github.io`
- Domain verified under GitHub profile Settings → Pages, so no one else can claim it.
- Email: Cloudflare Email Routing forwards support@jmpar.com to a personal inbox.
