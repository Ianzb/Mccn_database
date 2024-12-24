# 我的世界中国版Api逆向文档
本页面记录了通过多种手段发现的我的世界中国版Api的逆向信息，包括Api的调用方式、参数说明、返回值说明等。

## 说明
未特殊说明的Api均可直接访问。

## Api服务器：
[g79.gdl](https://g79.gdl.netease.com)  
[g79.update](https://g79.update.netease.com/)  
[g79.gph](https://g79.gph.netease.com)  
[x19.gdl](https://x19.gdl.netease.com)  
[x19.update](https://x19.update.netease.com/)  
[x19.gph](https://x19.gph.netease.com/)  
其中，gdl为安装包下载服务器（download），update为更新信息服务器，gph为更新补丁包服务器（patch）。  
x19为端游服务器，g79为手游服务器，但少部分资源位置错误。  
可使用互联网档案馆（archive.org）的前缀搜索功能查看Api服务器的大部分常用Api。

## 端游（x19）
### 更新服务器（update）
#### 1、身份验证服务器[authserver.list](https://x19.update.netease.com/authserver.list)
内容预览：
```
[
  {
    "IP": "45.253.165.190",
    "Port": 10201,
    "ServerType": "dockerB"
  },
  {
    "IP": "45.253.165.190",
    "Port": 10601,
    "ServerType": "dockerB"
  },
  {
    "IP": "45.253.165.190",
    "Port": 10401,
    "ServerType": "dockerB"
  },
  {
    "IP": "45.253.165.190",
    "Port": 10001,
    "ServerType": "dockerB"
  }
]
```
分析：应为登录身份验证服务器，暂时未发现可利用场景。  
也包括[authserver_expr.list](https://x19.update.netease.com/authserver_expr.list)、[authserver_gaiya.list](https://x19.update.netease.com/authserver_gaiya.list)、[authserver_qa.list](https://x19.update.netease.com/authserver_qa.list)、[authserver_sim.list](https://x19.update.netease.com/authserver_sim.list)，内容格式相同但数据不同，但暂时无法确认其具体作用场景。
#### 2、CDN版本（cdnversion）
内容预览：
```
{
    "PreStaticWebVersion": "obt20241107200321",
    "StaticWebVersion": "obt20241107200321"
}
```
分析：出现h5和Web字样，可能与内置浏览器有关，数据内容为日期形式，可能与版本过期检测有关，暂时未发现可利用场景。  
包括[cdnversion/expr_h5version.json](https://x19.update.netease.com/cdnversion/expr_h5version.json)、[cdnversion/obt_h5version.json](https://x19.update.netease.com/cdnversion/obt_h5version.json)、[cdnversion/qa_h5version.json](https://x19.update.netease.com/cdnversion/qa_h5version.json)、[cdnversion/sim_h5version.json](https://x19.update.netease.com/cdnversion/sim_h5version.json)、[cdnversionv2/obt_h5version.json](https://x19.update.netease.com/cdnversionv2/obt_h5version.json)、[cdnversionv2/qa_h5version.json](https://x19.update.netease.com/cdnversionv2/qa_h5version.json)，内容格式类似但数据不同，但暂时无法确认其具体作用场景。
#### 3、聊天服务器[chatserver.list](https://x19.update.netease.com/chatserver.list)
分析：与身份验证服务器类似，暂时未发现可利用场景。
也包括[chatserver_expr.list](https://x19.update.netease.com/chatserver_expr.list)、[chatserver_gaiya.list](https://x19.update.netease.com/chatserver_gaiya.list)、[chatserver_qa.list](https://x19.update.netease.com/chatserver_qa.list)、[chatserver_sim.list](https://x19.update.netease.com/chatserver_sim.list)，内容格式类似但数据不同，但暂时无法确认其具体作用场景。
#### 4、连接服务器（linkserver）
内容预览：
```
[
    {
    	"status": 1,
        "ip": "45.253.179.72",
        "ServerType": "dockerA",
        "id": 902,
        "port": 10000
    },
    {
         "status": 0,
        "ip": "45.253.179.72",
        "ServerType": "dockerB",
        "id": 1902,
        "port": 10001    
    }
]
```
分析：与身份验证服务器类似，但多出status等信息，可能与连接状态有关，暂时未发现可利用场景。
包括[linkserver_expr.list](https://x19.update.netease.com/linkserver_expr.list)、[linkserver_gaiya.list](https://x19.update.netease.com/linkserver_gaiya.list)、[linkserver_qa.list](https://x19.update.netease.com/linkserver_qa.list)、[linkserver_sim.list](https://x19.update.netease.com/linkserver_sim.list)，内容格式类似但数据不同，但暂时无法确认其具体作用场景。