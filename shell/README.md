# 一些简单的Linux shell脚本
> 每次搭建新的服务器避免不了安装一些新的软件，Docker,Git,JAVA,Maven,NodeJS等,为了方便这些软件的安装。编写一键安装脚本，一键执行，让每一台服务器的软件安装保持一样的风格

### 写在最前面！！！

强烈建议运行脚本的时候先创建一个空白文件夹 然后，再在空白文件夹里面运行脚本 安装软件，因为脚本里面有一些删除命令，防止删除自己电脑其他同名或者其他类似名称的文件。

### 错误解决
1. `/bin/bash^M:` 坏的解释器：没有那个文件或目录
> 问题是部分脚本是在Windows下用vscode写的；在win下编辑的时候，换行结尾是`\n\r` ;而在linux下 是`\n`，所以才会有 多出来的`\r`
- 解决办法 Linux终端运行 `sed -i 's/\r$//' 对应脚本名称`
  
  例如 `sed -i 's/\r$//' docker-centos.sh` 
