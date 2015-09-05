### stackedit：开源世界的markdown利器，让你随时随地做笔记、做记录
##### 关键字：stackedit markdown 写书 笔记 记录 跨平台 开源

工作的时候经常需要做很多的工作日志、笔记、购物清单、会议纪要，闲暇的时候也许心血来潮想在朋友圈发篇感想、文章。用word已经是很落伍的时期，相信很多人在电脑里面早就装好了诸如 TO－DO、evernote这样的软件来应对。
现在想向你推荐的是基于markdown标准的一个开源服务：stackedit.io。你不需要安装任何软件，只要你的设备能上网（电脑、手机），就可以随时记录你的想法。What's more？你的笔记全部记录在你的浏览器的存储空间中，不用担心个人隐私问题。当然，你也可以导出、上传到本地，或者类似dropbox、wordpress、github这样的公众服务平台。你甚至可以通过ssh协议将文件备份到你自己的linux服务器上。另外，由于stackedit是开源的，你甚至可以在自己的服务器上用node搭建服务器，供他人使用。
    
#### 有人要问什么是markdown？
markdown是一种文档撰写语法，近年在github的带动下，已经成为一种新的文档标准。它超级简单，但却可以让你在不碰鼠标的情况下，一次性流畅的把你想写的内容全部记录下来,避免频繁的鼠标操作阻碍了思路的延续。现在它已经成为几十万程序猿事实上的文档撰写标准，许多科技类作家也开始在github上用markdown语法写书。
有了markdown，你可以基本不用考虑字体、排版问题，写作时只要知道哪些是标题一、标题二、标题三，哪些是正文就可以了，真正是随手“mark down"。markdown还为超链接、图片、to－do列表、表格、插入式代码等日常要用的提供了方便的语法工具。你甚至可以用markdown语法画流程图，写一些专业的数据公式，这些功能以前往往需要借助专业工具才能做到，现在只需要用markdown语法就可以轻松实现。
举几个简单的例子给各位看官管窥一下：
##### **示例一：**
```
# 标题一
## 标题二
### 标题三
#### 标题四
```
在markdown编辑器中输入以上内容，将得到以下显示：

----
# 标题一
## 标题二
### 标题三
#### 标题四
----
##### **示例二(流程图）：**

```
```flow
st=>start: Start
e=>end
op=>operation: My Operation
cond=>condition: Yes or No?

st->op->cond
cond(yes)->e
cond(no)->op
```
在markdown编辑器中输入以上内容，将得到以下显示：

---
```flow
st=>start: Start
e=>end
op=>operation: My Operation
cond=>condition: Yes or No?

st->op->cond
cond(yes)->e
cond(no)->op
```
**有没有亮瞎眼?**
##### **示例三(列表）：**
```
*   Red
*   Green
*   Blue
```
在markdown编辑器中输入以上内容，将得到以下显示：

----
*   Red
*   Green
*   Blue

----

markdown还支持代码文本的语法高亮功能，可以将几十种不同的编程语言高亮显示。本文不是一篇markdown语言的介绍帖，感兴趣的看管可以跳转到传送门学习：[传送门](http://www.markdown.cn/)
#### markdown 我知道，但为什么要用stackedit？
##### 理由1：
随便搜索一下，就可以在网上找到很多种markdown工具。大多数是下载到本机，或者是一个浏览器的扩展程序，集成到浏览器中；又或者直接是一个网站，需要登录到网站上运行，不少还要收费。
那么有没有**免费+到处可用+文档上传服务器**的选择呢？目前看来只有stackedit 
##### 理由2：
stackedit除了支持markdown标准语法以外，还额外增加了对流程图、数学公式、脚注等语法，灵活度提高很多。流程图语法简直是我的大爱，简单的流程图再也不用跑到visio里面画来画去了，描述好对象和连接关系，一个漂亮的图就跃然纸上。
##### 理由3：
stackedit在文档的转换和导出上花了很多功夫，你可以将markdown文档按照markdown格式、html格式、自定义模版格式、甚至pdf格式（收费功能）导出。另外它还有反向转换功能，可以将html页面反向转换为markdown。另外，它还支持crouchdb、dropbox、google drive的同步功能。
令人感到惊喜的一个功能是，它甚至可以将你的文档，自动通过ssh发送到另外一台主机上，实现文档的备份。这样就不用担心一些敏感资料不小心在互联网散播了。

#### 我已经等不及了，要怎么才能用上stackedit？
很简单，只要在浏览器中输入：https://stackedit.io/editor, THIS IS IT！

#### stackedit漂亮又好用，如何自己搭建服务器？
ok，既然你问了这个问题，那我默认你就至少是个程序猿了。
##### step1
	确认你已经正确的配置了git
##### step2
	确认你已经正确的安装了node，npm，bower
##### step3
```
git clone https://github.com/benweet/stackedit.git //下载源代码
cd stackedit  
npm install    //安装必要的node module
bower install
export PORT=8080 && node server.js  //运行程序
```
完成以上工作，你就可以在自己的浏览器上通过以下地址访问了：https://localhost:8080/editor


	





