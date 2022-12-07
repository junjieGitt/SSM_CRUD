# SSM_CRUD
SSM integrates to develop CRUD quickly

# 功能点
1. 分页
2. 数据校验
   * jquery前端校验+JSR303后端校验
3. ajax
4. Rest风格的URI, 使用HTTP协议请求方式的动词， 来表示对资源的操作
   * GET(查询)
   * POST(新增)
   * PUT(修改)
   * DELETE(删除)
   
# 技术点
1. 基础框架-ssm (SpringMVC + Spring + MyBatis)
2. 数据库-MySQL
3. 前端框架-bootstrap
4. 项目的依赖管理-Maven
5. 分页-pagehelper
6. 逆向工程-MyBatis Generator


# 基础环境搭建
1. 创建Maven工程
2. 引入项目依赖的jar包
   * Spring
   * SpringMVC
   * mybatis
   * 数据库连接池，驱动包
   * 其他(jstl, servlet-api, junit)
3. 引入bootstrap前端框架
4. 编写ssm整合的关键配置文件
   * web.xml
   * spring
   * springmvc
   * mybatis
   * 使用mabatis的逆向工程生成对应的bean以及mapper (MBG mybatis generator)
5. 测试mapper

# 查询 
1. 访问index.jsp页面
2. index.jsp页面发送查询员工列表请求
3. EmployeeController来接受请求
4. 来到list.jsp页面进行展示
   * Controller 控制处理增删查改 service 业务
   * URI: /emps
   
# 查询-ajax
1. index.jsp页面直接发送ajax请求进行员工分页数据的查询
2. 服务器将查出的数据，以json字符串的形式返回给浏览器
3. 浏览器收到json字符串,可以使用js对json进行解析，使用js通过dom增删查改改变页面
4. 返回json, 实现客户端的无关性

# 新增-逻辑
1. 在index.jsp页面点击"新增"
2. 弹出新增对话框
3. 去数据库查询部门列表，显示在对话框中
4. 用户输入数据，并校验
5. 完成保存

* URI:
    * /emp/{id} GET查询员工
    * /emp           POST保存员工
    * /emp/{id}      PUT修改员工
    * /emp/{id}      DELETE删除员工

# 修改-逻辑
1. 点击编辑
2. 弹出用户修改的模态框
3. 点击更新，完成用户修改

# 删除-逻辑
1. 点击删除
    * URI:/emp/{id} DELETE


# 总结


