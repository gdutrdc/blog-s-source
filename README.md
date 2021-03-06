## [RDC's Blog](http://gdutrdc.github.io/)

### 项目结构

这个仓库放的是整个blog源站代码,而博客的静态文件代码则在`gdutrdc/gdutrdc.github.io`另外一个仓库上。
每次写博客的时候都会通过master分支的代码生成静态文件然后部署到`gdutrdc/gdutrdc.github.io`，所以无须关注`gdutrdc/gdutrdc.github.io`上的代码，只要记得**每次写完提交**，防止别人pull代码时拉不到你写的博文，导致最终重新部署到`gdutrdc/gdutrdc.github.io`的博文覆盖掉你写的博文。

### 怎么发表博客

#### 1 将项目clone到本地
```
git clone https://github.com/gdutrdc/blog-code.git
```

#### 2 [下载安装node](https://nodejs.org/dist/v4.3.2/node-v4.3.2-x64.msi)，已经安装跳过此步骤

#### 3 进入`/blog/themes/`目录，打开命令行
```
git clone https://github.com/yumemor/hexo-theme-primer.git
```
#### 4 安装成功后将`hexo-theme-primer`这个文件夹重命名为`primer`

#### 5 退回blog文件夹，在当前位置打开命令行工具

#### 6 安装hexo-cli
```
npm install hexo-cli -g 
```
如果因为墙而安装不了，加一下淘宝的镜像
```
npm install hexo-cli -g --registry=https://registry.npm.taobao.org
```

#### 7 安装hexo插件，在命令行输入
```
npm install 
```
安装不了同样加上镜像
```
npm install --registry=https://registry.npm.taobao.org
```
#### 8 安装完毕之后可以开始写东西了
```
hexo new "写一篇博文试试"
```

#### 9 在 `blog\source\_posts`这个目录下可以看到生成一个md文件
![hexo new](http://7xn5s5.com1.z0.glb.clouddn.com/hexo.png)

#### 10 打开你喜欢的编辑器，编辑这个md文件([md语法](https://github.com/LearnShare/Learning-Markdown/blob/master/README.md))

#### 11 编辑完保存后，输入
```
hexo g
```
将这篇md语法的文章生成对应的html文件

#### 12 打开一个静态服务器预览
```
hexo s
```

#### 13 一切都ok，输入
```
hexo d
```
将其部署到github上

#### 14 最后，记得提交整个blog代码！！！！！
```
git add -A
git commit -m "test"
git push origin master
```