# 文件系统层次结构
- 本书是[《 Filesystem Hierarchy Standard 》](https://refspecs.linuxfoundation.org/FHS_3.0/fhs-3.0.html)一书的中文译本。该文档规定了Unix/Linux系统中各层次目录的作用，是发行版规划目录层次的指南。对于Mac OS和Android等系统，也有很大指导意义。
- 英语初学者，所学浅薄、精力有限，在翻译的过程中难免存在一些错误或是不完整的部分，正在逐步修正和补充。如果存在疏漏、错误，欢迎各位以[Issue](https://github.com/jerry460/translate-FHS-Filesystem-Hierarchy-Standard-to-Chinese/issues/new)或者[PR](https://github.com/jerry460/translate-FHS-Filesystem-Hierarchy-Standard-to-Chinese/pulls)的方式批评指正，感激不尽。
## 翻译版本为：([2.3版本中文翻译指路](https://github.com/Wylmer/FHS_zh_CN)
### Filesystem Hierarchy Standard

LSB Workgroup, The Linux Foundation

Version 3.0

Copyright © 2015 The Linux Foundation

Copyright © 1994-2004 Daniel Quinlan

Copyright © 2001-2004 Paul 'Rusty' Russell

Copyright © 2003-2004 Christopher Yeoh
## 目录
### [1.介绍](https://github.com/jerry460/translate-FHS-Filesystem-Hierarchy-Standard-to-Chinese/blob/main/contents/%E7%AC%AC%E4%B8%80%E7%AB%A0%20%E4%BB%8B%E7%BB%8D.md)
- 1.1 目的
- 1.2 关于本文的一些特殊字符的说明

### [2.文件系统](https://github.com/jerry460/translate-FHS-Filesystem-Hierarchy-Standard-to-Chinese/blob/main/contents/%E7%AC%AC%E4%BA%8C%E7%AB%A0%20%E6%96%87%E4%BB%B6%E7%B3%BB%E7%BB%9F.md)

### 3.根(Root)文件系统

- 3.1 目的
- 3.2 要求
- 3.3 具体选项
- 3.4 /bin:基本用户命令的二进制文件（面向所有用户）
  - 3.4.1目的
  - 3.4.2要求
  - 3.4.3 具体选项

- 3.5 /boot：引导加载程序的静态文件
  - 3.5.1目的
  - 3.5.2具体选项

- 3.6 /dev:设备文件
  - 3.6.1目的
  - 3.6.2具体选项

- 3.7/etc: 主机特定的系统配置
  - 3.7.2 目的
  - 3.7.2 要求
  - 3.7.3 具体选项
  - 3.7.4/etc/opt:/opt 的配置文件
    - 3.7.4.1 目的
    - 3.7.4.2 要求
  - 3.7.5 /etc/X11:X winows 系统的配置文件
    - 3.7.5.1 目的
    - 3.7.5.2 具体选项
  - 3.7.6 
