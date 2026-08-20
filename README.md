# PFA 机甲大师战队 - 招新面试系统（网页版）

网页版招新面试报名系统，连接腾讯云开发(CloudBase)云数据库，与微信小程序共享同一套数据。

## 快速部署到 GitHub Pages

### 1. Fork 或上传本仓库到 GitHub

### 2. 开启 GitHub Pages
- 进入仓库 Settings → Pages
- Source 选择 Deploy from a branch
- Branch 选 main，文件夹选 / (root)
- 保存

### 3. 配置 CloudBase 安全域名
- 登录微信开发者工具 → 云开发控制台
- 设置 → 安全配置 → 网页域名白名单
- 添加你的 GitHub Pages 域名：`https://你的用户名.github.io`

### 4. 访问
打开 `https://你的用户名.github.io/pfa-recruit/` 即可使用

## 云数据库权限配置

在云开发控制台 → 数据库，将以下集合权限设为「所有用户可读写」：

- accounts
- users
- applications
- config
- interview_sessions
- interview_slots
- interview_bookings
- reviews
- email_log

## 默认邀请码
- 面试官邀请码：`PFA2026`
- 管理员邀请码：`PFA-ADMIN`

## 技术栈
- 纯 Vanilla JS，零依赖
- CloudBase JS SDK v3
- Web Crypto API (PBKDF2 SHA-512 密码加密，与小程序兼容)
