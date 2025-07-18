# 部署指南

## 将本地仓库推送到GitHub并启用GitHub Pages

### 步骤1：连接到GitHub仓库

由于您已经在GitHub上创建了同名仓库，需要将本地仓库连接到GitHub：

```bash
# 如果还没有初始化git，先初始化
git init

# 添加远程仓库（替换your-username为您的GitHub用户名）
git remote add origin https://github.com/your-username/Occlu-FER.git

# 验证远程仓库已添加
git remote -v
```

### 步骤2：处理现有内容

如果GitHub仓库中已有内容，需要先拉取：

```bash
# 拉取现有内容（如果有冲突，使用--allow-unrelated-histories）
git pull origin main --allow-unrelated-histories

# 如果有冲突，手动解决后再继续
```

### 步骤3：提交并推送

```bash
# 添加所有文件
git add .

# 提交更改
git commit -m "Add Occlu-FER dataset website"

# 推送到GitHub
git push -u origin main
```

### 步骤4：配置GitHub Pages

1. 访问您的GitHub仓库页面
2. 点击 **Settings** 选项卡
3. 在左侧菜单中找到 **Pages**
4. 在 **Source** 部分，选择 **GitHub Actions**
5. GitHub会自动检测到Hugo工作流文件并开始构建

### 步骤5：等待部署完成

- 推送代码后，GitHub Actions会自动开始构建
- 您可以在 **Actions** 选项卡中查看构建进度
- 构建完成后，网站将在 `https://your-username.github.io/Occlu-FER/` 可用

## 本地预览

在推送到GitHub之前，您可以本地预览网站：

```bash
# 启动Hugo开发服务器
hugo server

# 在浏览器中访问 http://localhost:1313
```

## 更新网站内容

要更新网站内容：

1. 编辑 `content/_index.md` 文件
2. 本地预览更改：`hugo server`
3. 提交并推送更改：
   ```bash
   git add .
   git commit -m "Update content"
   git push
   ```

## 自定义配置

### 更新baseURL

在 `hugo.toml` 中，将 `your-username` 替换为您的实际GitHub用户名：

```toml
baseURL = 'https://your-actual-username.github.io/Occlu-FER/'
```

### 更新社交链接

在 `hugo.toml` 中更新社交链接部分：

```toml
[[params.socialIcons]]
  name = "github"
  url = "https://github.com/Wenyuzhy/ORSANet-master"

[[params.socialIcons]]
  name = "email"
  url = "mailto:202522081112@std.uestc.edu.cn"
```

## 故障排除

### 如果构建失败

1. 检查 **Actions** 选项卡中的错误信息
2. 确保所有文件都已正确提交
3. 验证 `hugo.toml` 配置文件语法正确

### 如果网站无法访问

1. 确认GitHub Pages已启用
2. 检查仓库是否为公开（Public）
3. 等待几分钟让DNS传播

### 如果样式不正确

1. 确认 `baseURL` 设置正确
2. 检查自定义CSS文件是否存在
3. 清除浏览器缓存

---

**完成这些步骤后，您的Occlu-FER数据集网站就会在GitHub Pages上运行了！**
