# Steve 的 F-Droid 仓库

F-Droid 第三方仓库由 GitHub Actions 自动构建，收录 Tickets 与 AppSpace 的公开 Release APK。

## 仓库地址

- 主仓库：<https://steve0309.dpdns.org/fdroid/repo/>
- 历史版本：<https://steve0309.dpdns.org/fdroid/archive/>

## 启用发布工作流

在 GitHub 的 **HomePage** 仓库进入 **Settings → Secrets and variables → Actions**，新增 Repository secret：

`FDROID_REPO_SECRET`

请将 **Tickets** 仓库中现有的 `FDROID_REPO_SECRET` 原样复制到 HomePage；不要重新生成密钥。沿用原密钥是为了保持仓库签名身份。

添加后，进入 **Actions → Publish Steve F-Droid Repo (HomePage) → Run workflow** 手动运行一次。确认工作流成功，并检查上面的主仓库地址能打开有效的 `index-v2.json` 后，再把网站入口切换到新地址。

## 发布方式

- 每天自动检查 Tickets 和 AppSpace 的最新公开 Release。
- 可通过 Actions 手动触发更新。
- 仓库索引、APK 和历史版本归档发布在 HomePage 的 `fdroid/` 目录。
- 仓库签名密钥只存放在 GitHub Actions Secret 中，不提交到 Git。
