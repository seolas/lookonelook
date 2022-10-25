### 教程

[【Hexo】使用Hexo+github pages+travis ci搭建好看的个人博客（一）](https://mfrank2016.github.io/breeze-blog/2020/05/02/hexo/hexo-start/)

### 问题1

网上的教程更改主题都是直接克隆的，但是由于我们外层是一个 Git 仓库，所以会报错。

![图片](https://user-images.githubusercontent.com/59484008/95186674-cf89ce00-07fc-11eb-86a6-0745aa246c36.png)

应该使用子模块的方式下载 NexT主题。

```
git submodule add  https://github.com/theme-next/hexo-theme-next themes/next
```

### 问题2

Next 主题的博客使用 Travis CI部署后，打开博客首页是空白的。

> 参考链接 [搭建github免费个人博客之Travis自动部署Hexo四](https://jingyan.baidu.com/article/215817f7b606e81eda142388.html)

删除 next 文件夹下的 `.github`、`.git`、`.gitignore` 后，再运行以下命令，首页就出来了。

```
git rm -r --cached .  # 清除缓存
git add .
git commit -am "update"
git push
```
