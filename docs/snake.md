# 🐍 Snake

输入项目名称和单位列表，处理数据后获取单位的域名和ip，创建文档用于协作并在飞书群通知。

 
![snake](../images/snake.png)


## 操作步骤

1. 复制 [DSL 连接](https://github.com/din4e/DifyDSL4RedTeam/blob/main/dsl/snake.yml)
   
    ![bee step 1](../images/bee-p1.png)

2. `工作室 > 导入 DSL 文件 > URL`

    ![bee step 2](../images/bee-p2.png)

3. 先引入 [🐝Bee](./bee.md)，完成相关配置，输入修改为循环的 `/item`，修改联通和相关失效变量

    ![snake step 3](../images/snake-p3.png)

4. 配置飞书应用 `app_id`、`app_asccess_token`并开通相应权限，需要在授权和环境变量中配置
   
    ![snake step 4](../images/snake-p4.png)
    ![snake step 6](../images/snake-p6.png)
    ![snake step 6.1](../images/snake-p6.1.png)
    
5. 添加以及机器人 Webhook 地址，需要配置自定义关键词确保消息推送
   
    ![snake step 7](../images/snake-p7.png)
    ![snake step 8](../images/snake-p8.png)

6. 运行！

    ![snake step 9](../images/snake-p9.png)

## 注意事项

1. [[🐝Bee]](./bee.md) 目前零零信安误报较高；
2. [[🐝Bee]](./bee.md) Hunter、Quake暂不支持大数据量的分页；