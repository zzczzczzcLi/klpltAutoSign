# [KLPBBS_auto_sign_in](https://github.com/xyz8848/KLPBBS_auto_sign_in)
基于 GitHub Action 的苦力怕论坛自动签到脚本  
[![GitHub Stars](https://img.shields.io/github/stars/xyz8848/KLPBBS_auto_sign_in)](https://github.com/xyz8848/KLPBBS_auto_sign_in/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/xyz8848/KLPBBS_auto_sign_in)](https://github.com/xyz8848/KLPBBS_auto_sign_in/network/members)

## 如何使用

1. [Fork](https://github.com/xyz8848/KLPBBS_auto_sign_in/fork) 这个仓库
2. 授予工作流读取和写入权限（用于工作流保活，如果仓库中在过去 60 天内没有提交，GitHub 将暂停 GitHub 工作流的计划触发器。除非进行新的提交，否则基于 cron 的触发器不会运行。）
![step2.webp](img/step2.webp)
3. 打开 Actions secrets and variables  
![step3.webp](img/step3.webp)
4. 添加以下 secret：[`USERNAME`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#username)，[`PASSWORD`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#password)

## 更多功能
### 自定义签到时间
（默认每天 00:01 签到）
1. 到 [`.github/workflows/sign_in.yml`](.github/workflows/sign_in.yml) 中修改签到时间

### 用户组到期后自动续费
1. 打开 Actions secrets and variables
2. 添加以下 secret：[`SWITCH_USER`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#switch_user) 或 [`RENEWAL_VIP`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#renewal_vip) 或 [`RENEWAL_SVIP`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#renewal_svip)

### 签到后邮件提示
1. 打开 Actions secrets and variables
2. 添加以下 secret：[`MAIL_ENABLE`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#mail_enable)，[`MAIL_HOST`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#mail_host)，[`MAIL_PORT`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#mail_port)，[`MAIL_USERNAME`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#mail_username)，[`MAIL_PASSWORD`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#mail_password)，[`MAIL_TO`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#mail_to)

### 签到后企业微信提示
1. 打开 Actions secrets and variables
2. 添加以下 secret：[`WECHAT_ENABLE`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#wechat_enable)，[`WECHAT_WEBHOOK`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#wechat_webhook)，[`WECHAT_MENTIONED`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#wechat_mentioned)

### 签到后Server酱提示
1. 打开 Actions secrets and variables
2. 添加以下 secret：[`SERVERCHAN_ENABLE`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#serverchan_enable)，[`SERVERCHAN_KEY`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#serverchan_key)

### 签到后 Telegram 提示
1. 打开 Actions secrets and variables
2. 添加以下 secret：[`TG_ENABLE`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#tg_enable)，[`TG_TOKEN`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#tg_token)，[`TG_CHAT_ID`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#tg_chat_id)

### 签到后 Ntfy 提示
1. 打开 Actions secrets and variables
2. 添加以下 secret：[`NTFY_ENABLE`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#ntfy_enable)，[`NTFY_URL`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#ntfy_url)，[`NTFY_TOPIC`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#ntfy_topic)
3. 认证 **（以下方法任选一个）**
    1. 如果要使用**用户名+密码**认证，添加以下 secret：[`NTFY_USERNAME`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#ntfy_username)，[`NTFY_PASSWORD`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#ntfy_password)
    2. 如果要使用 **Token** 认证，添加以下 secret：[`NTFY_TOKEN`](https://github.com/xyz8848/KLPBBS_auto_sign_in/blob/main/docs/secrets.md#ntfy_token)

## 统计数据
![](https://repobeats.axiom.co/api/embed/61dc140b2e19a099f83e593318024e98f7b66be5.svg)
