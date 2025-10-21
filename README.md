# Telegram群组克隆工具 使用说明

## 开始使用
1. **账号登录与管理**  
   - 支持通过手机号添加新账号。  
   - 支持加载并管理已有账号的 Session 文件。

2. **群组消息克隆**  
   - 支持监听源群组消息，并将其克隆至目标群组。  
   - 支持为克隆账号设置昵称、头像及 Emoji 状态（不支持礼物挂件）。  
   - 支持自定义消息文本替换规则。

3. **代理支持**  
   - 支持通过 SOCKS5 代理连接 Telegram。

4. **黑名单支持**  
   - 可根据用户 ID、昵称或消息关键词进行过滤，自动跳过相关消息。

## 配置文件

项目的配置文件 `setting/config.ini` 包含以下内容：

```ini
[telegram]
source_group = ouyoung  # 源群组用户名/链接（被监听的群）
target_group = ouyoung  # 目标群组用户名/链接（接收转发消息的群）

[proxy]
is_enabled = true/false # 启用/不启用代理
host = 127.0.0.1  # SOCKS5 代理服务器地址
port = 7890  # SOCKS5 代理服务器端口
type = socks5  # 代理类型（SOCKS5）

[blacklist]
user_ids = 123, 12345 # 黑名单ID，多个请用英文逗号分隔
keywords = 飞机号, 出售 # 黑名单ID，多个请用英文逗号分隔
names = 服务器 # 黑名单ID，多个请用英文逗号分隔

[replacements]
a = b  # 文本替换规则
你好 = 我好  # 文本替换规则
```

## 其他说明
- 作者Telegram：https://t.me/ouyoung
- Telegram交流群：https://t.me/oyDevelopersClub
- Telegram频道：https://t.me/TGToolsChannel
