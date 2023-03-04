# GDScript 零基础图文入门

编写中的中文 Godot & GDScript 零基础图文入门教程。

阅读地址：

- [在线阅读-Github](https://reimenn.github.io/MyGDSciprtBook/)

- [在线阅读-Gitee](http://blog_rika.gitee.io/mygdscriptbook/)

# 愿意帮助我吗？（贡献方式）

截至目前，绝大部分正文内容都是我一个人写的，但我的技术、文笔、精力都有限，因此我十分期待各位的加入。

## 纠正错误或提供建议

如果你不想直接编写文章内容，只是想要指出文中错误或提供建议，那么你可以：

- 使用仓库的 Issue 功能，在 Issue 中描述你的想法。

或者

- 若你不会使用 Issue 或其他原因，可以在文中的[关于本书]章节寻找作者的其他联系方式。

## 内容修改

如果你想重新编写某段已有的内容，可以直接提交 PR，但注意只需要提交 src 目录即可。

同时注意，文中使用的图片资源应当放置在本章文件夹的 images 文件夹中。

## 目录修改

如果你想修改目录，例如添加、移动、删除章节，建议提交 `src/SUMMARY.md` 文件的 PR 并在其中说明每部分的修改原因。

## 认领未编写篇章

目录中有一些画饼章节，如果你想填坑，建议提交的 PR 中包含 `src/SUMMARY.md` 以及该章节的 md 文件，并且我建议在开始编写时就先将空文章提交上来，表示“这段我在写”，防止有人重复编写。

> 整活小节计划由我本人编写，且由于目前大部分内容都是我写，我就不发这种认领章节的 PR 了，但我会经常看看 PR 防止写重复的。

## 编写环境

本文采用 [mdbook](https://rust-lang.github.io/mdBook/) 编写，这是一个使用 Rust 开发的工具，可以让我们使用 Markdown 编写书籍。

本文使用的 mdbook 版本是 v0.4.27，如果你是 windows 系统也可以直接使用仓库目录中的 mdbook.exe。

进入到本仓库目录（src文件夹所在目录）后运行下面指令即可预览：

```
.\mdbook.exe serve --open
```

> 为了更好的展示小提示等内容，我还使用了 [mdbook-admonish](https://github.com/tommilligan/mdbook-admonish) 插件（版本 1.8.0），不过这个插件已经配置好了，克隆本仓库后不需要手动配置。

## Markdown 规范

1. 中文与英文之间间隔一个空格。

2. 采用严格换行模式，想要在 html 中开始新段落需要输入两个换行符。

3. 行内代码语法（就是指两个反引号 `\`\``）不要用太多，当句子中提到代码中出现的内容时，且该内容为重点时才标记，例如：

我们使用 `get_node` 来获取一个节点，get_node 需要一个字符串作为参数，且返回一个 Node 类型的结果。

4. 想要强调某些内容但又不是代码，请使用加粗功能。

5. 尽量不要在正文中使用 html。

## Markdown admonish

这个语法用于产生小提示或笔记那种独立的文本框，具体样式来自 mdbook-admonish 插件，但我更喜欢微软的语法，于是自己写了些 js 来把微软语法的 admonish 标签加上了 mdbook-admonish 的 css class。。。

实际用起来大概是这样：

> [!tip] 小提示标题
> 
> 这里是小提示，上面这行空行是因为采用严格换行。

> [!note] 
>
> 记个笔记吧

> [!warning]
>
> 注意这里有坑

注意 > 和 [ 符号之间的空格，且类型暂时之建议用 tip\note\warning 三者。
