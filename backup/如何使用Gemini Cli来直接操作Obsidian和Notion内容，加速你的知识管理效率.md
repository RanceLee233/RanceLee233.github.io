
主题类别/链接：[[输出]]、[[教程存档]]

# 前言
近期谷歌推出了Gemini Cli，可以直接在终端上运行AI。作为电脑小白的我之前几乎没有接触过终端和命令行。但是在AI的帮助和一段时间的运用后，我发现在终端中运行AI相比客户端或者浏览器有独特的优势，尤其是对于知识管理来说：
1. 之前我们和AI交互内容，必须把内容粘贴进去或者上传文件，修改后再重新粘贴回来，十分的麻烦。而终端可以直接在本地文件夹运行，直接修改你的文件，免去来回粘贴的烦恼。这一点对Obsidian用户来说特别友好
2. Gemini Cli可以连接Notion MCP，让AI来帮你查询、修改Notion中的文件。用户再也不用手动设计模板、关联内容和写公式了。你只要把自己的需求告诉他就可以了
3. 结合以上两点，不管是本地的Obsidian还是云端的Notion，都可以用Gemini Cli来协助。如果你也用这两款软件，希望这篇文章能帮助你

#  如何安装及使用Gemini Cli
## 关于Gemini Cli你需要知道的知识
1. Gemini是谷歌推出的AI，由于众所周知的原因，你需要自己会翻墙及有谷歌账号
2. 普通用户，每天可以通过Gemini Cli免费调用顶尖的Gemini-2.5-pro 1000次，对于个人用户来说基本上用不完

## 具体安装过程
由于我主要用的是Macbook，因此只介绍Mac系统上的安装方法：
1. 打开你的终端，具体方法是点击屏幕右上角的放大镜，然后输入“terminal”![202507181da0acc5ff4ea4249d4775523b25deba|image-1|600x95](https://cf-img.discoverlabs.ac.cn/202507181da0acc5ff4ea4249d4775523b25deba.webp)
2. 在打开的界面中输入代码（如果有报错，你可以直接复制到现有的AI里面去问问）
```
npx https://github.com/google-gemini/gemini-cli
```
![20250718bde7610f41a8c690e142851ff57ebebd|image-2|573x345](https://cf-img.discoverlabs.ac.cn/20250718bde7610f41a8c690e142851ff57ebebd.webp)
3. 安装完成后，再次打开终端，输入Gemini就可以启动它（注意部分用户不仅需要梯子，还需要虚拟网卡）
4. 第一次登录需要授权，直接按回车在跳出来的网页登录你的谷歌账号即可
5. 当出现这个界面后，你就可以输入和AI聊天了，聊天中AI有时候会和你要授权，我一般全部无脑Yes
 ![202507189b1fb5dc97e2cf35a24a376f65c6e3d3|image-3|976x539](https://cf-img.discoverlabs.ac.cn/202507189b1fb5dc97e2cf35a24a376f65c6e3d3.webp)

# 如何用Gemini Cli管理Obsidian或其它本地文件
## 如何进入存放Markdown文件的地址
如果你是直接打开终端进入Gemini Cli，那么你会在根目录。但是我们的很多Obsidian文件都在特定的目录，这时候就需要你告诉终端你要去那个目录运行AI，以下是具体步骤：
1. 打开你存放文件的文件夹，在下方右键文件夹选择在终端中打开
![image-2|1257x848](https://cf-img.discoverlabs.ac.cn/2025071867bbaa5eaa113242ec85188d0bc839fb.webp)
2. 当打开的终端左下角显示你要打开的文件夹，就说明你来对地方了
![image-3|1170x742](https://cf-img.discoverlabs.ac.cn/202507182100de0415094efbb146ed5923586427.webp)
3. 然后再输入Gemini，那么你的AI就自动在这个文件夹里面运行了

## Gemini Cli能帮我们的Obsidian做什么？
对于AI来说，markdown格式是十分方便读取和操作的文件，我们可以直接让AI：
1. 查看文件夹里面有多少文件
2. 查找提到某个主题/关键字的文件
3. 直接对文章内容修改
4. 任何你能做到的操作，AI都能做到
![20250718223181560f13754f8b9d38113897475c|image-10|1060x762](https://cf-img.discoverlabs.ac.cn/20250718223181560f13754f8b9d38113897475c.webp)

具体来说，日常使用中我会让AI：
1. 让AI直接查看文件，确认里面有没有错别字，有的话直接修改
2. 把某些内容转换成markdown格式的表格，OB中写表格很麻烦，我们可以让AI直接帮我写
3. dataview是很好用的查询和管理插件，但是像我一样的小白根本不会写代码，这时候你就可以要求它在某个文件里面写代码，来帮你查询某些内容

#  如何用Gemini Cli来管理Notion MCP
Gemini Cli不仅能管理我们的本地文档，还可以利用MCP来连接我们的Notion，让我们用自然语言直接操作AI来管理Notion

## 如何安装Notion MCP
让Gemini来管理Notion，我们需要先安装MCP。用户自己配置MCP服务对大部分人来说都十分麻烦，好在我们可以让AI自己管理自己：
1. 登录Gemini，然后输入：“查看网址https://developers.Notion.com/docs/get-started-with-mcp内容，使用STDIO (Local Server)来给我的Gemini Cli 安装Notion MCP”，之后AI就会自己查找安装（注意请在根目录打开终端，也就直接打开终端启动Gemini，不要在别的文件夹里面启动）
```
查看网址https://developers.Notion.com/docs/get-started-with-mcp内容，使用STDIO (Local Server)来给我的Gemini Cli 安装Notion MCP
```
1. 安装完成后，会跳出来Notion的授权网页，直接授权确认就可以了。之后在Gemini的界面，你可以看到下面提示你已经装了MCP（我装了2个）。而如果你输入命令/MCP再敲回车，能看到你所有安装的MCP。当看到Notion就说明成功了
![20250718593e8b6529fff56102cc1ef13a9d9cda|image-11](https://cf-img.discoverlabs.ac.cn/20250718593e8b6529fff56102cc1ef13a9d9cda.webp)

## Gemini Cli 能帮我们的Notion做什么
连接成功后，我们就可以让Gemini Cli来直接操作我们的Notion了，例如让他来查找一篇文章。请注意，指令中一定要说“请用Notion MCP”这几个字，不然有概率AI不知道要调用它。
![202507181a439898ea1af198706ac3423d057185|image-12](https://cf-img.discoverlabs.ac.cn/202507181a439898ea1af198706ac3423d057185.webp)
![20250718b3291c842c8eca56c22ee02a3140a517|image-13](https://cf-img.discoverlabs.ac.cn/20250718b3291c842c8eca56c22ee02a3140a517.webp)

类似的，我们可以给出更多指令：
1. 总结概括页面
2. 直接在文章或者表格中中插入内容
3. 甚至，我们要求做模板，AI也可以直接帮我们做出来，还能在其中填充公式
4. 任何你能想到的要求

# 其它
1. 如何在终端里面让AI读取图片？有两个方法：
	1. 把图片保存到AI进入的文件夹，直接告诉AI去读取
	2. 截图后复制，然后在终端中按快捷键control+c，不过这个方法AI会在这个文件夹中创建一个隐藏的Gemini文件夹，并且把图片保存在里面，用完后请记得删除
![202507180759aba6be88c1d74621c9d4621f6a5a|image-14](https://cf-img.discoverlabs.ac.cn/202507180759aba6be88c1d74621c9d4621f6a5a.webp)
2. 更多用法，推荐归藏老师的文章，能学到很多知识：https://mp.weixin.qq.com/s/Frdf_Gh3Xhvvmw2g-zOolA
3. 一点思考：对于卖Notion模板的创作者，AI出现后这个商业模式可能要走不通了。因为用户可以直接看着你挂出来的模板图片要求AI复刻。虽然中间的数据库、公式不一样，但最终能达到输入和输出符合用户预期，对用户来说没有区别。而如果你连模板图片都不放出来，大概率用户是不会购买的。这也是以后很多创作者会遇到的问题：在AI加持下，盗版或者说复刻的成本和门槛几乎为0，要怎么获取收入呢？