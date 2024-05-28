---
title: 自訂樣式

date: 2024-05-28 21:58:24
tags: 
- Hexo
- NexT
categories: Hexo
description: 自訂Hexo樣式
---

#### 步驟一 到 hexo-theme-next/_config.yml 搜尋 Custom_file_path，將custom_file_path 的 style 註解解開

```md
# Define custom file paths.
# Create your custom files in site directory `source/_data` and uncomment needed files below.
custom_file_path:
  #head: source/_data/head.njk
  #header: source/_data/header.njk
  #sidebar: source/_data/sidebar.njk
  #postMeta: source/_data/post-meta.njk
  #postBodyStart: source/_data/post-body-start.njk
  #postBodyEnd: source/_data/post-body-end.njk
  #footer: source/_data/footer.njk
  #bodyEnd: source/_data/body-end.njk
  #variable: source/_data/variables.styl
  #mixin: source/_data/mixins.styl
  style: source/_data/styles.styl
```

#### 步驟二 在 Hexo 專案根目錄的 source 建立 _data 資料夾並新增**styles.styl 檔案**

![圖片名稱](/images/style.png)

#### 將文章中的連結樣式移除下底線並改為藍色

```scss
.post-body {
 a:not(.btn){
    color: #337AB7;
    border-bottom: none;
}
}
```

a:not(.btn) 避免修改到首頁的閱讀全文按鈕
