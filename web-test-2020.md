#web考察课 2020-6 期末考试
答案 author：yueguang blog：https://www.cnblogs.com/ygbrsf/
## 选择题
1.下面错误的是（）。  
A 静态网页不需要数据库的支持  
B 静态网页内容相对稳定  
C 静态网页交互性强  
D 静态网页容易被搜索引擎检索  

答案：C

2.下面描述正确的是（）。  
A article 元素部分可以独立被外部引用  
B 使用article元素后页面显示效果发生变化  
C article元素的标题一般放在thead元素里面  
D article元素的脚注一般放在tfoot元素里面  

答案：A

3.下面（）是有序列表标记。  
A \<ul>  
B \<ol>  
C \<dl>  
D \<dt>  

答案：B

4.下面（）不是标签\<img/>的属性。  
A alt  
B width  
C href  
D height  

答案：C  
解释\<img/>必须的属性是src和alt

5.<meta>标签的作用（）。  
A 用于设置HTML文档的格式  
B 用于设计页面的标题  
C 用于实现当前网页的自动刷新  
D 用于设置HTML文档的信息  

答案：D  
解释：不单单是页面的标题，信息可能会更准确

6.下面（）是html5新增的input类型  
A text  
B password  
C file  
D number  

答案：number

7.在html页面中插入浮动框架应采用（）标签  
A \<frameset>  
B \<frame>  
C \<iframe>  
D \<noframeset>  

答案：C  
解释：HTML·浮动框架（内联框架）：\<iframe></iframe>  
可以写在页面中的任意位置。

8.下面（）不是CSS基本选择器
A 标记选择器  
B 伪类选择器  
C 类选择器  
D 类选择器  

答案：B

9.下面（）是CSS注释  
A /*...*/  
B .//  
C \<!--...-->  
D \<!--...//-->  

答案：A

10.DOM的顶层是（）对象。  
A Form  
B Document  
C \<html>元素  
D \<body>元素  

答案：C  
解释：     
   DOM中的节点之间的关系  
   父子关系（parent-child）：\<html> 元素作为父级，\<head> 和 \<body> 元素作为子级  
   兄弟关系（Sibling）:\<a> 和 \<h1> 元素就是兄弟关系;\<title> 和 \<h1> 元素并不是兄弟关系  

## 填空题
1.使用相对路径链接下一目录，先输入[填空1]，后加入[填空2]。  

answer  
填空1：目录名  
填空2： /文件名  

2.CSS中，定位属性position的取值可以为：[填空1],[填空2],[填空3],[填空4]。
填空1： static  
填空2： relative  
填空3： absolute  
填空4： fixed  

解释：https://www.cnblogs.com/thewaytoace/p/5264436.html  

3.在HTML页面中，当单机对象会触发JavaScript的[填空1]事件。
填空1： onKeyDow  

4.如果要获取name为login的表单中的name为username的文本框的值，应采用表达式[填空1]。
填空1：username=login.username.value   

5.\<video>标记允许使用多个[填空1]标记来链接不同的视频文件。  
填空1：<source>  

6.CSS选择器的语法是[填空1]  
填空1：  
```
<p>
selector {
        property:value;
      }
<\p>   
```

## 主观题
1.简述web的工作机制。  
（1）浏览器中输入将要访问页面的URL地址。由DNS进行域名地址解析，找到服务器IP地址，向该地址所指向的Web服务器发出请求。  
（2）Web服务器根据浏览器送来的请求，把URL地址转换成页面所在服务器上的文件全名，查找相应的文件。  
（3）如果URL指向静态HTML文档，Web服务器使用HTTP协议把该文档直接送给浏览器。如果HTML文档中嵌入了ASP、PHP或JSP程序，则由Web服务器运行这些程序，把结果送到浏览器。如果Web服务器运行的程序包含对数据库的访问，则服务器将查询指令发送给数据库服务器，对数据库执行查询操作。  
（4）查询结果由数据库返回Web服务器，再Web服务器将结果数据嵌入页面，并以HTML格式发送给浏览器。  
（5）浏览器解释HTML文档，在客户端屏幕上展示结果。   
2.简述html文档结构。  
\<html>
\<head>
……
\</head>
\<body>
……
\</body>
\</html>

3.简述超链接路径。
绝对路径，相对路径，根路径  

4.简述在HTML中使用CSS的方法。
内嵌样式、内部样式、链接样式和导入样式。  

5.简述CSS盒模型。  
页面上的所有元素，包括文本、图像、超级链接、DIV块等，都可以被看作盒子。
盒子将页面中的元素包含在一个矩形区域内，这个矩形区域则称为“盒模型”。
网页页面布局的过程，可以看作在页面空间中摆放盒子的过程。
在CSS中，一个盒子模型由content（内容）、border（边框）、padding（填充）和margin（间隔）四部分组成。一个盒子的实际宽度或高度为：
content + padding + border + margin

6.简述事件处理的步骤。  
事件处理是JavaScript 基于对象编程的一-个重要环节，它可以使程序的逻辑结构更加清晰，程序更具有灵活性，从而提高程序的开发效率。事件处理的一般步骤 如下。  
确定响应事件的元素。  
为指定元素确定需要响应的事件。  
为指定元素的指定事件编写相应的事件处理程序。  
将事件处理程序绑定到指定元素的指定事件。  

7.采用一个名为ragister.html文档实现以下要求  
(1)采用表格对以上表单页面内容进行布局。  
(2)采用JavaScript对以上表单进行合法性验证（焦点离开时验证）。

```html
<p>
    <!DOCTYPE html>
    <html>
    <head>
    <meta charset="utf-8">
    <title></title>
    </head>
    <body>
    <form name="myform" method="post" action="" onSubmit="return validateform()">
    <p style="text-align: center;"></p>
    <p>&nbsp;</p>
    <table border="1px" style="border-width: 0; margin: 0 auto;">
    <tr>
    <td colspan="3" style="text-align: center;background-color: #9b9b9b;">用户注册</td>
    </tr>
    <tr>
    <td>登录名：</td>
    <td colspan="2">
    <input name="txtUser" type="text" id="txtUser" onchange="checkUserName()">
    （可包含a-z、0-9和下划线）
    </td>
    </tr>
    <tr>
    <td>密码:</td>
    <td colspan="2">
    <input name="txtPassword" type="password" id="txtPassword" onchange="checkPassword()">
    （不能为空，不能少于6个字符，只能包含数字和字母）
    </td>
    </tr>
    <tr>
    <td>密码确认</td>
    <td colspan="2">
    <input name="txtcheckPassword" type="password" id="txtcheckPassword" onchange="checkcheckPassword()">
    （与上面密码一致）
    </td>
    </tr>
    <tr style="background-color: #9b9b9b;" >
    <td>
    <input type="reset" name="" id="" value="重置" />
    </td>
    <td colspan="2">
    <input name="registerButton" type="submit" id="registerButton" value="提交" />
    </td>
    </tr>
    </table>
    </form>
    </body>
    <script language="JavaScript">
    function checkUserName() {
    username=document.getElementById("txtUser").value;
    var re=/^[a-z0-9_]{6,}$/;
    if(!re.test(username)){
    alert("未输入用户名，请输入用户名");
    }
    }
    
    function checkPassword() {
    password=document.getElementById("txtPassword").value;
    var re=/^[a-z0-9]{6,}$/;
    if(!re.test(password)){
    alert("密码必须多于或等于6个字符。\n");
    }
    }
    
    function checkcheckPassword() {
    password=document.getElementById("txtPassword").value;
    password1=document.getElementById("txtcheckPassword").value;
    if (password!=password1){
    alert("两次输入的密码不一致，请检查后重新输入");
    }
    }
    
    function validateform() {
    if (checkUserName() && checkPassword() && checkcheckPassword())
    return true;
    else
    return false;
    }
    </script>
    </html>
</p>
```

## 最后
谈谈本学期对于本课程的学习心得
这是我自己写的（自我发挥ovo）
1.代码编辑器
2.规划好代码的每一步的实现
3.合理地计划项目
4.学习资料
