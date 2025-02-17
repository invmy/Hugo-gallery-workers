# Hugo-gallery-workers
使用Hugo Gallery主题快速创建你的个人相册。

# 图库端
本仓库右上角` use this template ` 创建一个自己的仓库，

点击`Settings`进去，开启 来自action的`Pages`

部署完成，仓库右小角会显示已经发布了的Pages。

# 上传端
## personal-access-tokens
前往https://github.com/settings/ 创建获取个人TOKEN. 主要权限 Contents 写入

将workers.js中的代码部署到cloudflare Workers上，实现快速上传。

修改上方的变量为自己的
变量token：是为了防止直接访问，可以是任意字符或者密码。不含特殊符号，推荐使用uuid。
主要修改`USER、REPO、GITHUB_TOKEN`

# 创建新的相册

比如创建`旅游`

则创建文件夹`旅游`
文件夹中创建`index.html`最简单内容为，
```
---
title: Fashion & Beauty
---
```
封面为第一张图片，默认文件名升序。更多请看主题的使用 https://github.com/nicokaiser/hugo-theme-gallery

# 注意事项

Hugo支持的格式优先，不支持AVIF、HEIF等格式。

先创建新的相册，再上传图片。上传段会自动读取新的文件夹。

默认CDN为jsdelivr。
