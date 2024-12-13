# JetLinks 项目脚手架

模块说明

```bash
---jetlinks-project-template
        |--bootstrap 单体项目启动模块
        |--micro-services 微服务相关模块
        |-----|----api-gateway-service API网关服务
        |--modules 子模块
        |-----|----examples  示例相关模块
        |-----|-------|-----crud-examples 增删改查示例
        |-----|-------|-----rule-engine-example 自定义规则引擎节点示例
```

## 使用

### 初始化子模块

```bash
git pull && git submodule init && git submodule update && git submodule foreach git checkout master && git submodule foreach git pull origin master
```

### 配置maven密码

修改maven的`settings.xml`,添加:
```xml
<servers>
    <server>
        <id>jetlinks</id>
        <username>{用户名}</username>
        <password>{密码}</password>
    </server>
</servers>

```

## 开发

项目开发建议使用maven模块化管理,在`modules`目录创建相应的业务模块,然后在`bootstrap`模块中引入依赖进行启动.