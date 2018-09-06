# 如何写好注释

> 注释虽然写起来很痛苦, 但对保证代码可读性至关重要，注释虽然很重要，但是好的代码其实本身就是文档，有意义的命名比起含糊不清的注释好上万倍。

## 为什么要写注释 ？

- 增强代码的可读性
- 减少团队协作的沟通成本
- 提升开发者维护的效率
- 等等……

## 注释风格

### Plain Javascript 中的注释

1、单行注释

```javascript
// const a = 1;
```

2、多行注释

```javascript
/*
    if (true) {
        alert(1);
    }
*/
```

3、给函数注释

``` javascript
/**
* [countArray 统计数组中指定元素出现的次数]
* @param  {[Array]} arr [目标数组]
* @param  {[String]} val [指定元素]
* @return {[Number]}     [统计到的次数]
*/
function countArray(arr, val) {
    let count = 0;
    let pos = 0;
    while (pos < arr.length) {
        pos = arr.indexOf(val, pos);
        if (pos === -1) { // 未找到就退出
        break;
        }
        count += 1;
        pos += 1;
    }
    return count;
}
```

### React 中的注释

1、jsx

``` jsx
<Parent backend={HTML5Backend}>
    {/* <Child name="Glass" /> */}
    <Child name="Banana" />
    <Child name="Paper" />
</Parent>
```

2、components（为组件的 props 加上 PropTypes）

``` javascript
class Confirm extends PureComponent {
  static propTypes = {
    onOk: PropTypes.func,  // 确认回调
    onCancel: PropTypes.func, // 取消回调
    okText: PropTypes.string, // 确认文本
    cancelText: PropTypes.string, // 取消文本
    title: PropTypes.string.isRequired, // 标题
    content: PropTypes.string, // 内容
    width: PropTypes.oneOfType([PropTypes.string, PropTypes.number]), // 宽度
  };
}
```

### CSS 中的注释

1、plain css

``` css
.comment {
    /* width: 200px;
    height: 100px; */
}
```

2、less

``` less
.comment {
    // width: 200px;
    height: 100px;
}
```

### HTML 中的注释

``` html
<!-- <p class="comment">Lorem ipsum</p> -->
```

### 文件注释

1、react

``` javascript
/**
 * Copyright (c) 2013-present, Facebook, Inc.
 *
 * This source code is licensed under the MIT license found in the
 * LICENSE file in the root directory of this source tree.
*/
```

2、vue

``` javascript
/*!
 * Vue.js v2.5.17-beta.0
 * (c) 2014-2018 Evan You
 * Released under the MIT License.
*/
```

## 注释插件推荐

- sublime 插件：DocBlocker
- vscode 插件：Better Comments

## Have fun

``` html

<!-- ####################################################
    #                                                   #
    #                       _oo0oo_                     #
    #                      o8888888o                    #
    #                      88" . "88                    #
    #                      (| -_- |)                    #
    #                      0\  =  /0                    #
    #                    ___/`---'\___                  #
    #                  .' \\|     |# '.                 #
    #                 / \\|||  :  |||# \                #
    #                / _||||| -:- |||||- \              #
    #               |   | \\\  -  #/ |   |              #
    #               | \_|  ''\---/''  |_/ |             #
    #               \  .-\__  '-'  ___/-. /             #
    #             ___'. .'  /--.--\  `. .'___           #
    #          ."" '<  `.___\_<|>_/___.' >' "".         #
    #         | | :  `- \`.;`\ _ /`;.`/ - ` : | |       #
    #         \  \ `_.   \_ __\ /__ _/   .-` /  /       #
    #     =====`-.____`.___ \_____/___.-`___.-'=====    #
    #                       `=---='                     #
    #     ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~   #
    #                                                   #
    #               佛祖保佑         永无BUG              #
    #                                                   #
    #####################################################
-->
```

## 参考资料 & 相关资源

- [Google 开源项目风格指南](https://zh-google-styleguide.readthedocs.io/en/latest/google-cpp-styleguide/comments/)
- [谈代码注释](https://blog.csdn.net/breaksoftware/article/details/79773947)
- [有趣的注释](https://blog.csdn.net/u010447573/article/details/46234951)
- [生成你的有趣注释](http://www.asciiworld.com/-Mangas)
