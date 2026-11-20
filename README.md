# loon-rules

tao 的 Loon 自定义规则库。从原 lxy-fixed.lcf 的本地 [Rule] 拆出，Loon 通过 [Remote Rule] 订阅本仓库的 .list 文件。
规则文件内每行只有 `类型,值[,no-resolve]`，**不带策略**；策略由 Loon 配置里订阅那一行 `policy=` 决定。

## 分类

- `emby/` — Emby 服规则（72 条）
- `modules/` — Rex / 各类模块规则（223 条）
- `daily/` — 日常规则（47 条）

每个分类按策略再分文件，如 `emby/emby-emby.list`（走 emby 组）、`emby/emby-direct.list`（直连）、`modules/modules-node.list`（走节点选择）、`modules/modules-tmdb.list`（走影视刮削）。

## 新增规则

在这个聊天（Loon配置文件）里直接说域名和走哪个组即可，例如：
- `xxx.com 加到 emby，走 emby`
- `yyy.com 加到模块，走日本节点`
- `zzz.com 日常直连`

维护者会把规则追加到对应文件并推送；Loon 端无需改配置，更新规则源后生效。

## 注意

本仓库只放域名/IP 规则，不放订阅地址、token、证书等敏感信息。
