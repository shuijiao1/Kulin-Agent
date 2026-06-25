# Kulin Agent

Kulin Agent 是 Kulin 面板配套的轻量服务器探针，基于 Nezha Agent 精简改名，保持与 Kulin Dashboard 当前 gRPC 协议兼容。

## 安装

Linux / macOS：

```bash
curl -L https://raw.githubusercontent.com/shuijiao1/Kulin/master/script/agent-install.sh -o kulin-agent.sh && chmod +x kulin-agent.sh && env KULIN_SERVER=<面板Agent地址:端口> KULIN_TLS=true KULIN_CLIENT_SECRET=<Agent密钥> ./kulin-agent.sh
```

Windows PowerShell：

```powershell
$env:KULIN_SERVER="<面板Agent地址:端口>";$env:KULIN_TLS="true";$env:KULIN_CLIENT_SECRET="<Agent密钥>";Invoke-WebRequest https://raw.githubusercontent.com/shuijiao1/Kulin/master/script/agent-install.ps1 -OutFile C:\kulin-agent.ps1;powershell.exe C:\kulin-agent.ps1
```

可选环境变量：

- `KULIN_UUID`：指定服务器 UUID
- `KULIN_AGENT_VERSION`：指定安装版本
- `KULIN_AGENT_INSTALL_DIR`：指定安装目录
- `KULIN_AGENT_CONFIG`：指定配置文件路径

## 发布

Release 从 `v0.1.1` 开始，产物命名为：

```text
kulin-agent_<goos>_<goarch>.zip
```

## 上游

本项目基于 `nezhahq/agent` 调整，感谢上游项目。
