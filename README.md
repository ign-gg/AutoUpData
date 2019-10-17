# AutoUpData
根据Github仓库 更新插件
## 开发者须知
1. 首先您拥有GitHub仓库
2. 保证版本格式为 v1.0.0 或 1.0.0
3. 插件名称为 `AutoUpData`
## 如何使用
请在 `plugin.yml`内增加
```
loadbefore:
  - AutoUpData
```
否则会出现null异常BUG
执行以下代码
```
import updata.AutoData;
/**
* @parm PluginBase plugin
* @parm String user GitHub用户名
* @parm String project 工程名称
* @return 是否更新完毕
* 获取接口
*/
/**
* 获取接口前请先判断插件是否存在
*/
UpData data = AutoData.get(plugin,user,project);
/**
* 在使用data参数前请先判断是否为null
*/
/*
* 判断是否存在新版本
* @return Boolean
*/
data.canUpdate();
/*
* 获取新版本名称
* @return String 版本名 格式: 1.0.0
*/
data.getNewVersion();
/*
* 使插件更新
*/
data.toUpData();
```
