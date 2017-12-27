
#### node在windows下的版本切换工具，原版不再维护,根据网上相关资料进行修改自用。
================================
#### 准备工作：
-------------

在安装nvmw之前需要安装:

- [git](http://code.google.com/p/msysgit/ "msysgit")
- [python 2.7+](http://python.org/download/) 只有在node版本小于0.8时需要

安装
------------

克隆git到本地或者下载zip文件到本地:

    git clone git://github.com/hakobera/nvmw.git "%HOMEDRIVE%%HOMEPATH%\.nvmw"

把nvmw所在目录加入到环境变量path中

    set "PATH=%HOMEDRIVE%%HOMEPATH%\.nvmw;%PATH%"

使用
-----

    命令:
      nvmw help                    命令帮助
      nvmw install [version]       下载和安装[version]版本
      nvmw uninstall [version]     卸载[version]版本
      nvmw use [version]           使用[version]版本
      nvmw ls                      已安装node版本列表

    例子:
      nvmw install v0.6.0          安装0.6.0版本
      nvmw use v0.6.0              使用0.6.0版本

### 支持不同架构下载

arch 支持这些值: `x86`, `x64`

    Usage:
      nvmw install [version] [arch]    安装某个架构的某个版本
      nvmw uninstall [version] [arch]  卸载某个架构的某个版本
      nvmw use [version] [arch]        使用某个架构的某个版本

    Example:
      nvmw install v0.12.0 x86         安装32位的0.12.0版本
      nvmw use v0.12.0 x86             使用32位的0.12.0版本


### 问题：


#### Q. 没有文件扩展js的脚本引擎

如果js有默认的打开程序，如vscode，则会出现这个提示，修复点这里 [here](https://jingyan.baidu.com/article/ff42efa93a7ad9c19e2202f0.html)