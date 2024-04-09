---
title: 发布xlog的新方法
datePublishedAt: 2024-04-09T11:26:08.585Z
summary: ""
slug: A-new-way-to-post-xlog
disableAISummary: false
cover: ""
tags: []
---

基于[Github项目-vscode-xlog插件](https://github.com/hyoban/vscode-xlog?tab=readme-ov-file)，我实现了从本地编辑xlog到远程发布。
这样就实现了文档自有化，并可以提交到GitHub。
目前已经实现了提交到Github。（创建仓库即可）期待插件可以自动sync，而不是靠繁琐的手动更新。

目前：
- Github
  - 可以向GitHub Push数据。作用：备份
  - 可以从Github pull数据。作用：备份恢复
    - 令我困惑的点就是这里：如果换了系统/电脑，我应该从GitHub还是xlog下载数据？
      - 稍微思考发现：如果xlog没有崩溃，那就从xlog下载，毕竟比如GitHub备份前更新的post需要xlog的数据，直接从GitHub恢复可能会导致部分数据错误回滚。
- xlog
  - 可以从xlog下载posts，可以在本地创建并更新posts。
  - 但是不知道能否用自定义的发布时间来覆盖xlog数据。
- 插件
  - 没有posts的模板，只能自己复制。
  - 没有自动更新GitHub的工具，比如做到更新xlog和GitHub push联动。