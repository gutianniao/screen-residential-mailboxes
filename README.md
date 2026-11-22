# 住宅邮箱地址筛选

这是一个 Codex Skill，用于采集美国 Anytime Mailbox 网点，并根据 Smarty 和 Firstlogic 的核验结果筛选住宅类地址。

- Smarty 要求 `RDI=Residential`、`CMRA=N`。
- Firstlogic 要求 `RDI=Y`、`R` 或 `Residential`，同时 `CMRA=N`。
- 筛选结果包含网点来源和两家服务的核验字段。查询进度保存到本地，可以断点继续。

## 安装

1. 下载并解压 [screen-residential-mailboxes-skill.zip](./screen-residential-mailboxes-skill.zip?raw=true)。
2. 将解压出的 `screen-residential-mailboxes` 文件夹复制到 `~/.codex/skills/`，确保该文件夹内直接包含 `SKILL.md`。Windows 上的默认目录为 `%USERPROFILE%\.codex\skills\`。
3. 在 Codex 中输入 `$screen-residential-mailboxes`，并说明要筛选的州和地址数量。

采集和筛选脚本需要 PowerShell。核验使用 Smarty 和 Firstlogic 的网页或正式 API。详细流程见安装包内的 `SKILL.md`。
