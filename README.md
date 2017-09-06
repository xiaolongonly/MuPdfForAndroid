[![CSDN](https://img.shields.io/badge/CSDN-@xiaolongonly-blue.svg?style=flat)](http://blog.csdn.net/guoxiaolongonly)
[![CSDN](https://img.shields.io/badge/PersonBlog-@xiaolongonly-blue.svg?style=flat)](http://xiaolongonly.cn/)
[![API](https://img.shields.io/badge/API-16%2B-green.svg?style=flat)](https://android-arsenal.com/api?level=16)


[mupdf](https://mupdf.com/)是一款轻量级的pdf浏览框架，而它的好处是支持很多第三方pdf框架没有的，文本的pdf文档搜索，标注等功能。当之无愧的强大。缺点是动态链接库实在大。


# 为什么推荐这个框架
我在[pdf框架一览](http://blog.csdn.net/guoxiaolongonly/article/details/76992138)中介绍过四种pdf框架，只有这个pdf框架功能最全最强大。而且封装方面包括对缩放,预览，缓存等的处理也值得借鉴。我将在之后研究这个库，还有他的java层封装，并将其做的更好!

# 怎么使用它？


```java

	Intent intent = new Intent(this, com.artifex.mupdflib.MuPDFActivity.class);
			intent.setAction(Intent.ACTION_VIEW);
			intent.setData(uri);
			
			//if document protected with password
			intent.putExtra("password", "encrypted PDF password");

			//if you need highlight link boxes
			intent.putExtra("linkhighlight", true);

			//if you don't need device sleep on reading document
			intent.putExtra("idleenabled", false);
			
			//set true value for horizontal page scrolling, false value for vertical page scrolling
			intent.putExtra("horizontalscrolling", true);

			//document name
			intent.putExtra("docname", "PDF document name");
			
			startActivity(intent);

```


由于界面是已经写死的，可以参照功能实现去修改界面。祝你好运~~ 



# License

```
Copyright 2017 Xiaolong 

MupdfForAndroid is free software: you can redistribute it and/or modify.

```
