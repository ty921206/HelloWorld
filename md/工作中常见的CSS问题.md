1. 单行文本的溢出显示省略号（一定要有宽度）
```
 p{
    width:200rpx;
    overflow: hidden;
    text-overflow:ellipsis;
    white-space: nowrap;
 }

```
2. 多行文本溢出显示省略号
```
p {
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 3;
    overflow: hidden;
 }

```
3. 首行缩进
```
<p style="text-indent:2em;">这是一段内容文字，这是一段内容文字</p>```
4. 首字下沉
```
p:first-letter{
    font-size:40px;
    float: left;
    color:red;
}

```
5. 中英文自动换行
    word-break:break-all;只对英文起作用，以字母作为换行依据
    word-wrap:break-word; 只对英文起作用，以单词作为换行依据
    white-space:pre-wrap; 只对中文起作用，强制换行
    white-space:nowrap; 强制不换行，都起作用

```
p{
  word-wrap: break-word;
  white-space: normal;
  word-break: break-all;
}

```
6. IOS页面滑动卡顿
```
body,html{
    -webkit-overflow-scrolling: touch;
}

```
7. CSS滚动条仿IOS
```
::-webkit-scrollbar{
    width: 5px;
    height: 5px;
  }
::-webkit-scrollbar-thumb{
    border-radius: 1em;
    background-color: rgba(50,50,50,.3);
  }
::-webkit-scrollbar-track{
    border-radius: 1em;
    background-color: rgba(50,50,50,.1);
  }


```
8. 实现隐藏滚动条同时又可以滚动
```
.demo::-webkit-scrollbar {
  display: none; /* Chrome Safari */
}

.demo {
  scrollbar-width: none; /* firefox */
  -ms-overflow-style: none; /* IE 10+ */
  overflow-x: hidden;
  overflow-y: auto;
}

```
9. 表格边框合并
```
table,tr,td{
  border: 1px solid #666;
}
table{
  border-collapse: collapse;
}
```