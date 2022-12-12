---
title: "Re"
date: 2022-10-23T12:06:11+08:00
draft: true

description: ""
upd: ""

tags: []
categories: []
---

<!--more-->

[官方文档](https://docs.python.org/3/library/re.html)

正则表达式在线测试

- https://c.runoob.com/front-end/854/
- https://www.w3cschool.cn/tools/index?name=create_reg


### regular expression

语法：

- 字符匹配符：\d、\s、\w
- 位置匹配符：**\b**、^
- 反义匹配符：\D、\S、\W、^
- 分组：()
- 重复：[]
- 数量：+,*，{}
- 懒惰限定符：？

### re库

- re.compile(pattern,flags=0)
  - 生成的对象可以调用以下所有方法

- re.match(re, str, 修饰符flags)
  - 从字符串的开头开始匹配的，一旦开头不匹配，那么整个匹配就失败
  - 生成match对象：方法group、span
  - 修饰符：
    - re.S：绝大部分的HTML文本都包含了换行符，所以尽量都需要加上`re.S`修饰符，以免出现匹配不到的问题
    - re.I
- re.search()：扫描整个字符串，然后返回第一个成功匹配的结果
- re.findall()
- re.sub(pattern,repl, string,count=0,flags=0)
- re.split(pattern,string,maxsplit=0,flags=0)
- re.finditer(pattern,string,flags=0)
  - 每个迭代元素是match对象

- **macth**对象属性与方法

## 功能

单个连续重复字符大于 3 时，替换为仅重复 3 次。

```Python
def reduce_duplicate(text):
    '''
    Reduce character sequences >3 to 3
    e.g. buuuuuuy ---> buuuy
    '''
    duplicate = re.compile(r"(.)\1{2,}")
    return re.sub(duplicate, r"\1\1", text)
```

参考：

- **待改进**：[文本处理那些奇淫技巧——缩写词还原、单词去除重复字符和命名实体识别](https://blog.csdn.net/qq_40438165/article/details/84943819)
- [python使用正则表达式去除句子中的重复词](https://blog.csdn.net/zhongkeyuanchongqing/article/details/117920875)
- [正则匹配字符串中重复字符（串）](http://guoxiaoyang.xyz/2017/07/30/match-string-repeated-pattern/)
- [利用正则匹配连续重复的字符：\1](https://blog.csdn.net/qq_43523725/article/details/119377617)
- [正则表达式中\1 \2是什么意思](https://blog.csdn.net/weixin_43639512/article/details/84785585)

改进：单个连续重复字符大于 3 时，减少重复次数，直至单词有意义：

```Python
def reduce_duplicate(text):
    '''
    Reduce character sequences >=3 to raw word with all cap
    e.g. buuuuuuy ---> BUY
    '''
    duplicate = re.compile(r"[a-zA-Z]*([a-zA-Z])\1{2,}[a-zA-Z]*")
    for item in re.finditer(duplicate, text):
        raw_word = item.group(0)
        if dictionary.check(re.sub(r"([a-zA-Z]*?)([a-zA-Z])\2{2,}([a-zA-Z]*?)", r"\1\2\2\3", raw_word)):
            new_word = re.sub(r"([a-zA-Z]*?)([a-zA-Z])\2{2,}([a-zA-Z]*?)", r"\1\2\2\3", raw_word)
            text = text.replace(raw_word, new_word.upper())
        elif dictionary.check(re.sub(r"([a-zA-Z]*?)([a-zA-Z])\2{2,}([a-zA-Z]*?)", r"\1\2\3", raw_word)):
            new_word = re.sub(r"([a-zA-Z]*?)([a-zA-Z])\2{2,}([a-zA-Z]*?)", r"\1\2\3", raw_word)
            text = text.replace(raw_word, new_word.upper())
    return text
```

Remove hashtags if not in Reuters corpus.

```Python
def remove_hashtag(text):
    '''
    The hashtag prefix from the token is deleted if that token is present in the NLTK Reuters English corpus.
    If the token is not present in the dictionary, the entire hashtag is removed from the text.
    '''
    Reuters = pickle.load(open("Corpora/Reuters.pickle", "rb"))

    hash = re.compile("#(\w+)")
    hashtags = re.findall(hash, text)
    if hashtags:
        for hashtag in hashtags:
            if hashtag not in Reuters:
                text = re.sub("#" + hashtag, "", text)

        text = re.sub("#", "", text)
        return text
    else:
        return text
```

参考：

- [Python 解析tweet以将hashtag提取到数组中](https://duoduokou.com/python/40729872522172902777.html)

只要字符串里面包含数字，就被删除

```Python
def remove_numerical(text):
    '''
    Remove tokens with numerical characters
    '''
    numerical = re.compile("\s[\w]*[0-9]+[\w]*\s")
    return re.sub(numerical, " ", text)
```

仅删除单独的数字

```Python
def remove_numerical(text):
    '''
    Remove tokens with numerical characters
    '''
    numerical = re.compile("\s-?(,?\d+)*(\.\d+)?\s")
    return re.sub(numerical, " ", text)
```