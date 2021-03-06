## 导航（amp 平台版）

本篇基于 Amp 平台介绍了几种常用的导航方式

### 平台内应用间导航
1. Amp 平台秉承碎片化应用的理念，把各个业务按功能分成了大量应用模块。遵循辐射状导航模式，网上办事服务大厅是一切导航路径的核心，用户登录网上办事服务大厅后，根据待办搜索或推荐进入目标应用（浏览器新建标签页）。返回到网上办事服务大厅的标签页，即可重新选择应用。
2. 应用间跳转一般通过链接或者按钮触发，点击后新建标签页进入新的应用。同样通过浏览器标签页的切换在应用间导航

![](http://oizi4nn30.bkt.clouddn.com//20170807112835_WuYbLF_BetweenApps.jpeg)

***

### 应用内导航

- 当一个应用内有多个功能模块时，通常会使用我们叫做「全局导航栏」的组件在模块间导航，点击可在不同模块间切换。

![](http://oizi4nn30.bkt.clouddn.com//20170807114434_juPlAV_routes.jpeg)

见组件-全局导航栏

- 当一个应用内有很多个功能模块，且可以划分成数个类型时，可以把应用首页作为跳板页，点击相应功能新建标签页或纸质弹窗打开页面。同时可在每个功能后用不同属性的标签Tag展示必要的信息，如待办数目等。

![](http://oizi4nn30.bkt.clouddn.com//20170814101848_KynYT2_tiaobanye.jpeg)

特点：
- 通过跳板页进入的页面默认已经进行了筛选。比如卡片中显示了待办数目，点击进入后直接筛选进入待办的列表。
- 跳板页各个功能模块的显示隐藏可以根据需求对不同角色进行设置。

***

### 页面内导航

#### 纸质弹窗

纸质弹窗用于展示弹窗无法承载的信息。触发后在当前页面 y 轴上弹出一层新页面。

<img class="preview-img no-padding" align="right" src="http://oizi4nn30.bkt.clouddn.com//20170810095428_nWkIia_zhizhitanchuang.jpeg">

点击表示上一级页面的 1.蓝色条，和纸质弹窗的 2.关闭按钮均关闭当前纸质弹窗，回到上一级页面。

理论上来说，纸质弹窗可以无限增加，但是出于垂直空间利用率和美观的考虑，一般不建议在设计中使用二级以上的纸质弹窗。

![](http://oizi4nn30.bkt.clouddn.com//20170810095428_yZzJva_2zhizhitanchuang.jpeg)

#### 标签页（Tabs）

在一个页面内部，有时会把内容的不同模块组织成一个 Tab，这样每次只能看到一个模块。用户点击这些 Tab 来查看不同的模块内容。

![](http://oizi4nn30.bkt.clouddn.com//20170810100423_5SvJXO_Tab.jpeg)

特点：
- 用户每次只需要看到一个模块。
- 每个模块需要的显示面积大小相仿。
- 没有太多模块需要显示-一般小于十个，最好只有四五个。
- 这些模块相对来说比较稳定，不会有经常性的增减。
- 这些模块的内容有关或相仿。

见组件-标签页

#### 导航菜单（Menu）

为页面和功能提供导航的菜单列表
和标签页切换相比，左侧导航菜单可扩展性更强。一般数量较多的切换选择左侧导航菜单。

![](http://oizi4nn30.bkt.clouddn.com//20170810102238_i7PwM7_menu.jpeg)

#### 步骤条（Steps）

步骤条通常用于引导用户按照规定的步骤完成一系列任务，比如填写长表单。

![](http://oizi4nn30.bkt.clouddn.com//20170810113011_YP8ST1_stepbar.jpeg)

如使用步骤条，需要根据业务场景考虑到
- 新建和编辑状态下是否可以在任何时候点击步骤条中的某一步跳转
- 步骤条之间的关联和保存机制
- 全局按钮的设定
