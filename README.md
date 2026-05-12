# MailboxHub Online

中文 | [English](#english)

MailboxHub Online 是一个轻量的在线 Outlook 邮箱验证码读取页面。它是纯静态 GitHub Pages 前端，实际 IMAP/OAuth2 读取由 `https://www.boji1334.com` 后端 API 完成。

在线地址：

<https://boji1334.github.io/mailboxhub-online/>

## 功能

- 支持 `email----password----client_id----refresh_token` 格式账号行。
- 在线读取 Outlook INBOX 最新邮件列表。
- 自动提取验证码并支持点击复制。
- 支持查看邮件全文。
- Windows、macOS、Ubuntu 都可通过浏览器使用。
- 无需安装 macOS 桌面客户端。

## 后端 API

默认后端：

```text
https://www.boji1334.com
```

接口：

```text
POST /api/sms/fetch
POST /api/sms/view
```

## 隐私说明

账号行会发送到 boji1334 后端用于 Outlook OAuth2 / IMAP 读取。请不要把真实 refresh token 提交到公开 Issue、截图或源码仓库中。

## English

MailboxHub Online is a lightweight GitHub Pages frontend for reading Outlook mailbox verification codes online. The static page calls the boji1334 backend API for OAuth2/IMAP access.

Live site:

<https://boji1334.github.io/mailboxhub-online/>

Features:

- Supports account lines in `email----password----client_id----refresh_token` format.
- Reads recent Outlook INBOX messages.
- Extracts verification codes and supports click-to-copy.
- Supports full email body preview.
- Works in browsers on Windows, macOS, and Ubuntu.

Privacy note: account lines are sent to the boji1334 backend for Outlook OAuth2/IMAP access. Do not publish real refresh tokens in issues, screenshots, or repositories.
