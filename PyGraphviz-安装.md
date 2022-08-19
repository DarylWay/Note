### 1. 安装 Graphviz

首先到官网下载对应的graphviz安装包(pygraphviz的依赖软件)

http://www.graphviz.org/download/

![image-20220819224212049](images/image-20220819224212049.png)

安装过程中选择添加环境变量

### 2. 测试 dot

在任意目录下vim一个sample.dot文件, 输入以下内容:

```
//dot simple.dot -Tpng -o simple1.png  -Gsplines=line  
digraph G {
  //a -> c;
  a -> b;
  b -> c;
  subgraph x{
      rank=same;
      b->d;
  }
  subgraph y{
      //rank = same;
      d->e;
  }
  subgraph z{
    rank=same;
    c->e;
  }

 }
```

cmd运行该文件:

```
sdot simple1.dot -Tpng -o simple1.png -Gsplines   
//-Gsplines=line  表示强迫边是直线.
```

若同目录下导出png图片, 则测试成功, 否则检查环境变量.

### 3. 安装 PyGraphviz

https://www.lfd.uci.edu/~gohlke/pythonlibs/#pygraphviz

下载对应python版本的whl到本地, cd到该目录下, 执行pip

```
pip install pygraphviz-1.3.1-cp34-none-win_amd64.whl
```

安装成功.