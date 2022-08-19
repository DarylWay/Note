# Anaconda-虚拟环境

## 一 查看当前虚拟环境

使用

```
conda info --env
```

或者

```
conda env list
```

## 二 创建虚拟环境及一些常用命令 

### 1. 通过复制现有环境创建

```
conda create -n conda-env2 --clone conda-env1
```

### 2. 创建一个全新的环境

```
conda create -n env(虚拟环境名) python=3.x
# 可不指定python版本
```

### 3. 删除虚拟环境

```
conda remove -n env --all
```

### 4. 激活环境

```
conda activate env
```

### 5. 查看环境中已有的package

```
conda list
```

## 三 在jupyter notebook中使用虚拟环境内核

### 1. 激活虚拟环境

```
conda activate env
```

### 2. 安装ipykernel

```
pip install ipykernel
```

### 3. 在当前环境中打开jupyter notebook

```
jupyter notebook
```

### 4. 更改当前内核名称

base环境:

```
D:\Software\Anaconda\share\jupyter\kernels\python3
```

虚拟环境:

```
D:\Software\Anaconda\envs\envx\share\jupyter\kernels\python3
```

在该目录下修改kernel.json文件下的display-name即可修改对应环境内核的显示名称.