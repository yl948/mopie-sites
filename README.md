# Mopie PT Sites Configuration

这是 Mopie 媒体管理工具的 PT 站点配置仓库。只收录已经对照站点页面适配过的配置，未适配的站点不会放进来。

## 已适配站点

| 站点 | ID | 类型 | 配置文件 |
|------|-----|------|----------|
| 青蛙 | qingwa | NexusPHP | qingwa.yml |
| 红豆饭 | hdfans | NexusPHP | hdfans.yml |
| 麒麟 | hdkylin | NexusPHP | hdkylin.yml |
| 家园 | HDHome | NexusPHP | hdhome.yml |
| 咖啡PT | ptcafe | NexusPHP | ptcafe.yml |
| 织梦 | zmpt | NexusPHP | zmpt.yml |

Mopie 更新配置时只会同步本机已经添加的站点，不会把仓库里其它文件整包拉下来。

## 使用方法

### 自动更新（推荐）

在 Mopie 站点页检查更新。只会更新已添加站点对应的 YAML。

### 手动更新

```bash
git clone https://github.com/yl948/mopie-sites.git
cp mopie-sites/data/sites/<站点id>.yml /path/to/mopie/data/sites/
```

## 配置文件结构

每个站点配置文件包含：

```yaml
id: 站点ID
name: 站点名称
domain: 站点域名
encoding: 编码格式
allow_auth_type: 认证方式（可选）

login: 登录检测规则
category_mappings: 分类映射
userinfo: 用户信息提取规则
search: 搜索参数
torrents: 种子列表解析规则
```

## 贡献

新增站点请先在真实页面上适配并跑通搜索/折扣/标签，再提交 PR。未对照过 HTML 的配置不要加入本仓库。

## License

MIT
