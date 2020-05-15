# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
    
```python
# 缩进格式    
    &nbsp;&nbsp;
    两个空格

# 段落
    ==
    -

# 背景色
    `背景色`
    **背景色**

# 文字类型
    正常文字
    *倾斜文字*
    _倾斜文字_
    **加粗文字**
    ***倾斜加粗文字***
    ~~下划线~~
    - - -
    * * *

# 代办事宜
    -[]一件
    -[x]二件
 
```

![地球图片](https://www.helloglobal.com/online-public/index/index__earth.gif)

![百度](http://www.losking.cn/uploads/img1/20180907/5b91f44540c03.jpg)

6. 锚点，利用锚点可以制作目录。
    Github 并不支持 HTML 形式的锚点链接，它有自己的规则
```bazaar
规则:
    1. 任意 1-6 个 # 标注的标题都会被自动添加上同名的锚点链接
     可把鼠标放到 Github 的标题上进行观察

[标题1](#标题1) 
[标题2](#标题2) 
[标题3](#标题3) 

# 标题1
## 标题2
### 标题3
    2. 锚点跳转的标识名称，可使用任意字符，大写字母要转换成小写
[Github标题1](#github标题1)

### Github标题1
    3. 多单词锚点的 空格 用 - 代替
[Github 标题2 Test](#github-标题2-test)

### Github 标题2 Test
    4. 多级序号需要去除 '.'
[2.3. Github 标题](#23-github-标题)

### 2.3. Github 标题
    注意
    非英文的锚点字符，在单击跳转时，在浏览器的 url 中会按照规则进行 encode 和 decode
```

<details>
<summary>点击查看运行日志</summary>
<!--注释：收缩写法-->

```
INFO     Loading environment variables from /Users/debugtalk/mubu-demo/.env
INFO     Start to run testcase: /api/login/submit
/api/login/submit
INFO     POST https://mubu.com/api/login/submit
INFO     status_code: 200, response_time(ms): 206.3 ms, response_length: 45 bytes
```