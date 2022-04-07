# 在项目开发中大家都需要注意的规范

俗话说，无规矩，不成方圆。为了维护方便，保持代码的见解，我们会有一些共同的约定，而这些约定便是团队开发工作的规范。其中包括了项目配置的规范，项目结构的规范以及命名规范等。

### 项目配置规范 ###

- 项目包命名格式：com.{公司名}.{项目名} 
- 配置文件存放位置，所有配置文件都有放在classpath目录下或classpath/config目录下，Spring，Hibernate，数据库配置使用XML， Log的配置使用properties。
- Web.xml加载配置：
    - Welcome-file 需要设置为index.html,index.jsp,index.do或者/index中的一种
    - 完成Welcome-file配置后，如果使用Spring框架和Hibernate框架，需要配置Context文件，引入-classpath下的配置文件
    - 先配置Filter以及Filter-mapping，后配置Servlet以及Servlet-mapping
- Spring配置：
    - 配置文件：所有spring配置文件放在classpath目录下。
        - SpringMVC.xml： 控制器，静态资源，视图解析器，拦截器等配置
        - SpringDataSource.xml: 数据源的信息，Hibernate、连接池的配置
        - SpringCornJob.xml：定时任务的配置
- 数据库配置：
    - 涉及移动端的数据库，需要适配Emoji表情，统一使用UTF-8MB4四位Unicode编码。
    - 配置文件： 直接配置在SpringDataSource.xml里面
    - 配置URL格式： **jdbc:mysql://{server}:3306/{dbName}?useUnicode=true&amp;characterEncoding=UTF-8** 

### 项目目录结构规范 ###


以下以Eclipse为例

![工作室项目结构截图](images/eclipse_projects.png)


### 组件定义和使用规范 ###
**Controller类命名规范：**
> 前端控制器：模块名+Controller，如：UserController 

**Dao类命名规范（Dao类必须符合“接口/实现”规范）：**

- 接口命名： 模块名+Dao，如：UserDao

- 实现类命名：模块名+DaoImpl，如：UserDaoImpl 

 **Service类命名规范** （Service类必须符合“接口/实现”规范）：

- 接口：模块名+Service，如：UserService 

- 实现：模块名+ServiceImpl，如：UserServiceImpl 

 **Interceptor类命名规范：** 模块名+ Interceptor ，如：UserInterceptor 

 **Entity类命名规范：** 模块名+Entity，如：UserEntity

 **POJO类命名规范：** 
- 数据传输对象使用 模块名+Dto , 用于服务层与控制器层的数据传递
- 视图数据对象使用 模块名+Vo，用于控制器层向展示层传递数据

 **Enum类：** 模块名+Enum，如：UserStatusEnum 

 **Util类命名规范：** 工具功能名+Util，如：DateUtil 

 **全局变量类的命名规范：** 模块名+Config。如，NetLimitConfig 
