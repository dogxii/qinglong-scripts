# 青龙脚本状态记录

本仓库收录了各种自动化脚本，用于青龙面板。以下是脚本的可用性状态记录。

## 📋 脚本状态概览

| 脚本名称 | 状态 | 最后更新 | 备注 |
|---------|------|---------|------|
| 微软积分.js | ✅ 可用 | 2025.9.6 | 微软浏览器积分自动获取 |
| 小黑盒签到.js | ❌ 失效 | 2025.9.6 | 小黑盒签到已失效，无法使用 |
| 胖乖生活.py | ⚠️ 部分可用 | 2025.9.6 | 仍能使用但部分失效 |

## 📝 详细说明

### ✅ 微软积分.js - 可用
- **功能**: 微软Rewards积分自动获取
- **状态**: ✅ 正常工作
- **运行时间**: `11 18 * * *`
- **依赖**: axios、moment、crypto
- **配置**: 需要设置 `MS_COOKIES_1` 环境变量
- **说明**: 抓取 https://rewards.bing.com/welcome?rh=F5F34605&ref=rafsrchae 下的cookie即可

### ❌ 小黑盒签到.js - 已失效
- **功能**: 小黑盒签到及日常任务
- **状态**: ❌ 已失效，无法使用
- **说明**: 该脚本已确认失效，不再提供服务

### ⚠️ 胖乖生活.py - 部分可用
- **功能**: 胖乖生活积分获取
- **状态**: ⚠️ 仍能使用但部分失效
- **运行时间**: `0 06-20 * * *`
- **依赖**: urllib3、requests、requests_toolbelt
- **配置**: 需要设置 `PGSH_TOKEN` 环境变量
- **获取ck**: https://avrinbai.cn/pg/ 或 https://bigostk.github.io/pg/
- **说明**: 作者标注部分功能失效，建议谨慎使用

## 🔧 使用说明

### 环境依赖安装

#### 微软积分脚本依赖
```bash
npm install axios moment crypto
```

#### 胖乖生活脚本依赖
```bash
pip install urllib3 requests requests_toolbelt
```

### 环境变量配置

#### 微软积分
```bash
export MS_COOKIES_1="your_cookies_1"
export MS_REFRESH_TOKEN_1="your_refresh_token_1"  # 可选
export MS_ALIAS_1="Account 1"  # 可选
export MS_PROXY_1="proxy:8080"  # 可选
export LICENSE_KEY="your_license_key"  # 需要授权
```

#### 胖乖生活
```bash
export PGSH_TOKEN="your_token"
# 可选配置
export pg_dl="True"  # 代理开关
export pg_dlurl="proxy_api_url"  # 代理API
export pg_bf="True"  # 并发开关
export pg_bfsum="3"  # 并发数量
export pg_ts="False"  # 推送开关
```

## ⚠️ 注意事项

1. **授权要求**: 微软积分脚本需要授权码 `LICENSE_KEY`
2. **脚本失效**: 小黑盒签到脚本已确认失效，无法使用
3. **部分失效**: 胖乖生活脚本部分功能可能失效，请根据实际情况使用
4. **更新频率**: 建议定期检查脚本可用性并更新此文档

## 📅 状态更新记录

- **2025.9.6**: 初始记录创建
  - 微软积分: ✅ 确认可用
  - 小黑盒签到: ❌ 确认失效（已无法使用）
  - 胖乖生活: ⚠️ 部分可用

## 🤝 贡献说明

如果您测试了脚本的可用性，欢迎更新此README文档：

1. 测试脚本功能
2. 更新状态表格
3. 补充使用说明
4. 提交PR

---

**免责声明**: 本仓库脚本仅供学习交流使用，使用者需自行承担风险。请遵守相关平台的使用条款。