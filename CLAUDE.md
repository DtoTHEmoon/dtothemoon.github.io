# dtothemoon.github.io · 作品集网站

## 项目定位
谢力维（Darren Xie）个人作品集，部署在GitHub Pages。
地址：https://dtothemoon.github.io

## 目录结构
```
dtothemoon.github.io/
├── index.html          # 主页，单页滚动
├── resume.pdf          # 简历PDF，"下载简历"按钮链接此文件
└── assets/
    └── images/
        ├── ark-main.png        # 方舟大脑主页截图
        ├── ark-finance.png     # 方舟财务报表截图
        ├── gos-dashboard.png   # GrowthOS成长看板截图
        ├── gos-heatmap.png     # GrowthOS热力图截图
        └── gos-talent.png      # GrowthOS人才推荐截图
```

## 技术说明
- 纯静态HTML，无框架，无构建步骤
- 配色：主色#FF2442，背景#FFFFFF，文字#1a1a1a
- 响应式，手机端适配
- GitHub Pages自动部署，push到main分支后1-2分钟生效

## 页面结构
- 导航栏（固定顶部）：DX logo + Projects/Writing/GitHub/下载简历
- Hero：姓名+定位+按钮
- Projects：方舟AI系统 / Baichuan-M2评测 / GrowthOS平台
- Open Source & Writing：Rein Skill
- Education：暨南大学 / El Camino College
- Footer：联系方式

## 更新方式
```bash
cd ~/projects/dtothemoon.github.io
# 修改index.html或替换截图后
git add .
git commit -m "update: 描述修改内容"
git push
```

## 简历更新
1. Claude Design修改简历HTML
2. 发给claude.ai转PDF
3. 替换 resume.pdf 文件
4. git add resume.pdf && git commit -m "update resume" && git push

## 踩坑记录
- wkhtmltopdf转PDF时无法访问Google Fonts，需提前移除字体link标签
- Cloudflare会混淆HTML里的邮箱地址，转PDF前需还原为明文
- GitHub Pages对*.github.io仓库自动启用，无需手动开启
- SSH Key配置：~/.ssh/id_ed25519，已添加到GitHub账号

## 关键链接
- 仓库：github.com/DtoTHEmoon/dtothemoon.github.io
- 线上：https://dtothemoon.github.io
- 简历PDF：https://dtothemoon.github.io/resume.pdf
