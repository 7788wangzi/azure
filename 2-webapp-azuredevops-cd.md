## 使用Azure CLI创建webapp

**登录Azure Account**
在命令行工具中运行:
```
az login
```
在弹出的浏览器窗口中输入用户名密码登录。

列出账号下的所有订阅:
```
az account list --output table
```
--output table是以表格形式输出结果。

切换订阅:
```
az account set -s <id>
```

**创建资源组，托管计划和应用程序**  

创建资源组
```
az group create -l westus -n <resource-group name>
```

创建应用程序托管计划
```
az appservice plan create -g <resource-group name> -n <app-plan name>
```

创建应用程序
```
az webapp create -g <resource-group name> -p <app-plan name> -n <webapp name>
```

## 在Azure Portal中设置自动化部署方案

