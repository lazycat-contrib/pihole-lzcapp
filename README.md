# Pi-hole for LazyCat

LazyCat LPK v2 packaging for Pi-hole `2026.07.2`.

The runtime image is delivered through `docker.1ms.run`. The Pi-hole web UI is exposed through the application domain. DNS is exposed without Host networking on TCP and UDP port `1053`, forwarded to Pi-hole port `53`, because LazyCat reserves host port 53. DHCP is not exposed.

GitHub Actions checks upstream Pi-hole releases daily, builds a versioned LPK Release Asset, and publishes it only to the MiaoMiao store. Configure these repository secrets before enabling publication:

- `APPSTORE_URL`
- `APPSTORE_TOKEN`
- `APP_ID` (optional)
- `PRIVATE_STORE_GROUP_CODES` (optional)
