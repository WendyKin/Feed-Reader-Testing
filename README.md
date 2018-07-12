# 订阅阅读器测试项目

    本项目为优达学城使用jasmine编写测试用例项目，编写代码在 Jasmine spec 文件 **./jasmine/spec/feedreader.js** 中。
    本项目参考了[优达学城论坛]（https://discussions.youdaxue.com/）中相关帖子思路。

打开index.html即可查看页面及测试是否通过。

*    `"RSS Feeds"` 测试用例

1.编写一个测试遍历 allFeeds 对象里面的所有的源来保证有链接字段而且链接不是空的。
2.编写一个测试遍历 allFeeds 对象里面的所有的源来保证有名字字段而且不是空的。
    使用forEach()遍历url和name字段。

*    `"The menu"` 测试用例

1.写一个测试用例保证菜单元素默认是隐藏的。
    检查body是否默认带有menu-hidden的class。

2.写一个测试用例保证当菜单图标被点击的时候菜单会切换可见状态。这个测试应该包含两个 expectation ： 当点击图标的时候菜单是否显示，再次点击的时候是否隐藏。
    点击2次检查menuIcon被点击时body的menu-hidden是否会切换。

*    `"Initial Entries"` 测试用例

写一个测试保证 `loadFeed` 函数被调用而且工作正常，即在 `.feed` 容器元素里面至少有一个 `.entry` 的元素。
    在异步加载loadFeed后检查.feed下子容器里是否有内容。
    为异步加载设置超时时间。

*    `"New Feed Selection"` 测试用例

写一个测试保证当用 `loadFeed` 函数加载一个新源的时候内容会真的改变。
    设置2个变量为loadFeed函数加载源和新源，在异步加载loadFeed后检查2个变量是否相同。
    为异步加载设置超时时间。

