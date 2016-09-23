# 脚本说明

有3个顶级命令，分别为daraemon [service | install | depend]

## service 服务管理命令

    命令：`dareamon service {name} {script}`，`name`:服务名称 `script`: 执行的脚本名称 
    例子：`daraemon service mysql start`
    
以`daraemon service mysql start`命令说明处理逻辑：
1. 检查：设定的service_path路径中查找mysql文件夹
1. 如果service_path文件夹中存在env文件，则使用source命令执行env文件
1. 使用source命令载入mysql脚本的start命令

## install 构建命令

    命令：`dareamon install {build script}`
    
    
## depend 依赖管理命令，执行install进行依赖配置

    命令:`dareamon depend [unset|{lib_name}]`,`unset` unset去掉全部的依赖