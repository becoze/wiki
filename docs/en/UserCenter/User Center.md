# User Center

## 项目初始化

### 前端初始化

- 配置环境

	- 下载node.js
	- 下载yarn

- 初始化项目
- 项目瘦身

### 后端初始化

- 安装 MySQL 环境
- 初始化 Spring Boot
- 引入 MyBatis-Plus 框架

	- 连接数据库
	- 引入依赖
	- 编码
	- 使用
	- （Error: Spring Boot 不兼容）

## 数据库设计

## 后端 - 注册功能

### 规整项目目录

### 实现基本数据库操作(MyBatisX)

- 删除demo数据
- MyBatisX 安装，使用和测试 

	- 安装MyBatisX 插件
	- 使用MyBatisX
	- 测试 MyBatisX 生成的代码

		- 放入假数据 
		- 输出验证
		- 代码
		- 关闭默认转换
		- 测试结果

### 注册接口编写

- 分析注册逻辑
- 实现注册功能  (编写代码)

	- 定义接口
	- 实现用户注册功能
	- 对密码进行加密
	- 插入用户数据
	- UserService 最终代码

- 编写测试类进行测试

## 后端 - 登录功能

### 分析登录逻辑

### 设计登录功能

### 实现业务逻辑层 - 构建 UserService 

- 1. UserService 初始化
- 2. 定义登录方法
- 3. 校验用户账户和密码是否合法
- 4. 校验登录密码
- 5. 脱敏用户信息
- 6. 记录用户的登录状态（session）
- 7. 返回脱敏后的用户信息

### 封装控制层请求成接口 - 构建 UserController 

- 1. UserController 初始化
- 2. 接收 注册 请求参数 - 编写 `request.UserRgisterRequest`
- 3. 编写注册请求
- 4. 接收 登录 请求参数 - 编写 `request.UserLoginRequest`
- 5. 编写登录请求
- （6. Error - 缺失接口地址）

### 测试后端接口

- API 通常测试
- 组件“逻辑删除” 测试

## 后端 - 用户管理功能

### 用户管理接口设计

### 实现鉴权功能 

- 添加新 userRole 数据库字段
- 同步其他设置(userRole)
- （Error：不能正常导入包，或 Mapping 出错。）
- 优化常量管理（统一管理常量）

### 实现查询用户功能

### 实现删除用户功能

### 优化重复代码

### 设置超时时间

### 测试  - 管理员权限查询用户

### 过滤管理员查询结果

### 优化 “信息脱敏” 代码

## 前后端连接

### 修改登录提交的表单名

### 修改请求的API域名

### 测试 API 域名

### Error: 跨域错误

### 配置代理 - 跨域

- （什么是代理）
- 配置代理
- 测试

### 修改前端传递的参数

## 阶段测试

## 前端 - 修改UI

### 修改 i18n 默认语言

### 修改footer

### 修改logo

### 修改Title / Sub-Title

### 删除不需要的功能

### 修改功能

## 前端 - 注册功能

### 增加注册页面

### 添加路由

### 优化默认框架（解决跳转Error） 

### 删掉不需要的功能

### 修改文本代码

- （Error - '注册' 按钮文字错误）

### 实现用户输入框

### 实现注册提交逻辑

- 定义注册参数
- 添加密码校验
- 实现注册逻辑
- 添加页面跳转 

### 测试登录功能

- （Error - 返回地址 redirect=undefined）

## 前端 - 登录功能 

### 获取当前用户信息接口，和用户登录态

- 编写后端接口
- 编写前端接口

### 修改前端全局文件 `app.tsx`

- 修改第一次登录
- 修改白名单
- 修改登录态获取
- 修改水印报错

### 添加用户信息

- Error - 没有用户名和用户头像
- Error - 头像加载失败

## 前端 - 用户管理后台

### 创建 `Admin` 管理页面

### 设置权限管理

### 开发管理页面

- 引用官方现成组件（ProComponents 高级表单）
- 删除不必要功能
- 开发页面

	- Error - 错误 import api
	- 修改表格列
	- 实现用户搜索并显示结果
	- 显示用户头像的图片
	- Error - 表格行高不一致
	- 优化枚举值的显示

## 开发用户注销功能

### 后端

- 服务层 `UserService`
- 控制层 `UserController`

### 前端 - 添加接口

### 测试

## 后端代码优化

### 封装通用返回对象 `BaseResponse`

- 初始化
- 封装 `ResultUtil` 工具类
- 用 `ResultUlt` 工具类的 `BaseResponse` 封装之前的代码
- 自定应错误码
- 优化 `BaseResponse` 同时支持返回成功和错误信息

### 封装全局异常处理 `UserService`

- 定义业务异常类

	- 初始化异常构造器
	- 在 `UserController` 里使用异常类
	- 在 `UserService` 里使用异常类
	- Error: 抛出了 500 异常

### 编写全局异常处理器

- 初始化
- 拓展之前的代码
- 实现捕获异常方法
- 测试"异常信息返回“

## 前端代码优化

### 创建通用返回类

- 初始化
- 封装 `register` 响应类
- 运用
- Error: 编辑器自动引入错误的包
- 封装全部剩余响应类

### 适配后端通用返回对象

- .gitignore 添加新无视文件
- 实现全局响应拦截器

### 测试 - 错误信息返回

## 多环境

### 前端多环境

- 前端多环境设计
- 配置前端区分环境
- 构建本地静态化项目文件

	- start & build

- Error - 占用 `dist` 文件的进程
- 运行本地项目`serve` 
- 实现根据不同的环境请求不同的地址

### 后端多环境

- 后端多环境设计
- 配置后端多环境

	- 新建 `prod` 环境配置文件
	- 获取建表 DDL

## 最终测试

