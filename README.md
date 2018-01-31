# Email-templates
responsive-html-email-templates

## Why
之前做过一个邮件编辑器的项目，当时要求是兼容低版本的outlook的客户端，在outlook客户端上，有很多css的特性是不支持的。因此，需要做很多邮件兼容性的测试。
已经上线的邮件编辑器有完成版的邮件兼容性处理，但是代码量较多，`<table />`的嵌套层级数过多，需要进行优化。这是开这个仓库的主要原因。

## What
这个仓库里面的模板都是通过了 Litmus[https://litmus.com] 的测试，并且是支持移动客户端的响应式邮件模板。
国内比如微信的客户端，qq邮箱客户端等的支持有较为繁杂的测试过程，已经有对其做过一些兼容性的测试。

## How
直接 fork 或者下载。
可以将邮件分为三个部分，分别是 Structure, Widget, Content。

Structure：
  Structure是具有多列结构且比例可不同的块，多个 Structure 组成一封完整的邮件。
  如：2:3两列结构，1:1:2三列结构
Widget：
  Widget 是在 Structure 的每一列中可放置的块，多个 Widget 组成一个完整的 Structure。
  如：在一个 Structure 的一个列中放置的一个或者多个 Button 或者 Image，这些称之为 Widget模块。
Content：
  Content 就是 Widget 中用户可编辑的内容。
  如：在一个 Text Widget 中，可修改编辑文字内容。在 Image Widget 中，可以修改图片。
  
以上是邮件的 “块”，也就是这个仓库提供的模块化积木式的邮件拼装方式，让用户专注于内容的修改，也就是Content部分的修改，而不必过多的关注邮件兼容性的部分。

代码中，有具体的注释，包括属性的修改位置及相应的提示信息。

### Todo List
1.列出模板所支持的邮件客户端版本。
2.逐步添加邮件模块，如社交图标模块。
3.优化代码量，并完善注释。
