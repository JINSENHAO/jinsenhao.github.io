# hexo-theme-gal    
# 配置说明2

    git clone https://github.com/ZEROKISEKI/hexo-theme-gal.git themes/gal
    
    or 
    
    git clone https://github.com/ZEROKISEKI/hexo-theme-gal.git themes/gal --depth 1

## 使用该主题前要安装的东西:

    更改主题为: gal

    在你的hexo站点目录(非主题目录)下安装 hexo-renderer-sass 和 hexo-renderer-scss
    
    npm install hexo-renderer-sass --save 
    
    npm install hexo-renderer-scss --save
    
    or 
    
    cnpm install hexo-renderer-sass --save
    
    cnpm install hexo-renderer-scss --save
    
    or 
    
    yarn add hexo-renderer-sass(推荐)
    
    yarn add hexo-renderer-scss(推荐)
    
    
    上面的一步是将.scss样式文件渲染成最后的style.css文件
    
    然后, 在你的hexo站点目录下安装 hexo-generator-json-content
    
    npm install hexo-generator-json-content --save
    
    or 
    
    cnpm install hexo-generator-json-content --save
    
    如果后面你hexo g的时候有问题, 注意看看是不是这个json-content的问题, 如果是的话就是你的node比较老
    
    接着在hexo站点目录的_config.yml下进行配置:
    
    jsonContent:
      dateFormat: MM-DD
      pages:
        title: true
        text: true
        path: true
        date: true
        excerpt: true
        preview: true
      posts:
        title: true
        text: true
        path: true
        date: true
        excerpt: true
        preview: true
    
    接着, 进行下面的步骤:
    
    hexo new page "search"              // 搜索功能的必须步骤
    hexo new page "404"                 // 开启404页面
    
    至于tags和categories页面的设置, 百度或google就有对应的方法了, 这里就不多说了
    
    对了, hexo站点目录的_config.yml的title, description, author和url要自己正确配置
    
## 主题的配置说明:

主题配置说明在[wiki](https://github.com/ZEROKISEKI/hexo-theme-gal/wiki/%E4%B8%BB%E9%A2%98%E9%85%8D%E7%BD%AE%E8%AF%B4%E6%98%8E)

## 使用建议:

    1. 建议每一篇文章都要在front-matter设置preview图片地址, 这个地址是url地址(本地的也要写完整的url)
    2. 每一篇文章的excerpt部分(即<!--more-->之前的部分)是纯文本而不要是markdown
    3. 作为背景用的图片大小都应该差不多, 比如示例用的几张背景图片都是1920 * 1080那样的
    4. 使用gitment作为评论系统, 在新发布文章时要去对应文章页面下点击初始化评论系统按钮(需登录)
    5. 可以设置置顶文章, 需要在front-matter设置top: true, 设置置顶文章最好只设置一篇

# 吐槽 && 痛点:

hexo只能采用第三方的评论系统, 要达到还原主题的评论效果, 目前只有gitment符合要求, 但是github issue没有那种一层一层回复的效果, 所以回复评论上只能采用**@**的方式

挺多hexo主题的搜索功能是直接链接到搜索引擎的site或者出现搜索框ajax出现搜索内容, 主题的搜索功能为了尽可能达到完全一致, 采用的方法并不是很妥当(用了带url参数的方式), 不过静态博客系统应该问题不大(也没什么东西可以被打):grin:

原主题采用了shortcode(短代码), 比如说`[warning]blablabla[/waring]`是对应解析成警告框的, 这点在hexo上可以实现, 但是这样就要求hexo用户也知道对应的规则, 不是很好, 所以在文章的markdown解析样式上是参照了其他一些主题的样式, 这点我无法做到完全的还原:disappointed:, 如果有人可以的话, 也可以做一下这个功能, 不过要对zanblog的解析规则了解才好

侧边栏标签云那里的字体随机大小, wordpress 直接有个方法`change_tag_cloud_font_sizes()`, 直接设定最大最小就行了, 每次刷新页面都是固定的值, 我用hexo取随机值每次都会变大小, 这点以后再改好些吧

反正近期有空的话就继续做




