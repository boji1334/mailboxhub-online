# MailboxHub Online

中文 | [English](#english)

MailboxHub Online 是一个轻量的在线 Outlook 邮箱验证码读取页面。它是纯静态 GitHub Pages 前端，实际 IMAP/OAuth2 读取由 `https://www.boji1334.com` 后端 API 完成。

在线地址：

<https://boji1334.github.io/mailboxhub-online/>

## 功能

- 支持 `email----password----client_id----refresh_token` 格式账号行。
- 默认通过 `POST /api/v1/code` 获取最近 30 秒内的 OpenAI 验证码。
- 页面只展示最新验证码，完整邮件列表请使用 `https://www.boji1334.com/sms`。
- 加载时显示动态转圈和进度条。
- Windows、macOS、Ubuntu 都可通过浏览器使用。
- 无需安装 macOS 桌面客户端。

## 后端 API

默认后端：

```text
https://www.boji1334.com
```

接口：

```text
POST /api/v1/code
```

`POST /api/v1/code` 请求示例：

```json
{
  "account_line": "email----password----client_id----refresh_token",
  "provider": "openai",
  "within_seconds": 30,
  "top": 20
}
```

成功时直接读取返回 JSON 中的 `code` 字段。

## 隐私说明

账号行会发送到 boji1334 后端用于 Outlook OAuth2 / IMAP 读取。请不要把真实 refresh token 提交到公开 Issue、截图或源码仓库中。

## English

MailboxHub Online is a lightweight GitHub Pages frontend for reading Outlook mailbox verification codes online. The static page calls the boji1334 backend API for OAuth2/IMAP access.

Live site:

<https://boji1334.github.io/mailboxhub-online/>

Features:

- Supports account lines in `email----password----client_id----refresh_token` format.
- Uses `POST /api/v1/code` by default to read OpenAI verification codes from emails dated within the last 30 seconds.
- Shows only the latest code. Use `https://www.boji1334.com/sms` for the full mailbox view.
- Shows a spinner and progress bar while loading.
- Works in browsers on Windows, macOS, and Ubuntu.

Privacy note: account lines are sent to the boji1334 backend for Outlook OAuth2/IMAP access. Do not publish real refresh tokens in issues, screenshots, or repositories.
