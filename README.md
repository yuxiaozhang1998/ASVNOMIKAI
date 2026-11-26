# ASV Party Quiz — ASVNOMIKAI Upgrade

ASV 聚会娱乐问答站，基于 ASVNOMIKAI 升级。线上地址：https://asv.imyuxiao.com

## 功能
- ASV Quiz：主持屏 + 手机扫码进房（Room ID + QR），MQTT 同步（broker.emqx.io，prefix partyquiz/asv-v13）
- 4 语言：日本語 / 繁體中文 / Tiếng Việt / English，自动识别 + 手动切换
- 题库 20 题（ASICS 历史 + 越南文化），主持可选 10/15/20 题、随机顺序、每题 15/20/30 秒
- 计分：基础分 + 速度奖励 + 连对奖励，5 题答错淘汰，最后前三名领奖台
- 娱乐中心首页另带 Random Picker（随机抽人）和 Bingo Caller（1-75 叫号），无需联网同步

## 使用
- 主持：打开 https://asv.imyuxiao.com 选 ASV Quiz → 主持，投影大屏，设置题数/计时后开始
- 参加者：扫主持屏 QR 码（?mode=player&room=XXXX）或手动输 Room ID，填昵称进房答题
- 语言：右上角切换，每台设备各自选，不影响同步

## 部署
Netlify 静态站（publish dir `.`，无构建步骤）。推送 main 后 Netlify 自动部署。自定义域名 asv.imyuxiao.com（Cloudflare DNS CNAME，DNS-only）。
