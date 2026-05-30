# Clash Meta 功能详解

Clash Meta 是 Clash 的增强分支，支持更多协议和高级功能。

## 新增协议支持

### VLESS Reality

目前最强的抗封锁协议：

```yaml
proxy-groups:
  - name: VLESS-REALITY
    type: select
    proxies:
      - name: my-node
        type: vless
        server: your-server.com
        port: 443
        uuid: your-uuid
        network: tcp
        tls: true
        flow: xtls-rprx-vision
        client-fingerprint: chrome
        reality-opts:
          public-key: your-public-key
          short-id: your-short-id
```

### Hysteria2

高性能 QUIC 协议：

```yaml
proxies:
  - name: HY2
    type: hysteria2
    server: your-server.com
    port: 443
    auth: your-password
    up: "100 Mbps"
    down: "100 Mbps"
```

## 性能对比

| 功能 | Clash | Clash Meta |
|------|-------|-----------|
| VLESS Reality | No | Yes |
| Hysteria2 | No | Yes |
| TUIC | No | Yes |
| Rule Providers | Yes | Yes |

## 使用建议

- **Windows**: [Clash Verge](https://github.com/clash-verge/clash-verge) 内置 Meta
- **Android**: [ClashMeta](https://github.com/MetaCubeX/ClashMetaAndroid)
- **Linux**: 手动安装 Meta 内核

---

推荐工具：

- [Clash for Windows](https://clashforwindows.site/)
- [ClashMI](https://clashmi.site/)
- [FlClash](https://flclash.us/)
