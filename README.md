# Chirpy Starter

[![Gem Version](https://img.shields.io/gem/v/jekyll-theme-chirpy)][gem]&nbsp;
[![GitHub license](https://img.shields.io/github/license/cotes2020/chirpy-starter.svg?color=blue)][mit]

When installing the [**Chirpy**][chirpy] theme through [RubyGems.org][gem], Jekyll can only read files in the folders
`_data`, `_layouts`, `_includes`, `_sass` and `assets`, as well as a small part of options of the `_config.yml` file
from the theme's gem. If you have ever installed this theme gem, you can use the command
`bundle info --path jekyll-theme-chirpy` to locate these files.

The Jekyll team claims that this is to leave the ball in the user’s court, but this also results in users not being
able to enjoy the out-of-the-box experience when using feature-rich themes.

To fully use all the features of **Chirpy**, you need to copy the other critical files from the theme's gem to your
Jekyll site. The following is a list of targets:

```shell
.
├── _config.yml
├── _plugins
├── _tabs
└── index.html
```

To save you time, and also in case you lose some files while copying, we extract those files/configurations of the
latest version of the **Chirpy** theme and the [CD][CD] workflow to here, so that you can start writing in minutes.

## Usage

Check out the [theme's docs](https://github.com/cotes2020/jekyll-theme-chirpy/wiki).

## Contributing

This repository is automatically updated with new releases from the theme repository. If you encounter any issues or want to contribute to its improvement, please visit the [theme repository][chirpy] to provide feedback.

## License

This work is published under [MIT][mit] License.

[gem]: https://rubygems.org/gems/jekyll-theme-chirpy
[chirpy]: https://github.com/cotes2020/jekyll-theme-chirpy/
[CD]: https://en.wikipedia.org/wiki/Continuous_deployment
[mit]: https://github.com/cotes2020/chirpy-starter/blob/master/LICENSE

## 以下是massorant自己的话
和任何教程都不一样，我没有在本地额外安装任何东西包括jekyll、ruby等，直接通过Click the Use this template button and then select Create a new repository然后修改配置文件en-->zh-CN。打开myname.github.io网址就有了。并且通过_post正常写博客。
调试也是在github上调试的，比本地调试需要的时间稍微多一些。
### 期间发生了一些我无法理解的事情：
1、刚开始我不了解index.html指向另一个html文件的原理
```code
---
layout: home
# Index page
---
```
打开网址只显示这个指令，以为需要自己添加内容，于是复制了dome的index.html，然后显示出来了。但是第二天换回原来的index.html也能正常显示。并且后续我发现，如果配置文件写错或者文件结构新增文件夹都会让指向失败，只显示出指令。

我怀疑是github服务器的网络延迟 + 我本地的浏览器cookies导致的。

2、正常运行了，但是侧边导航栏显示的是英文，我想设置成中文。我第一次在配置文件里填写lang: zh-CN 的时候没有显示中文，看到注释的是需要_data/locales/的路径下需要有对应的zh-CN.yml文件（当时我的库中连locales文件夹都没有，但是别人的dome有）。于是我去dome里复制文件夹带文件。完成后网站又只显示index.html的指向命令，不显示正常的博客内容。我把创建的locales文件夹删除，网站正常，同时也显示出了中文，匪夷所思！
