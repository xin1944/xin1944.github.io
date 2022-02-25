---
layout: post
comments: true
section-type: post
title: C++实现删除字符串中的空白字符
category: daily
tags: [ 'tutorial' ]
---

# 合理的创建标题，有助于目录的生成

## 插入链接与图片
![Alt](https://wx3.sinaimg.cn/mw2000/98b11d27ly1gz1osjww9jj21kw1kwh7i.jpg#pic_center)

## 如何插入一段漂亮的代码片

```C++
#include <algorithm>
// trim from start (in place)
static inline void ltrim(std::string &s) {
    s.erase(s.begin(), std::find_if(s.begin(), s.end(), [](unsigned char ch) {
        return !std::isspace(ch);
    }));
}

// trim from end (in place)
static inline void rtrim(std::string &s) {
    s.erase(std::find_if(s.rbegin(), s.rend(), [](unsigned char ch) {
        return !std::isspace(ch);
    }).base(), s.end());
}

// trim from both ends (in place)
static inline void trim(std::string &s) {
    ltrim(s);
    rtrim(s);
}

```


