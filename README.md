# 简介

## 什么是 Lin CMS？

> Lin-CMS 是林间有风团队经过大量项目实践所提炼出的一套内容管理系统框架。Lin-CMS 可以有效的帮助开发者提高 CMS 的开发效率。

本项目是基于ThinkPHP 5.1的 Lin CMS 后端实现。

本项目非官方团队出品，仅出于学习、研究目的丰富下官方项目的语言支持。

官方团队产品了解请访问[TaleLin](https://github.com/TaleLin)

## Lin CMS 的特点

Lin CMS 的构筑思想是有其自身特点的。下面我们阐述一些 Lin 的主要特点。

**Lin CMS 是一个前后端分离的 CMS 解决方案**

这意味着，Lin 既提供后台的支撑，也有一套对应的前端系统，当然双端分离的好处不仅仅在于此，我们会在后续提供NodeJS和PHP版本的 Lin。如果你心仪 Lin，却又因为技术栈的原因无法即可使用，没关系，我们会在后续提供更多的语言版本。为什么 Lin 要选择前后端分离的单页面架构呢？

首先，传统的网站开发更多的是采用服务端渲染的方式，需用使用一种模板语言在服务端完成页面渲染：比如 JinJa2、Jade 等。 服务端渲染的好处在于可以比较好的支持 SEO，但作为内部使用的 CMS 管理系统，SEO 并不重要。

但一个不可忽视的事实是，服务器渲染的页面到底是由前端开发者来完成，还是由服务器开发者来完成？其实都不太合适。现在已经没有多少前端开发者是了解这些服务端模板语言的，而服务器开发者本身是不太擅长开发页面的。那还是分开吧，前端用最熟悉的 Vue 写 JS 和 CSS，而服务器只关注自己的 API 即可。

其次，单页面应用程序的体验本身就要好于传统网站。

**框架本身已内置了 CMS 常用的功能**

Lin 已经内置了 CMS 中最为常见的需求：用户管理、权限管理、日志系统等。开发者只需要集中精力开发自己的 CMS 业务即可

Lin CMS 本身也是一套开发规范
Lin CMS 除了内置常见的功能外，还提供了一套开发规范与工具类。换句话说，开发者无需再纠结如何验证参数？如何操作数据库？如何做全局的异常处理？API 的结构如何？前端结构应该如何组织？这些问题 Lin CMS 已经给出了解决方案。当然，如果你不喜欢 Lin 给出的架构，那么自己去实现自己的 CMS 架构也是可以的。但通常情况下，你确实无需再做出架构上的改动，Lin 可以满足绝大多数中小型的 CMS 需求。

举例来说，每个 API 都需要校验客户端传递的参数。但校验的方法有很多种，不同的开发者会有不同的构筑方案。但 Lin 提供了一套验证机制，开发者无需再纠结如何校验参数，只需模仿 Lin 的校验方案去写自己的业务即可。

还是基于这样的一个原则：Lin CMS 只需要开发者关注自己的业务开发，它已经内置了很多机制帮助开发者快速开发自己的业务。

**基于插件的扩展**

任何优秀的框架都需要考虑到扩展。而 Lin 的扩展支持是通过插件的思想来设计的。当你需要新增一个功能时，你既可以直接在 Lin 的目录下编写代码，也可以将功能以插件的形式封装。比如，你开发了一个文章管理功能，你可以选择以插件的形式来发布，这样其他开发者通过安装你的插件就可以使用这个功能了。毫无疑问，以插件的形式封装功能将最大化代码的可复用性。你甚至可以把自己开发的插件发布，以提供给其他开发者使用。这种机制相当的棒。

**前端组件库支持**

Lin 还将提供一套类似于 Vue Element 的前端组件库，以方便前端开发者快速开发。相比于 Vue Element 或 iView 等成熟的组件库，Lin 所提供的组件库将针对 Lin CMS 的整体设计风格、交互体验等作出大量的优化，使用 Lin 的组件库将更容易开发出体验更好的 CMS 系统。当然，Lin 本身不限制开发者选用任何的组件库，你完全可以根据自己的喜好/习惯/熟悉度，去选择任意的一个基于 Vue 的组件库，比如前面提到的 Vue Element 和 iView 等。你甚至可以混搭使用。当然，前提是这些组件库是基于 Vue 的。

**完善的文档**

我们将提供详尽的文档来帮助开发者使用 Lin

## 所需基础

由于 Lin 采用的是前后端分离的架构，所以你至少需要熟悉 PHP 和 Vue。

Lin 的服务端框架是基于 ThinkPHP 的，所以如果你比较熟悉 ThinkPHP 的开发模式，那将可以更好的使用 Lin。但如果你并不熟悉 ThinkPHP，我们认为也没有太大的关系，因为 Lin 本身已经提供了一套完整的开发机制，你只需要在 Lin 的框架下用 PHP 来编写自己的业务代码即可。照葫芦画瓢应该就是这种感觉。

但前端不同，前端还是需要开发者比较熟悉 Vue 的。但我想以 Vue 在国内的普及程度，绝大多数的开发者是没有问题的。这也正是我们选择 Vue 作为前端框架的原因。如果你喜欢 React Or Angular，那么加入我们，为 Lin 开发一个对应的版本吧。