---
title: hexo 添加live2D
date: 2025-1-29 12:00:00
tags: [Hexo, 教程]
categories: [技术]
---

添加插件：

`npm install --save hexo-helper-live2d
`

然后在hexo的`_config.yml`中增加live2d的配置

```html
live2d:
  enable: true
  # enable: false
  scriptFrom: local # 默认
  pluginRootPath: live2dw/ # 插件在站点上的根目录(相对路径)
  pluginJsPath: lib/ # 脚本文件相对与插件根目录路径
  pluginModelPath: assets/ # 模型文件相对与插件根目录路径
  tagMode: false # 标签模式, 是否仅替换 live2d tag标签而非插入到所有页面中
  debug: false # 调试, 是否在控制台输出日志
  model:
    use: live2d-widget-model-hibiki # 模型名称  
  display:
    position: left
    width: 150
    height: 350
  mobile:
    show: true # 手机中是否展示

```

支持很多种模型：  [模型预览](https://blog.csdn.net/wang_123_zy/article/details/87181892)
``` python
# 使用模型前需要先安装 npm install name
# 模型可选项
live2d-widget-model-chitose
live2d-widget-model-epsilon2_1
live2d-widget-model-gf
live2d-widget-model-haru
live2d-widget-model-haruto
live2d-widget-model-hibiki
live2d-widget-model-hijiki
live2d-widget-model-izumi
live2d-widget-model-koharu 
live2d-widget-model-miku  
live2d-widget-model-ni-j  
live2d-widget-model-nico 
live2d-widget-model-nietzsche 
live2d-widget-model-nipsilon 
live2d-widget-model-nito 
live2d-widget-model-shizuku  
live2d-widget-model-tororo 
live2d-widget-model-tsumiki  
live2d-widget-model-unitychan 
live2d-widget-model-wanko  
live2d-widget-model-z16  

```

用哪个模型需要提前安装:

`npm install 模型名称`

安装模型之后，需要修改安装的模型名称
```html
 model:
    use: live2d-widget-model-hibiki # 模型名称
```

TODO： 可替换为加强版live2D，可换装、文字，再接入deepsek之类的大模型效果更佳