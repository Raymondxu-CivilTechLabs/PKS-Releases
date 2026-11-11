# PKS Releases

本仓库**只存放发布产物**，不含源码。源码在私有仓库中维护。

## 下载

最新版本：见右侧 **Releases** → **Latest**。

| 文件 | 用途 |
|---|---|
| `PKS_Setup_v<版本>.exe` | 安装版（推荐）。标准 Windows 安装向导，覆盖升级保留全部数据 |
| `PKS_Portable_v<版本>.zip` | 便携版。解压即用，不写注册表、不建快捷方式 |
| `*.sha256` | 对应文件的 SHA-256 校验值 |

## 校验下载完整性

Windows（PowerShell）：

```powershell
Get-FileHash .\PKS_Setup_v0.2.0.exe -Algorithm SHA256
```

把输出与 `PKS_Setup_v0.2.0.exe.sha256` 里的那串十六进制逐字符比对。

Linux / macOS / WSL：

```bash
sha256sum -c PKS_Setup_v0.2.0.exe.sha256
```

## 版本号规则

`主版本.次版本.修订号`，三段纯数字。tag 形如 `v0.2.0`。

- 破坏性变更（数据库/文件格式不兼容）→ 升次版本
- 修 bug、加不破坏兼容的功能 → 升修订号
- 同一版本号只发布一次，已上传的资产永不覆盖

## 关于更新提示

应用内置的自动更新目前**尚未实现**（设置页的「自动检查更新」开关暂为占位）。
请手动回到本页面下载新版本。
