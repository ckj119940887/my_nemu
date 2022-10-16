# dependencies
```
sudo apt-get install flex bison build-essential man gdb git libreadline-dev libsdl2-dev 
sudo apt-get install llvm llvm-dev llvm-11 llvm-11-dev
```

# dowload sub-project
```
修改src/utils/filelist.mk
CXXFLAGS += $(shell llvm-config-11 --cxxflags) -fPIE
LIBS += $(shell llvm-config-11 --libs)

bash init.sh nemu 
bash init.sh abstract-machine

执行完init.sh后，会修改.bashrc
将添加到.bashrc中的内容放到.zshrc
```

# compile project
```
进入nemu目录
make menuconfig 不要作任何修改，退出就行
make
```
