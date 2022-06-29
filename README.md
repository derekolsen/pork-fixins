# pork-fixins
Simple Porkbun dynamic DNS intended for use in home servers.

Currently, this script only updates an existing 'A' record.
In the future, this will be expanded to automatically create
missing records.

By default, `pork-fixins` keeps files nearby in `pbhosts`
to detect when your ISP changes your public IP address.

## Requirements
- bash
- curl
- jq

## About
```
Usage:  pork-fixins [OPTIONS] FQDN

Options:
  -v, --verbose   
  -f, --json      Keyfile [pb_keys.json]
  -H, --hosts     Directory of host files [pbhosts]
  -t, --ttl       Time-To-Live (TTL) [600]
  -V, --version
  -h, --help

The FQDN must only include one subdomain,
a second-level domain (SLD), and
a top-level domain (TLD), i.e. `www.example.com`

The keyfile should be JSON:

  {
    "secretapikey": "YOUR_SECRET_API_KEY",
    "apikey": "YOUR_API_KEY"
  }
```
