Quick start

0)
Mac下面建议用pyenv 来选择特定的python版本。
Mac自带的python就是个傻缺。。。

1）
下载代码<br> git clone https://github.com/chinesejie/broc.git chinesejie/broc

安装protobuf<br> 进入到tools目录执行sh install protobuf, protobuf被安装在$HOME/protobuf目录下

处理proto文件<br> 进入到tools目录下面执行sh install proto, 生成broc自用的py文件. 生成过程是：使用了$HOME/protobuf/bin/protoc程序根据 proto/BrocModule.proto文件生成了dependency/BrocModule_pb2.py代码。

设置PATH<br> 将broc的client目录设置到PATH中， 例如：export PATH=$HOME/broc/client:$PATH

2)
export PATH=$BROC_HOME/client:$PATH
很别扭。

所以直接 来个软链。。
cd $BROC_HOME<br>
ln -s client/broc broc.py<br>
ln -s client/Options.py Options.py<br>
ln -s client/Scratch.py Scratch.py<br>
ln -s client/TaskMaster.py TaskMaster.py<br>
ln -s client/TaskWorker.py TaskWorker.py<br>
这样可以在pycharm里面直接运行 broc.py<br>


运行：
cd $BROC_HOME<br>
./broc.py build
