# Transdoc

## 概述
- - -
Transdoc的目标是快速地将word文档转换为格式一致的Markdown文件，目前支持图片/表格/段落的识别和提取，单一文字样式(仅黑体或仅斜体)；暂未支持无序列表，无法识别嵌套列表，需手动校验。

Markdown是一门专注于文档结构的语言工具，可十分方便地将md转换为html。但是需要注意的是，markdown重点关注于信息的内容，而不是显示的效果，因此markdown不应包含任何样式定义的内容，如有需要,应使用额外的css来定义样式。

本工具适用于生成符合规范的md文本，不推荐使用带有html标签和css样式的md文本内容。但是在特殊情况下(比如，表格单元格内容中的段落换行)，工具会使用html标签“&lt;br&gt;“来代替换行符号“\n“。

markdown支持两种标题的编写格式，分别是Setext和atx，本工具使用atx格式生成标题，优点在于可以支持与html同样数量的标题级别(6级)。atx的标题格式如下：  

	# 一级标题  
	## 二级标题  
	### 三级标题  
	...

## Doc文件编写格式说明
- - -
#### 要求:
- 标题(**重要**)：
    1. 文档的标题使用大纲级别1级；
    2. 章节和子标题须使用正确的大纲级别定义(2级和以上大纲级别)，并去除列表自动编号。

- 列表：
    1. 长的正文段落使用列表，简短的标题使用标题；
    2. 任何列表前的序号和正文段落之间需用一个空格隔开；
    3. 列表可用两种方式：  
        1) 设置列表符号或列表编号;  
        2) 不设置项目符号和编号，按markdown格式手动添加列表符号，如:[+、-、*、1.] 等等；

- 表格：
    1. 插入脚本及代码时，需要使用1x1的表格，即单个单元格，本工具将识别其为代码块。正常文本内容请勿使用单个独立的单元格；
    2. 由于markdown缺少支持，不要使用合并单元格，本工具可能成功通过转换，但不能保证格式正确，尽量使用没有合并单元格的表格；

- 正文：
    1. 插入url链接需独立一行，后面带一个空格。

#### 建议:
1. 为了生成结果的md文档内容和显示效果美观，尽可能地减少列表嵌套的层级。同时，由于列表存在缩进，过多的缩进会导致页面每行可显示的内容减少。
2. 尽量利用上6级标题的优势，同时你可以自定义有序标题的序号格式，如：[第一章，1)，一、]，这样做可以避免md种有序列表只能采用“1.”来表示的短板

## 软件使用说明
- - -
下载获取分发包transdoc-bin.zip，解压到任意目录，点击run.bat即可执行程序，程序将扫描./docs目录下的doc文件并进行转换，输出到./docs目录中。  
或者解压后打开how_to_use.txt阅读使用说明。

## Demo演示
- - -
本章节将展示以往的测试文档转换结果地址,供文档编写人员查看,以便于文档编写人员对文档结构进行改进和统一,并对本工具存在的问题进行合理的建议.意见和建议可以在issue提出.

地址: