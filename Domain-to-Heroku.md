# Pointing the domain to Heroku

## Overview

* Using Google Domains to manage the domain
* Using CloudFlare to manage the DNS records
* Using Heroku to host

Purchase or transfer the domain via [Google Domains](https://domains.google/).

Create a [CloudFlare](https://www.cloudflare.com/) account.

## Set CloudFlare to manage your DNS settings

Choose "Add Site" on Cloudflare and pick the appropriate plan (Free is fine).

You don't need to transfer any DNS records over (ignore the warning that A, AAAA, and CNAME records were not found).

On Google Domains, choose "Manage" for the appropriate domain and select "DNS" on the left menu.

Click "Use custom name servers" and use the two name servers that CloudFlare. Note that this can take up to 48 hours, especially if you've just registered your domain.

Turn on "Always use HTTPS" on CloudFlare.

## Setting up the DNS records

[Add a custom domain name for your Heroku app](https://devcenter.heroku.com/articles/custom-domains).

You can read more on configuring Heroku and Cloudflare over HTTPS [here](https://support.cloudflare.com/hc/en-us/articles/205893698-Configure-Cloudflare-and-Heroku-over-HTTPS).

### Root Domain

```
# Add the root domain
heroku domains:add example.com
```

Be sure to look at the output and look for the line that starts with: `Configure your app's DNS provider to point to the DNS Target`

Copy the DNS target and add a CNAME record on CloudFlare using that target in the `IPv4` text box. Point this at the root domain (enter `@` in the `Name` box).

### Add the `www` subdomain

```
heroku domains:add www.example.com
```

Follow the same steps above to create a CNAME record on CloudFlare for the `www` subdomain.

You also might want to add the `www` subdomain.
