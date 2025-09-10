+++
date = '2025-09-10T13:25:05+08:00'
draft = false
title = '解决codex执行任务需不断确认问题'
description = '文章简介'
tags = ['codex']
categories = ['AI']
author = 'Ushaio'
showToc = true
TocOpen = false
hidemeta = false
comments = false
disableHLJS = false
disableShare = false
searchHidden = false

+++

最近使用codex，vscode插件选择full access即可，但是命令行模式下会不断需要手动确认，一个任务得点几十次，改了配置和更新都没用，最后刷到一个解决办法，使用命令行执行即可：

```powershell
codex --ask-for-approval never --sandbox danger-full-access -c model_reasoning_effort=high
```

丝滑多了
