>  参考来源：
>
> [JavaScript基础语法-dom-bom-js-es6新语法-jQuery-数据可视化echarts黑马pink老师前端入门基础视频教程(500多集)持续_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=234&spm_id_from=pageDriver)

## 网页GitHub地址如下：（若加载较慢建议刷新后耐心等待一会~）

[js_bbs](https://jiang-lijun.github.io/js_bbs/)

## 主要功能：

1. 未输入内容时点击发送按钮，会弹出对话框提示；
2. 输入内容后点击发送按钮，文本内容会显示在下方区域。

## 网页代码如下：

### HTML：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>js_bbs</title>
    <link rel="stylesheet" href="index.css">
</head>
<body>
    <p>留言板:</p>
    <textarea name="bbs" id="bbs" cols="30" rows="10"></textarea>
    <button>发布</button>
    <p>评论区:</p>
    <ul></ul>
    <script src="index.js"></script>
</body>
</html>
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

### CSS：

```css
textarea {
    outline: none;
    margin: 0 0 10px 100px;
}
ul {
    margin: 0;
    padding: 0;
}
li {
    list-style: none;
    margin: 10px 0 10px 100px;
    font-size: 16px;
    color: pink;
}
```

![点击并拖拽以移动](data:image/gif;base64,R0lGODlhAQABAPABAP///wAAACH5BAEKAAAALAAAAAABAAEAAAICRAEAOw==)

### JS:

```javascript
var ul = document.querySelector('ul');
var text = document.querySelector('textarea');
var btn = document.querySelector('button')
btn.onclick = function() {
    if (text.value == '') {
        alert('您没有输入内容');
        return false;
    }else {
        var li = document.createElement('li');
        li.innerHTML = text.value;
        ul.insertBefore(li,ul.children[0]);
    }
}
```

