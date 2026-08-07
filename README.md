# Pi-hole for LazyCat

LazyCat LPK v2 packaging for Pi-hole `2026.07.2`.

The runtime image is delivered through `docker.1ms.run`. This package exposes only the Pi-hole web UI. It deliberately does not expose DNS or DHCP because LazyCat reserves port 53.

GitHub Actions checks upstream Pi-hole releases daily, builds a versioned LPK Release Asset, and publishes it only to the MiaoMiao store. Configure these repository secrets before enabling publication:

- `APPSTORE_URL`
- `APPSTORE_TOKEN`
- `APP_ID` (optional)
- `PRIVATE_STORE_GROUP_CODES` (optional)
