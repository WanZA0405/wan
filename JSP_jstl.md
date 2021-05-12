# **JSP_jstl**

在jsp页面

```
<%@taglib uri="http://java.sun.com/jsp/jstl/core" prefix="c"%>//引入jsp标签
<%@taglib uri="http://java.sun.com/jsp/jstl/fmt"  prefix="fmt"%>//格式化标签
<%@taglib uri="http://java.sun.com/jsp/jstl/functions" prefix="functions" %>//函数
```



### 利用el表达式：

${ };

| 功能                | 用法                                   |
| :------------------ | -------------------------------------- |
| 获取request对象     | **${requestScope.对象名}**             |
| 获取session中的对象 | **${sessionScope.对象名}**             |
| 获取项目路径        | **${pageContext.request.contextPath}** |
|                     |                                        |
|                     |                                        |
|                     |                                        |



- 获取request对象的数组循环  

  ```
  <c:forEach items="${requestScope.集合名}" var="对象名">
  循环中,用${对象名.参数名}
  ```

  

- 多条分支判断 

  ```
  <c:choose>
  	<c:when test=" ">//条件
  	</c:when>
  	<c:otherwise>//其他结果
  	</c:otherwise>
  </c:choose>
  ```

  

- if判断

  ```
  <c:if test="">//条件
  </c:if>
  ```
  
  
  
- if判断

