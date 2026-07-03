# 杨洋的个人主页

温暖风格的个人主页，支持中英双语切换，每小时自动更换励志金句。

## 功能特点

- 简洁温暖的视觉设计
- 中英双语一键切换
- 24小时金句自动轮换（每小时一条）
- 响应式布局，适配手机和电脑
- 纯静态页面，无需后端

## 本地预览

用浏览器直接打开 `index.html` 即可预览。

## GitHub Pages 部署步骤

### 第一步：创建 GitHub 仓库

1. 登录 [GitHub](https://github.com)
2. 点击右上角 **+** 号，选择 **New repository**
3. 仓库名称填写：`你的用户名.github.io`（例如 `yangyang.github.io`）
   - 注意：必须用这个格式命名，这样 GitHub Pages 会自动识别
   - 如果想用其他仓库名也可以，后续需要额外设置
4. 选择 **Public**（公开）
5. 勾选 **Add a README file**
6. 点击 **Create repository**

### 第二步：上传网站文件

**方法一：网页上传（最简单）**

1. 在仓库页面点击 **Add file** → **Upload files**
2. 将以下文件拖入上传区域：
   - `index.html`
   - `css/` 文件夹（含 `style.css`）
   - `js/` 文件夹（含 `main.js`）
3. 在下方填写提交信息，点击 **Commit changes**

> 注意：网页上传不支持文件夹，需要先上传 `css` 和 `js` 文件夹内的文件。
> 建议在仓库中先创建 `css` 和 `js` 文件夹，再分别上传文件。

**方法二：Git 命令上传（推荐）**

```bash
# 克隆仓库到本地
git clone https://github.com/你的用户名/你的用户名.github.io.git

# 将网站文件复制到仓库目录
cp -r index.html css js 你的用户名.github.io/

# 进入仓库目录
cd 你的用户名.github.io

# 添加所有文件
git add .

# 提交
git commit -m "添加个人主页"

# 推送到 GitHub
git push origin main
```

### 第三步：开启 GitHub Pages

1. 进入仓库页面，点击 **Settings**（设置）
2. 左侧菜单找到 **Pages**
3. 在 **Source** 下拉菜单中选择：
   - Branch: `main`
   - Folder: `/ (root)`
4. 点击 **Save**

### 第四步：访问你的网站

等待 1-2 分钟后，在 Pages 设置页面顶部会显示你的网站地址：

```
https://你的用户名.github.io
```

打开这个链接即可看到你的个人主页！

## 自定义修改

### 修改个人信息

编辑 `index.html` 文件中的内容。

### 修改金句

编辑 `js/main.js` 文件中的 `quotes` 数组，共有 24 条金句（0-23点各一条）。

### 修改抖音链接

在 `index.html` 中找到这一行：

```html
<a href="#" class="contact-card" id="douyin-link">
```

将 `#` 替换为你的抖音主页链接，例如：

```html
<a href="https://www.douyin.com/user/你的抖音ID" class="contact-card" id="douyin-link">
```

### 修改颜色主题

编辑 `css/style.css` 文件顶部的 `:root` 变量：

```css
:root {
    --primary: #FF8C69;       /* 主色调 */
    --primary-light: #FFB088;  /* 浅色调 */
    --warm-yellow: #FFD93D;    /* 点缀色 */
    /* ... */
}
```

## 文件结构

```
├── index.html        # 主页面
├── css/
│   └── style.css     # 样式文件
├── js/
│   └── main.js       # 脚本文件（语言切换+金句轮换）
└── README.md         # 说明文档
```

## 技术栈

- HTML5
- CSS3（动画、渐变、毛玻璃效果）
- 原生 JavaScript（无框架依赖）
