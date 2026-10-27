# Steve 的 F-Droid 仓库

F-Droid 第三方仓库由 GitHub Actions 自动构建，收录 Tickets 与 AppSpace 的公开 Release APK。

## 仓库地址

- 主仓库：https://steve0309.dpdns.org/fdroid/repo/
- 历史版本：https://steve0309.dpdns.org/fdroid/archive/

## 仓库指纹

当前仓库签名密钥 SHA-256 指纹：

`F2 6E F2 0F 15 DD 71 71 3A AE 94 A9 24 BC 7C 1F BF 22 70 17 B5 71 B5 1D 46 7D 7F A3 5F 75 00 85`

添加仓库时，建议通过主仓库页面的 QR 码或 `fdroid.link` 链接添加，并核对指纹。

## GitHub Actions Secrets

发布工作流使用以下两个 Repository secrets：

- `FDROID_KEYSTORE_BASE64`：新仓库签名密钥文件的 Base64 内容（只放 Base64，不要包含 BEGIN/END 行）。
- `FDROID_STORE_PASSWORD`：该密钥文件的密码。

不要把密钥文件或密码提交到 Git 仓库。

## 发布方式

- 每天自动检查 Tickets 和 AppSpace 的最新公开 Release。
- 可通过 Actions 手动触发更新。
- 仓库索引、APK 和历史版本归档发布在 HomePage 的 `fdroid/` 目录。
- 仓库签名密钥只存放在 GitHub Actions Secret 中，不提交到 Git。
