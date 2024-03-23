# Node.js安装&Vue3安装

[TOC]

# 一、安装Node.js

## （一）下载安装包

官网地址【英文】：[Node.js — Download Node.js® (nodejs.org)](https://nodejs.org/en/download)

官网地址【中文】：[下载 | Node.js 中文网 (nodejs.cn)](https://nodejs.cn/download/)

*下载地址任选其一即可*

## （二）安装程序

### 1. 点击Next

![img](https://img-blog.csdnimg.cn/9369d0597b874c7897757e9aa9b00861.png)

### 2. 修改路径到D盘，点击Next

![img](https://img-blog.csdnimg.cn/259f228be12d412488001e8e40e3f0d2.png)

### 3. 默认，点击Next

![img](https://img-blog.csdnimg.cn/e25af67216e34076ac456d9813376ee8.png)

### 4. 不选中，点击Next

![img](https://img-blog.csdnimg.cn/723ca00461b14107a04141f5bd1ef1af.png)

### 5. 点击Install

![img](https://img-blog.csdnimg.cn/6e61d654e92e454fb1d9c0dd83aa4f7a.png)

### 6. 点击Finish

![img](https://img-blog.csdnimg.cn/c48b41f81f70447e9679fbcfe6d509b8.png)

### 7. 测试安装是否成功

在使用管理员身份打开命令行【在任务栏的搜索栏中搜索“命令提示符”，点击“以管理员身份运行”】中测试

```
node -v
// 显示node.js版本

npm -v
// 显示npm版本
```

![image-20240323212045732](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323212045732.png)



# 二、配置环境

## （一）配置默认安装目录和缓存日志目录

### 1. 创建目录

找到安装的目录，在安装目录下新建两个文件夹【node_global】和【node_cache】

![image-20240323212247241](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323212247241.png)

### 2. 配置目录

*此时仍然以管理员身份打开命令行*

```
npm config set prefix "D:\Program Files\nodejs\node_global"
// npm config set prefix “你的路径\node_global”（复制你刚刚创建的“node_global”文件夹路径）

npm config set cache "D:\Program Files\nodejs\node_cache"
// npm config set cache “你的路径\node_cache”  （复制你刚刚创建的“node_cache”文件夹路径）
```

## （二）配置环境变量

### 1. 进入环境变量窗口

- 右键“此电脑”
- 点击”属性"
- 点击“高级系统设置”
- 点击“环境变量”

### 2. 配置系统变量

在系统变量下新建 NODE_PATH 变量，输入默认安装目录 node_global 下的 node_modules 的路径

```
NODE_PATH
D:\Program Files\nodejs\node_global\node_modules
```

![image-20240323213055058](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323213055058.png)

进入系统变量的Path，输入nodejs安装路径【可能已经存在】

```
D:\Program Files\nodejs\
```

![image-20240323213204472](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323213204472.png)

### 3. 配置用户变量

进入用户变量的Path，输入 nodejs 默认的模块调用路径

```
D:\Program Files\nodejs\node_cache
D:\Program Files\nodejs\node_global
```

![image-20240323213310205](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323213310205.png)

***【全部配置完后，别忘了点确定！】***



# 三、配置淘宝镜像

*此时仍然以管理员身份打开命令行*

## 1. 安装 cnpm

请注意此处协议为**http**而不是*https*

```
npm install -g cnpm --registry=http://registry.npm.taobao.org
```

![image-20240323215916033](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323215916033.png)

## 2. 测试安装是否成功

```
cnpm config get registry
```

![image-20240323215924966](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323215924966.png)

# 四、安装vue及相关包

*此时仍然以管理员身份打开命令行*

## 1. 安装vue.js

```
cnpm install vue -g
```

![image-20240323214054031](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323214054031.png)

## 2. 测试安装是否成功

```
cnpm info vue
```

![image-20240323214140582](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323214140582.png)

```
npm list vue
// 输出有内容最好，但是输出为空也没关系
```

![image-20240323214202910](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323214202910.png)

## 3. 安装 webpack 模块

```
cnpm install webpack -g
```

![image-20240323214326890](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323214326890.png)

```
cnpm install --global webpack-cli
```

![image-20240323214444144](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323214444144.png)

## 4. 安装vue-cli3.x

```
cnpm install @vue/cli -g
```

![image-20240323214515253](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323214515253.png)

![image-20240323214538934](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323214538934.png)

![image-20240323214616153](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323214616153.png)

![image-20240323214633225](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323214633225.png)



# 五、创建vue3项目

*此时仍然以管理员身份打开命令行*

## 1. 安装Yarn

```
cnpm install -g yarn
```

![image-20240323215313848](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323215313848.png)

## 2. 测试安装是否成功

```yarn -v
yarn -v
```

![image-20240323215402435](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323215402435.png)

## 3. 创建项目

进入想要创建项目的目录（可不进入）

```
cd 目录
```

创建项目

```
vue create demo
// vue create [项目名称]
```

![image-20240323215431366](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323215431366.png)

根据给出的提示进入项目目录，运行项目

```
cd demo
yarn serve
```

![image-20240323215515126](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323215515126.png)

## 4. 测试创建是否成功

根据给出的提示在浏览器打开`http://localhost:8080/`或`http://10.202.227.170:8080/`，出现以下界面即为成功

![image-20240323215653132](C:\Users\DELL\AppData\Roaming\Typora\typora-user-images\image-20240323215653132.png)