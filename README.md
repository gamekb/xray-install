# ⚡ Xray (VMess+WS+TLS) 自用一键脚本

这是一个主打**轻量、兼容性**的 Xray 安装脚本。

此脚本是为了在一些**比较刁钻的环境**（比如 Alpine Linux、Docker 容器、或者没有 Systemd 的极简 VPS）也能快速跑起一个代理节点。

## 核心配置逻辑

* **核心版本**：锁定使用 Xray-core `v1.8.4` (稳定够用)。
* **协议组合**：`VMess` + `WebSocket` + `TLS`。
* **证书策略**：**自签名证书** (Self-Signed)。
    * *好处*：不需要你真的去买域名，也不用折腾 Cloudflare 解析，直接用 IP 就能连。
    * *坏处*：客户端必须设置“跳过证书验证”。

## 🚀 一键安装

用 curl 或 wget 拉取运行即可：

```bash
bash <(curl -sL https://raw.githubusercontent.com/gamekb/xray-install/main/install.sh)
```
或

```bash
bash <(wget -qO- https://raw.githubusercontent.com/gamekb/xray-install/main/install.sh)
