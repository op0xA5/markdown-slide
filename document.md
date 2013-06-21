--- 1 single ---

# Yii Framework 简介 #
## zhujinliang ##

--- 2 ---

# 资源 #

- 官网：<http://www.yiiframework.com/>
- 源码及下载：<http://www.yiiframework.com/download/>
- 学习资源：
  - The Definitive Guide to Yii  
    <http://www.yiiframework.com/doc/guide/>
  - Class Referencee  
    <http://www.yiiframework.com/doc/api/>
  - 应用Yii1.1和PHP5进行敏捷Web开发  
    <http://www.yiibook.com/book/agile_web_application_development_with_yii1.1_and_php5>
  - Google & English  
    <http://google.com> <http://www.iciba.com>

--- 3 ---

# 创建一个webapp #

- 下载解压framework
- 将php添加到path中
- 使用yiic创建webapp
  - cd 到站点目录
  - 执行 php yiic.php webapp testdrive
  - yiic创建所需的目录及初始文件
  - 访问测试
- 组织数据库
- 配置yii

*参考: <http://www.yiiframework.com/doc/guide/1.1/zh_cn/quickstart.first-app>*

--- 4 ---

# 建模型 #

- 配置gii
- 登录gii，进入Model Generator
  - Table Name => 完整表名
  - Model Class => 生成模型的类名
  - Preview & Generate
  - 打开文件调整rules,attributeLabels等

--- 5 ---

# 建控制器 #

- Gii Controller Generator
- Controller ID => 生成的控制器名称
- Base Class => 控制器基类  
  (默认的Controller类位于protected\components中)
- Action IDs => 生成action名称，逗号分割。  
  之后有需要在文件中添加即可。
- Preview & Generate
- 打开文件完成自己的业务逻辑

--- 6 ---

# view和layout #

- 都是用来输出页面
- 和控制器直接对应的view更关系与当前逻辑有关的部分
- layout关心整个页面的布局，菜单栏，侧边栏等通用部分
- layout可多层

--- 7 ---

# 模型基本操作 #

- 插入数据
  - 创建一个实例
  - 通过attributes导入数据，或直接写入表名相对应的属性导入数据
  - save()保存，如果通过验证并正确保存，则返回true。
  - 如果保存有错误，通过errors属性取出错误原因。
- 修改数据
  - 通过 Model::model()->findByPk()载入模型
  - 修改数据，类似插入过程
  - save()保存
- 删除数据
  - 通过 Model::model()->findByPk()载入模型
  - delete()删除

--- 8 ---

# 建Form #

--- 9 ---

# 基本流程 #

- 请求路由
- 载入Controller，执行对应方法
- Controller中处理业务逻辑，通过Model存取数据库
- COntroller将处理后的数据交予View进行渲染
- 被渲染页面解读数据，调用widget，输出业务相关的部分页面
- 结合layout完成全部页面输出

--- 10 single ---

# 感谢观看 #