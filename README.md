# LEDERG VPN configs for v2RayTun (iPhone)

## Recommended: import the VLESS link

Use this link in v2RayTun on iPhone:

```text
vless://dbf3f074-3b18-43f3-b82a-debd8c879c69@216.152.155.189:443?encryption=none&flow=xtls-rprx-vision&security=reality&sni=www.apple.com&fp=chrome&pbk=F5BVp5XkY93lll_Ju34lOIE6A1-dx16_frY6eu9Nzzk&sid=fecf2b55bb11bb0d&spx=%2F&type=tcp#LEDERG-REALITY-Moscow-136ms
```

In v2RayTun, tap **+ → Import from clipboard** (copy the full link first), or open the link on the iPhone. Official deep-link format: `v2raytun://import/{configuration}`.

## Subscription text

`vless.txt` contains one standard VLESS share link on one line. If your version offers **Import from URL**, use:

https://raw.githubusercontent.com/lederg001/lederg-happ-proxy/main/vless.txt

## Xray JSON

`json` and `2raytun.json` are a full, legacy-compatible Xray JSON configuration, using the VLESS `vnext/users` structure and REALITY `publicKey` field. This avoids the newer flattened Xray config form that can be rejected by older iOS cores.

## Moscow TCP check

On 2026-11-11, Check-Host node `ru1.node.check-host.net` (Moscow) opened TCP to `216.152.155.189:443` in **136 ms**:
https://check-host.net/check-report/5721415ck650

This confirms only TCP reachability from that probe. It does not prove a successful VLESS/REALITY handshake or working traffic from your iPhone.

## Security note

This is a third-party public proxy, not a private LEDERG server. Its operator may observe traffic metadata and unencrypted destination traffic. Do not use it for banking, passwords, or sensitive accounts. Public nodes can stop working without notice.
