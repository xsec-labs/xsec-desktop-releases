# XSec Desktop Releases

XSec Desktop 的安装包和应用内更新资产发布在本仓库的 [Releases](https://github.com/xsec-labs/xsec-desktop-releases/releases)。

| 系统 | 首次安装 | 应用内更新 |
| --- | --- | --- |
| macOS Apple Silicon | `XSec_<version>_aarch64.dmg` | `xsec-desktop_<version>_darwin_aarch64.app.tar.gz` |
| macOS Intel | `XSec_<version>_x86_64.dmg` | `xsec-desktop_<version>_darwin_x86_64.app.tar.gz` |
| Windows x64 | `XSec_<version>_x64-setup.exe` | 同一当前用户 NSIS 安装器 |

稳定版客户端读取 [latest.json](https://github.com/xsec-labs/xsec-desktop-releases/releases/latest/download/latest.json)，下载匹配平台的更新包，并使用内置公钥验证 Tauri 签名。每个安装器和更新包旁均发布 `.sig` 文件。

旧更新签名私钥已丢失，旧签名根的客户端需先手动安装新签名根版本一次。Bundle ID `com.xsec.desktop`、账号和既有用户数据继续沿用。

当前 macOS 安装包未做 Developer ID 签名和公证；Windows 安装包未做 Authenticode 签名。系统可能显示首次打开或未知发布者提示，受管设备按其策略处理。Tauri 签名用于验证应用内更新包。
