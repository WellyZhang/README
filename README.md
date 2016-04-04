# Introduction
This is a brief English introduction to `GitHub Flavored Markdown`, or `GFM`. Markdown has been adopted for its implicity and expressiveness over a wide range of applications and the specfic version from GitHub adds a myriad of extensions to it, only making it more than popular among programmers.

Now we are going to explore a little bit in depth of it.

Note that GFM also supports HTML.

## Headers
Use 1 ~ 6 '#'s to indicate header level. You can't really make a header bold, but you can italicize certain words(to be discussed later).

# Header One
## Header Two
### Header Three
#### Header Four
##### Header Fix
###### Header Six
###### _Italic Header Six_


## Text
### Italics
Surround words with underscores \_ to _italicize_ words.
### Bold
Surround words with two asterisks \*\* to make them **bold**.
### Combination of Italics and Bold
Surround with \*\*\_ like **_Italics and Bold_**.
### Straigh-through
Surround words with ~~ for ~~straight-through~~.
### Hightlight
Surround words with \` to `highlight`.
### Escape
Use \ for for escape.
### Newline
Use double blanks at the end of each line for soft break  
while use /n between lines for hard break such as

this.

## Links
###链接外部URL
[我的博客](http://blog.csdn.net/guodongxiaren "悬停显示")   语法如下：
```
[我的博客](http://blog.csdn.net/guodongxiaren "悬停显示")
```
###链接的另一种写法
[我的博客][id]  

[id]:http://blog.csdn.net/guodongxiaren "悬停显示"   
语法如下：
```
[我的博客][id]
[id]:http://blog.csdn.net/guodongxiaren "悬停显示"
```
中括号[ ]里的id，可以是数字，字母等的组合。这两行可以不连着写，**一般把第二行的链接统一放在文章末尾**，id上下对应就行了。这样正文看起来会比较干净。

###链接本仓库里的URL
[Book](./Book)
语法如下：
```
[Book](./Book)
```
如果文件要引用的文件不存在，则待点击的文本为红色。引用的文件存在存在则文本为蓝色。
###锚点
我们可以使用HTML的锚点标签（`#`）来设置锚点：[回到目录](#index)  
但其实呢，每一个标题都是一个锚点，不需要用标签来指定，比如我们 [回到顶部](#TEST)
不过不幸的是，由于对中文支持的不好，所以中文标题貌似是不能视作标签的。

##<a name="pic"/>显示图片
###来源于网络的图片
![baidu](http://www.baidu.com/img/bdlogo.gif "百度logo")
![](https://assets-cdn.github.com/images/modules/contact/goldstar.gif)

###GitHub仓库中的图片
![](https://github.com/guodongxiaren/ImageCache/raw/master/Logo/foryou.gif)
###<a name="piclink">给图片加上超链接
####第一种

[![head]](http://blog.csdn.net/guodongxiaren/article/details/23690801)
[head]:https://github.com/guodongxiaren/ImageCache/raw/master/Logo/jianxin.jpg "点击图片进入我的博客"

#### 第二种
[![内容任意](http://www.baidu.com/img/bdlogo.gif "百度logo")](http://www.baidu.com)




##<a name="dot"/>列表
###圆点列表
* 昵称：果冻虾仁
* 别名：隔壁老王
* 英文名：Jelly

###更多圆点
* 编程语言
    * 脚本语言
        * Python

###数字列表
####一般效果
就是在数字后面加一个点，再加一个空格。不过看起来起来可能不够明显。    
面向对象的三个基本特征：

1. 封装
2. 继承
3. 多态

####数字列表自动排序
也可以在第一行指定`1. `，而接下来的几行用星号`*`（或者继续用数字1. ）就可以了，它会自动显示成2、3、4……。    
面向对象的七大原则：

1. 开闭原则
* 里氏转换原则
* 依赖倒转原则
* 接口隔离原则
* 组合/聚合复用原则
* “迪米特”法则
* 单一直则原则

####多级数字列表
和圆点的列表一样，数字列表也有多级结构：  

1. 这是一级的数字列表，数字1还是1
   1. 这是二级的数字列表，阿拉伯数字在显示的时候变成了罗马数字
      1. 这是三级的数字列表，数字在显示的时候变成了英文字母
	    1. 四级的数字列表显示效果，就不再变化了，依旧是英文字母

### 复选框列表
- [x] C
- [x] C++
- [x] Java
- [x] Qt
- [x] Android
- [ ] C#
- [ ] .NET

您可以使用这个功能来标注某个项目各项任务的完成情况。
##<a name="blockquotes"/>块引用

###常用于引用文本
####文本摘自《深入理解计算机系统》P27
　令人吃惊的是，在哪种字节顺序是合适的这个问题上，人们表现得非常情绪化。实际上术语“little endian”（小端）和“big endian”（大端）出自Jonathan Swift的《格利佛游记》一书，其中交战的两个派别无法就应该从哪一端打开一个半熟的鸡蛋达成一致。因此，争论沦为关于社会政治的争论。只要选择了一种规则并且始终如一的坚持，其实对于哪种字节排序的选择都是任意的。
><b>“端”（endian）的起源</b><br>
以下是Jonathan Swift在1726年关于大小端之争历史的描述：<br>
“……下面我要告诉你的是，Lilliput和Blefuscu这两大强国在过去36个月里一直在苦战。战争开始是由于以下的原因：我们大家都认为，吃鸡蛋前，原始的方法是打破鸡蛋较大的一端，可是当今的皇帝的祖父小时候吃鸡蛋，一次按古法打鸡蛋时碰巧将一个手指弄破了，因此他的父亲，当时的皇帝，就下了一道敕令，命令全体臣民吃鸡蛋时打破较小的一端，违令者重罚。”

###块引用有多级结构
>数据结构
>>树
>>>二叉树
>>>>平衡二叉树
>>>>>满二叉树

##<a name="code"/>代码高亮
```Java
public static void main(String[]args){} //Java
```
```c
int main(int argc, char *argv[]) //C
```
```Bash
echo "hello GitHub"#Bash
```
```javascript
document.getElementById("myH1").innerHTML="Welcome to my Homepage"; //javascipt
```
```cpp
string &operator+(const string& A,const string& B) //cpp
```
##<a name="table"/>显示表格
表头1  | 表头2
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell

| 表头1  | 表头2|
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

| 名字 | 描述          |
| ------------- | ----------- |
| Help      | Display the help window.|
| Close     | Closes a window     |

表格中也可以使用普通文本的删除线，斜体等效果

| 名字 | 描述          |
| ------------- | ----------- |
| Help      | ~~Display the~~ help window.|
| Close     | _Closes_ a window     |

表格可以指定对齐方式

| 左对齐 | 居中  | 右对齐 |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |

表格中嵌入图片

| 图片 | 描述 |
| ---- | ---- |
![baidu](http://www.baidu.com/img/bdlogo.gif "百度logo") | baidu

#<a name="emoji"/>Emoji
GFM supports Emoji naively. To display emoji, surround the name of the expression with two `:`s.  
E.g. `:blush:` :blush:  

GitHub has a [Emoji cheatsheet](http://www.emoji-cheat-sheet.com), but for your convenience I've also included it in the [repo](./emoji.md).

# Acknowledgement

I'm grateful for developers of [Markdown Tutorial](http://www.markdowntutorial.com/) which provides basics and fundamentals on how to write a startup Markdown file,  for his thorough explaination of GFM in Chinese and authors of the Markdown Cheat Sheet whose summarization is right to the point.
