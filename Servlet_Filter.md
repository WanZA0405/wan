# Web/Servlet

##### 控制层继承HttpServlet

<input>中的name为需要的

##### request

```
request.setCharacterEncoding("utf-8");//处理收集数据时的中文乱码

request.getParameter("");//获取页面的数据

request.getParameterValues("");//获取页面的全部数据 返回数组

request.setAttribute("", );//存临时对象

request.getAttribute("");//取临时对象

request.getRequestDispatcher("").forward(request, response);//页面跳转,需要绝对路径

HttpSession session = request.getSession();//调用session

request.getContextPath();//获取项目的绝对路径,后面接/文件夹/jsp


```

数据转换（可强转）

```
int = Integer.parseInt(request.getAttribute(" ").toString());//转为数字

String  = request.getAttribute(" ").toString());//转为字符串

double  = Double.parseDouble(request.getAttribute(" ").toString());//转为浮点数
```



##### response

```
response.setContentType("text/html; charset=UTF-8");//处理放回页面时的中文乱码

PrintWriter out = response.getWriter();//用于页面输出

response.sendRedirect("");//页面重定向,相当于超链接
```



与浏览器的Cookie有关系

##### session

```
session.setAttribute("", )//用于存在session中的对象

session.getAttribute("")//用于取在session中的对象

session.removeAttribute("");//清理之前的存的session中的对象
```





## Servlet 生命周期

##### 构造方法 init doget/dopost destroy

##### 构造方法 init tomcat 

​		启动后，有第一个人访问某个servlet的时候创建servlet对象，然后执行init，再执行 doget or dopost
​		有第二个人访问某个servlet的时候直接执行已经创建好的servlet对象的doget or dopost

​		**注意   init 只会执行一次**

​		**destroy在服务停掉时执行，释放对象，执行一次**

#### 	servlet 是单例模式，一个servlet类只有一个对象





## Filter 过滤器 生命周期

​	构造方法 init  doFilter  destroy 

​		**init是在tomcat启动时就执行初始化(一次)，**

​		**doFilter会执行多次。**

​		登录验证
​		乱码处理
​		访问资源执行的时间统计

ServletRequest    ——》  HttpServletRequest
ServletResponse   ——》 HttpServletResponse

req.getRequestURI();
req.getRequestURL()