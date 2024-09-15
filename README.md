1.将Simulink文件生成的压缩文件解压，至本源码的根目录，此时本目录的文件关系为

复制前的根目录结构
```
|--.gitignore
|--CMakeLists.txt
|--README.md
```

复制后的根目录结构
```
|--\code
|--\R2021a
|--.gitignore
|--CMakeLists.txt
|--README.md
```

2.创建build文件夹

3.进入build文件夹，执行cmake ..命令

4.执行make命令

5.在根目录会看到libsimodel_win64.so文件
