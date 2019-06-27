
## css开发时书写规范
### 命名
使用小写字母，以中划线分割
    .list-tab {
        ...
    }

### 使用tab缩进
    .tab {
        width: 100%;
        height: 100%;
    }

### 每个属性声明末尾添加分号

### 添加空格
属性值前。
选择器'>','+','~'等前后。
'{'前。
'!important'的'!'前。
    .element {
        width: 100%;
        height: 100%;
    }

    .element + div {
        font-size: 16px !important;
    }

### 统一使用双引号

### 其他项
不允许有空的规则。
选择器不要超过4层。
尽量少用'*'选择器。

## JavaScript开发时书写规范
### 变量命名
标准变量采用驼峰式。
变量命名需要起的有意义，不要拼音和单词结合。也不要拼音首字母组合。
'ID','URL'在变量名中全大写。
'Android'在变量名中首字母大写，其他字母小写。
'iOS'在变量名中首字母小写，其他字母大写。
常量全大写，使用下划线链接。
构造函数大写第一个字母。
jquery对象使用'$'开头。

    let thisIsObj;

    let myID, myURL;

    let isAndroid, iOSVersion;

    let MAX_COUNT = 6;

    function Person(name) {
        ...
    }

    let $body = $('body');

### 变量声明
一个函数作用域中所有变量声明提前到函数首部，除了for中使用的一次性变量。
一行定义一个var/let/const。

    function doSomethingHandle() {
        let num;
        let value;
        let COUNT = 5;
        for(let i = 0; i < COUNT; i++){
            let something;
            ...
        }
    }

### 函数
声明函数和函数表达式，'('前不要有空格，'{'前一定要有空格。
立即执行函数必须包一层'()'。
参数之间使用','分割，逗号后要有一个空格。
    function doSomething(name, age, sex) {
        ...
    }

    (function() {
        ...
    })();

### 最外层统一使用单引号

### 单行长度
单行长度不超过120。

### 换行
代码块'{'后和'}'前。
定义变量后。

### 空行
代码块后需要空行。

### 其他项
'_'使用表示私有变量。
不允许使用三元运算符嵌套。
不允许使用空的代码块。
函数未被使用时应及时删除。
注释的无用的代码在上线前予以删除。
不允许使用if时不加{}。

### 函数定义使用规范
模块内定义函数禁止使用赋值的形式声明。

    // bad code
    let fn = function(){}

    // good code
    function fn(){}

箭头函数禁止用于函数的定义，可以用于作为参数传值时的定义。

    // bad code
    let fn = () => {};

    // good code
    arr.forEach(item => {});

### 关键字的使用
不建议继续使用var关键字，使用let关键字替代var关键字。
声明常量时，使用const关键字，不建议定义引用类型时使用。


文件命名与书写规范参考[腾讯imweb团队规范](http://imweb.github.io/CodeGuide/#js-variable-declaration)
