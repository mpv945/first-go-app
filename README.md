# first-go-app
vscode开发谷歌的go语言

# 开发环境搭建
  1. 安装go插件
  2. 配置go环境，https://golang.org/下载对应的go；环境变量增加GOROOT:解压目录
     Linux/macOS配置：vim ~/.profile  在文件末尾加入
       export GOROOT=/usr/local/go
       export PATH=$PATH:GOROOT/bin
    配置完后执行source ~/.profile
    最后输入go version验证是否配置成功
  3. 配置delve，在GOROOT下找到src\github.com\derekparker没有就新建（空文件夹），切换到该目录执行git clone https://github.com/derekparker/delve.git，然后cd GOROOT下找到src目录；执行go get -u github.com/derekparker/delve/cmd/dlv
# 新建项目
1. 打开文件---》首选项---》设置---》工作区设置。在项目下生成settings.json ；参考配置
2. ctrl+shift+D 打开debug。如果没有配置launch.json 在设置图标有小红点。点击设置，会自动生成配置。然后点击运行就能运行该go语言了