# 模式化监控

>用于代替力控模式化监控的测试项目


### 开发环境
    1.拥有nodejs环境 v6.0.0以上
    2.执行npm run install 下载所需要的依赖包
    3.执行npm run dev 进入开发环境
### 产品环境
    1.1.拥有nodejs环境 v16.50
    2.执行npm run install 下载所需要的依赖包
    3.执行npm run build 生产dist文件
    4.将文件夹下内容移动的web服务器目录下。（以文件的形式打不开）
## 目录结构
    build：与项目构建（webpack）相关代码
    config：配置目录
    node_modules：项目依赖包
    src：开发主目录
        assets：静态资源
            img：图片
            style：样式
        components：封装的组件
        page：页面
        router：路由
        store：状态机
        tools：封装的工具函数
        app.vue:页面入口文件
        main.js:程序入口文件
    static：静态资源（类库等）
    index.html：首页入口文件
    package.json：配置文件
## 使用接口格式
    1.读取历史数据
        参数:{点集合，开始时间，结束时间，查询数量}
            tags:["data\\tag1","data\\tag2"] 格式：节点名\\点名  
            sTime:1635146177434 格式：timestamp 
            eTime:1635146177434 格式：timestamp
            count:2   格式：number
        返回示例：
            [[tag1,tag1],[tag2,tag2],[tag3,tag3]]
    2.读取实时数据
        参数：{点集合}
            tags:["data\\tag1","data\\tag2"] 格式：节点名\\点名  
        返回示例：
            [tag1,tag2]
## 使用的依赖包
    axios ：用于发送请求
    core-js： ie兼容es6
    dayjs：轻量级时间处理
    echarts：数据可视化图表库
    element-ui：有赞组件库
## 实现功能
    1.实时查询（并通过散点图、折线图、仪表盘和表格展示）
    2.历史查询（并通过散点图、折线图、仪表盘和表格展示）
