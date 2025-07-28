
主题类别/链接：[[存档教程：]]、[[教程存档]]
## 前言
近期在用claude code折腾各种小工具，发现用Vercal来部署github上的小网页很方便。但是Vercal 部署的网页在国内不方便访问，这时候我们就可以用找赛博大善人Cloudflare来帮我们加速一下Vercal，当然前提是你有自己的域名并且已经部署到了Cloudflare

# 具体步骤
## 一、进入Vercal项目设置，添加域名
![image-2](https://cf-img.discoverlabs.ac.cn/20250728d4cc52cad8586acb172745f4fddec55e.webp)![image-3](https://cf-img.discoverlabs.ac.cn/202507283567cba09618a49385d2babdadf7e8c2.webp)
比如假设你的域名是hello.com，那么你这里可以填写项目名字.hello.com，例如blog.hello.com。点击save后会爆红，这时候不用害怕，点击左边的红字，就会变成下面的内容，把这些内容记录下来![image-8](https://cf-img.discoverlabs.ac.cn/2025072822cd3eaf06713f0a04f513bfa8d53b25.webp)

## 进入Cloudflare填写相关信息
进入你的DNS页面，选择新加一条
![image-12](https://cf-img.discoverlabs.ac.cn/20250728be883bebbfb31f411a4eb70a5c35df0a.webp)
根据Vercal给的信息填写相关内容。记得小云朵得先是关闭状态，填完后保存，然后我们回到Vercal
![image-13](https://cf-img.discoverlabs.ac.cn/2025072822f82c1b4e430c67cdc6411a57143a8a.webp)
## 回到Vercal刷新
回到Vercal后点击右上角刷新，之后会提示在申请免费的ssl证书。等待变绿后，回到Cloudflare把相关条目的小云朵打开就行了。然后你就可以用自己设置的域名来访问你的项目了。对了，记得把你的SSL/TLS设置成“严格”
![image-11](https://cf-img.discoverlabs.ac.cn/20250728723904e338ef9144a7b5ee3dcbd88286.webp)
![image-14](https://cf-img.discoverlabs.ac.cn/202507280cc96ff6dc2e8af372e70fc4a25b6691.webp)