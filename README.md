# 酒店网

本项目为存`CSS、HTML、JavaScript布局的项目`主要展示静态网页，训练自己的基础知识是否过关

## 1. 相关页面

1. 项目首页，在首页下拉那个卡片是可以点击切换的另外一个卡片（index.html）

   ![](https://github.com/liuxingzhumeng/Hotel_Website/blob/master/show/1.png)

2.  今日特惠，里边有个靠js倒计时的功能（discount.html）

   ![](https://github.com/liuxingzhumeng/Hotel_Website/blob/master/show/2.png)

3.  进入店铺，选项图，是可以动态切换的（hotels.html）

   ![](https://github.com/liuxingzhumeng/Hotel_Website/blob/master/show/3.png)

4. 预定房间（subscribe.html）

   ![](https://github.com/liuxingzhumeng/Hotel_Website/blob/master/show/4.png)

5. 登录注册功能

   ![](https://github.com/liuxingzhumeng/Hotel_Website/blob/master/show/5.png)



## 2. 相关技术

index.js中的代码，主要实现index.html功能，通过全部清空算法，在清空后重新赋值，达到唯一属性的目的，基本上后边的切换卡片都用到了这个技术

```JavaScript
var lis = document.querySelectorAll('.box-nav li');

for (var i = 0; i < lis.length; i++) {
    lis[i].setAttribute('index', i);
    lis[i].onclick = function() {
        for (var i = 0; i < lis.length; i++) {
            lis[i].className = '';
        }
        this.className = 'choose-box';// 通过这个方法，动态方式一大堆的CSS属性
        var index = this.getAttribute('index'); // 用于判断当前点到哪个东西
        if (index==0){
            document.getElementById("key").style.display="block"
        }else {
            document.getElementById("key").style.display="none"
        }
    }};

```

清除CSS浮动带来的影响，设置浮动后，控件时没有高度的，所有内容容易重叠这时我们可以

在浮动下边加个div，并添加属性去除浮动

注意如果在本地看文档的话，可以吧https://github.com/liuxingzhumeng/Hotel_Website/blob/master/ 部分删掉 ，就可以正常显示图片了
