# frigabun

Addon to allow FritzBox routers to update Gandi, Cloudflare and Porkbun DNS entries when obtaining a new IP address.

## Requirements
- A domain name on Gandi, Porkbun or Cloudflare
- Gandi, Porkbun or Cloudflare API credentials
- FritzBox router with up-to-date firmware

## Set up service

- Install addon
- Go to `configuration` tab and set up credentials for the registrars you want to use and set `enabled` to `true`

## Obtaining credentials

### Gandi

- Obtain Gandi API credentials: 
  - Go to [Account settings](https://account.gandi.net/en)
  - Choose Authentication options 
  - Generate an API key on the bottom of the page

### Porkbun

- Obtain Porkbun API credentials as per [this article](https://kb.porkbun.com/article/190-getting-started-with-the-porkbun-api):
  - Go to your [account settings](https://porkbun.com/account/api)
  - Create an API key, note down API key and API secret key
  - Go to [domain management](https://porkbun.com/account/domains)
  - Expand the details of your domain and enable the API access toggle on every domain you want to manage via frigabun

### Cloudflare

- Get your `zoneId` as per [this article](https://developers.cloudflare.com/fundamentals/setup/find-account-and-zone-ids/)
- Create an API token on [this page](https://dash.cloudflare.com/profile/api-tokens)
  - Make sure to set `Zone.DNS` permissions and set it to the zone your domain is in

## FritzBox Setup
- Log into your FritzBox
- Navigate to `Internet` -> `Permit Access` -> `DynDNS`
- Enable DynDNS and use `User-defined` as Provider
- Enter the following URL: `http://{HOST}:{PORT}/api/update?domain={DOMAIN}&subdomain={SUBDOMAIN}&ip=<ipaddr>&registrar=<username>`
  - Replace the `{HOST}` and `{PORT}` with your deployment of the application
    - By default, the application uses port `9595`, and the IP should be your HA host
  - Replace `{DOMAIN}` with your base domain
    - e.g. `yourdomain.com`
  - Replace `{SUBDOMAIN}` with your subdomain or comma separated subdomains
    - e.g. `subdomain` or `sudomain1,subdomain2`
- Enter the full domain in the `Domain Name` field
  - e.g. `subdomain.domain.com` (if you use multiple subdomains, just choose any of those)
- Enter the registrar name in the `Username` field, either `gandi`, `cloudflare` or `porkbun`
- Enter any value in the `Password` field
  - Unused, but required by the FritzBox interface

Your settings should look something like this:

![](https://kore.cc/fritzgandi/fbsettings.png "FritzBox DynDNS Settings")

Right after you save the settings, your FritzBox will make a request to the application. You should see the following
success message in its log:

![](https://kore.cc/fritzgandi/success-frigabun.png "Success Message")

Your FritzBox will now automatically communicate new IPs to the application. 
