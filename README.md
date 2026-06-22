# Kulin Agent

Kulin Agent 是 Kulin 面板配套的轻量服务器探针，基于 Nezha Agent 精简改名，保持与 Kulin Dashboard 当前 gRPC 协议兼容。

## 安装

Linux / macOS：

```bash
curl -L https://raw.githubusercontent.com/shuijiao1/Kulin/master/script/agent-install.sh -o kulin-agent.sh && chmod +x kulin-agent.sh && env NZ_SERVER=<面板Agent地址> NZ_TLS=true NZ_CLIENT_SECRET=<Agent密钥> ./kulin-agent.sh
```

Windows PowerShell：

```powershell
$env:NZ_SERVER="<面板Agent地址>";$env:NZ_TLS="true";$env:NZ_CLIENT_SECRET="<Agent密钥>";Invoke-WebRequest https://raw.githubusercontent.com/shuijiao1/Kulin/master/script/agent-install.ps1 -OutFile C:\kulin-agent.ps1;powershell.exe C:\kulin-agent.ps1
```

可选环境变量：

- `NZ_UUID`：指定服务器 UUID
- `NZ_DISABLE_AUTO_UPDATE`：禁用自动更新
- `NZ_DISABLE_FORCE_UPDATE`：禁用强制更新
- `NZ_DISABLE_COMMAND_EXECUTE`：禁用命令执行
- `NZ_SKIP_CONNECTION_COUNT`：跳过连接数采集

## 发布

Release 从 `v0.1.1` 开始，产物命名为：

```text
kulin-agent_<goos>_<goarch>.zip
```

## 上游

本项目基于 `nezhahq/agent` 调整，感谢上游项目。
