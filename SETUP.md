# Utopia - GitHub Profile Setup Guide

这是一个自定义 GitHub 个人资料展示项目，包含自动生成的统计数据和活动信息。

## 🚀 快速开始

### 1. 替换个人信息

编辑 `README.md` 文件，替换以下内容：
- `your-username` → 你的 GitHub 用户名
- `your-wakatime-username` → 你的 WakaTime 用户名
- `your-email@example.com` → 你的邮箱
- 其他社交媒体链接

### 2. 设置 GitHub Token

在项目设置中配置 `METRICS_TOKEN`：

**步骤：**
1. 访问 https://github.com/settings/tokens
2. 点击 "Generate new token (classic)" 或 "Generate new token"
3. 选择以下权限范围：
   - `public_repo`
   - `read:user`
   - `read:org`
   - `read:packages`（可选）
4. 生成并复制 token

**在项目中添加 Secret：**
1. 进入你的仓库 → Settings → Secrets and variables → Actions
2. 点击 "New repository secret"
3. 名称：`METRICS_TOKEN`
4. 值：粘贴你的 token

### 3. 启用 GitHub Actions

1. 进入项目 → Actions 选项卡
2. 确认工作流已启用
3. 手动运行 "Utopia Metrics" 工作流

## 📊 工作流说明

### left.svg
生成左侧统计信息，包括：
- 个人资料卡片
- 贡献活动
- 社区参与
- 编程语言统计
- 代码行数统计
- 热门仓库

### right.svg
生成右侧统计信息，包括：
- 用户元数据
- GitHub 成就
- 最近活动

## 🎨 自定义选项

### 时区设置
在 `metrics.yml` 中修改 `config_timezone`：
- `UTC`
- `Asia/Shanghai`
- `America/New_York`
- 等其他 IANA 时区

### 编程语言筛选
修改 `plugin_languages_skipped` 忽略特定仓库

### 更新频率
修改 cron 表达式改变更新周期：
- `"0 */6 * * *"` - 每 6 小时
- `"0 0 * * *"` - 每天
- `"0 0 * * 0"` - 每周

## 📚 相关资源

- [Lowlighter Metrics 文档](https://github.com/lowlighter/metrics#-documentation)
- [GitHub Stats API](https://github.com/anuraghazra/github-readme-stats)
- [WakaTime Stats](https://wakatime.com)

## 💡 提示

- 首次运行可能需要几分钟时间生成图表
- 确保你的 GitHub 贡献有足够的活动数据
- 定期检查 Actions 日志排查问题

---

**Enjoy your Utopia! 🌟**
