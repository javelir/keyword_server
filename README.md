[![Build Status](https://travis-ci.org/yanyiwu/keyword_server.png?branch=master)](https://travis-ci.org/yanyiwu/keyword_server)
- - -

# 微型中文关键词抽取服务

## 简介

`keyword_server` 是一个基于 [CppJieba] 包装而成 **中文关键词抽取服务** 。

[CppJieba] 项目自带 **关键词抽取** 的功能， 但是没有包装成服务，本来想改进 [CppJieba] 使之支持该服务。

但是考虑再三，为了避免 [CppJieba] 变得越来越臃肿，所以将该需求单独出来做成该项目。

这样好处也很明显，代码清凉解暑，不到50行代码的 `server.cpp` 就可以编译出一个 **中文关键词抽取服务** 。

## 特性

+ 支持`utf-8`编码。
+ 使用 `TF-IDF` 抽取算法。
+ 支持 GET 和 POST 请求。

## 用法

### 依赖

* `g++ (version >= 4.1 recommended) or clang++`;

### 下载

```sh
git clone git://github.com/yanyiwu/keyword_server.git
cd keyword_server
make
#如果是MacOSX用户，请使用 make osx 。
```

### 启动服务

```
./keyword.server
```

### Demo脚本 

```
./curl.demo
```
 
curl.demo 里面包含 GET 和 POST 请求 。
因为 GET 请求有长度限制，当要对长文进行关键词抽取时，请使用 POST 请求。

## 客服

```
i@yanyiwu.com
```

[CppJieba]:https://github.com/yanyiwu/cppjieba
[simhash]:https://github.com/yanyiwu/simhash
