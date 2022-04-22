本演示库美化方案如下：

1、安装 Minimal 主题并启用，可配套 Minimal Theme Settings 插件修改主题颜色。

2、隐藏不必要的页面元素，使页面更简洁，通过 Hider 插件实现。

3、自定义字体。通过 `font.css` 代码片段实现。正文字体参考 Bear，选用 Avenir next。代码字体选用 Menlo。表格字体选用 Sarasa Mono Slab J，是更纱黑体的一种，配合 Advanced Table 插件，可以实现表格的中英文对齐。

4、设置左侧导航栏文件夹图标。通过 `folder-icons.css` 代码片段，指定不同文件夹名前缀加不同的 emoji。这样的好处是本身文件夹命名不用加emoji，以免出现路径上的异常。

5、设置标签小药丸效果。通过 `tag-pills.css` 代码片段，指定不同标签不同颜色，默认为蓝色。

6、添加 Banner。Notion 风 Banner，美化用。Banner图片存放在 `/template/media` 路径下。个人喜欢在日记模板中添加 banner，每日自动生成，增强一下写日志的体验。

7、为链接增加小图标。使用 `external-link-icons.css` 代码片段，效果示例为：[Obsidian 随机生成读书笔记片段](https://sspai.com/post/69005)

8、其他小点的小改，统一放在 `general.css` 中。比如取消斜体引用，因为在传统的中文版本中，没有斜体中文的做法。

9、提供图片并列显示功能。利用 `image-grid`+Contextual-Typography 显示。



效果如下：

![Obsidian_Beautification.jpg](https://vip1.loli.io/2022/04/23/9juDBds8g4AC76H.jpg)
