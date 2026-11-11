# LEDERG VPN configs

## 2RayTun

Import `2raytun.json` in 2RayTun using **+ → Import from File**.

The file contains one VLESS + REALITY outbound:
- Server: `216.152.155.189:443`
- Transport: RAW/TCP
- REALITY SNI: `www.apple.com`
- Fingerprint: `chrome`
- Flow: `xtls-rprx-vision`

## Moscow reachability check

On 2026-11-11, Check-Host node `ru1.node.check-host.net` (Moscow) opened TCP to `216.152.155.189:443` in **136 ms**:
https://check-host.net/check-report/5721415ck650

A TCP-open result confirms only that the port accepted a TCP connection from that probe. It does **not** confirm the VLESS/REALITY handshake, authentication, speed under load, or continued uptime. Test the profile in the client before relying on it.

Other public candidates that answered TCP checks used `security=none`; they are intentionally excluded from this primary privacy-oriented profile. One candidate timed out and was excluded.

## Source and caution

The public share URI was taken from the TOP 100 feed of:
https://github.com/0xRadikal/Free-v2ray-Configs

This is a third-party public proxy, not a private LEDERG server. Its operator may be able to observe traffic metadata and, for unencrypted destination traffic, content. Do not use it for banking, passwords, or sensitive accounts. Public nodes can disappear or change without notice.
