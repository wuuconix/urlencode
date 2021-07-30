# url编码[字母和数字版]

## 背景

在做ctf题目的时候遇到过很多次url二次编码的问题，在这种情况下很可能需要知道一个字母比如`a`的url编码值。但是当我们使用`urllib.parse`的时候，它无法返回我们需要的结果。

![image-20210730152804070](https://gitee.com/Wuuconix/image_host/raw/master/image-20210730152804070.png)

这也不难理解，因为在普通的url编码里，26个英文字母和数字都是不需要编码的。

但是我们现在就想要知道`a`的编码值怎么办呢？

<img src="https://gitee.com/Wuuconix/image_host/raw/master/image-20210730152950694.png" alt="image-20210730152950694" style="zoom:50%;" />

之前我都是去网上查url编码对照表。但是这个操作很麻烦，当你vscode里指舞飞扬即将写出一个payload脚本的时候，发现python无法获得`a`的url编码值，便只能去浏览器里搜索`url编码表`，这种方法会有很强大的割裂感，也不够优雅。

于是我写了这个url编码脚本，它仅支持0-9, a-z, A-Z，当然这也够了，其他的完全可以用urllib.parse来获得。

## 使用方法

1. 单字符编码

```python
python3 urlencode a
```

![image-20210730153443720](https://gitee.com/Wuuconix/image_host/raw/master/image-20210730153443720.png)

2. 字符串编码

```python
python3 urlencode.py -m wuuconixyyds
```

![image-20210730153553713](https://gitee.com/Wuuconix/image_host/raw/master/image-20210730153553713.png)

这里的`-m`取意自`multiple`