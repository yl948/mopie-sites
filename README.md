# Mopie PT Sites Configuration

这是 Mopie 媒体管理工具的 PT 站点配置文件仓库。

## 支持的站点

| 站点 | ID | 类型 | 配置文件 |
|------|-----|------|----------|
| 馒头 | mteam | API/cookies | mteam.yml |
| 青蛙 | qingwa | NexusPHP | qingwa.yml |
| 天空 | hdsky | NexusPHP | hdsky.yml |
| 海带 | hddolby | NexusPHP | hddolby.yml |
| 红豆饭 | hdfans | NexusPHP | hdfans.yml |
| 柠檬 | audiences | NexusPHP | audiences.yml |
| 阿童木 | hdatmos | NexusPHP | hdatmos.yml |
| 兔子 | tjupt | NexusPHP | tjupt.yml |
| 葡萄 | putao | NexusPHP | putao.yml |
| 蜂蜜 | keepfrds | NexusPHP | keepfrds.yml |
| 翠岛 | springsunday | NexusPHP | springsunday.yml |
| 柚子 | ptsbao | NexusPHP | ptsbao.yml |
| 皇后 | agsv | NexusPHP | agsv.yml |
| CHD | chdbits | NexusPHP | chdbits.yml |
| Mikan | mikanani | MikanAPI | mikanani.yml |
| FileList | filelist | FileListAPI | filelist.yml |
| IPT | iptorrents | IPTAPI | iptorrents.yml |
| Exoticaz | exoticaz | Unit3D | exoticaz.yml |
| Sukebei | sukebei | NexusPHP | sukebei.yml |

## 使用方法

### 自动更新（推荐）
在 Mopie 设置中配置：
- 配置仓库地址：`https://github.com/yl948/mopie-sites`
- 自动更新间隔：每天/每周

### 手动更新
```bash
# 下载单个站点配置
wget https://raw.githubusercontent.com/yl948/mopie-sites/main/data/sites/qingwa.yml

# 下载所有配置
git clone https://github.com/yl948/mopie-sites.git
cp -r mopie-sites/data/sites/* /path/to/mopie/data/sites/
```

## 配置文件结构

每个站点配置文件包含：
```yaml
id: 站点ID
name: 站点名称
domain: 站点域名
encoding: 编码格式
config_url: 配置文件URL（用于自动更新）
allow_auth_type: 认证方式（可选）

login: 登录检测规则
category_mappings: 分类映射
userinfo: 用户信息提取规则
search: 搜索参数
torrents: 种子列表解析规则
```

## 贡献

欢迎提交 PR 添加新的站点配置或修复现有配置。

### 添加新站点
1. Fork 本仓库
2. 在 `data/sites/` 目录创建新的 `.yml` 文件
3. 参考现有配置文件格式
4. 测试配置文件是否正常工作
5. 提交 PR

### 配置文件规范
- 必须包含 `id`、`name`、`domain` 字段
- 选择器必须符合站点实际 HTML 结构
- 建议添加 `config_url` 便于后续更新

## License

MIT License
