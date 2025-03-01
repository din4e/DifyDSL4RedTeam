# DifyDSL4RedTeam

收集一些红队 Dify Workflow，在 AI 浪潮下赋能红队自动化。  
对应于Ai迷思录（应用与安全指南）[的AI应用篇——网络侦察与威胁情报](https://github.com/Acmesec/theAIMythbook?tab=readme-ov-file#2-%E7%BD%91%E7%BB%9C%E4%BE%A6%E5%AF%9F%E4%B8%8E%E5%A8%81%E8%83%81%E6%83%85%E6%8A%A5) 部分的内容，Dify 安装问题见[链接](https://github.com/langgenius/dify?tab=readme-ov-file#quick-start)。

> 硅基流动注册邀请码 [YWEJ5632](https://cloud.siliconflow.cn/i/YWEJ5632)，实在是谢谢啦😙😙😙😙。

## DSL 简介

### 1. [🐝Bee](docs/bee.md) 

输入目标名称，从 [Hunter](https://hunter.qianxin.com/)、 [Quake](https://quake.360.net/quake/#/index)、[零零信安](https://0.zone/) 获取目标域名和ip。

> 需要配置 Hunter、Quake、零零信安的 API Key

### 2. [🐍Snake](docs/snake.md)

输入项目名称和单位列表，处理数据后获取单位的域名和ip，创建文档用于协作并在飞书群通知。

> 1. 创建飞书应用需要提供，同时群通知机器人需要提供 hook地址 ；
> 2. 依赖于 [Bee](docs/bee.md)，所以需要配置 Hunter、Quake、零零信安的 API Key；

### 3. [🤺Soldier](docs/soldier.md)

手机输入指令，进行扫描任务，例如fscan等（POC版本，非常脆弱，但是非常酷）。

<video src="./images/soldier-demo.mp4" autoplay="true" controls="controls" width="360" height="800">
</video>

> 需要一台 vps；
> 目前依赖于 iphone 快捷指令实现使用，底层还是 API 调用；


## 常见问题汇总

<details>
<summary>
代码执行提示`run failed: The length of output variable result must be less than 30 elements. `
</summary>
将 .env 中`CODE_MAX_STRING_ARRAY_LENGTH`, `CODE_MAX_OBJECT_ARRAY_LENGTH`,` CODE_MAX_NUMBER_ARRAY_LENGTH` 数值从 30 修改为 500。
</details>

<details>
<summary> 
代码执行提示`HTTP Request: Text size is too large, max size is 1.00 MB, but current size is 1.69 MB.`
</summary>
将 .env 中 `HTTP_REQUEST_NODE_MAX_TEXT_SIZE` 扩大到 20971520
</details>

## 免责申明

由于传播、利用开源信息而造成的任何直接或间接的后果及损失，均由使用者本人负责，作者不承担任何责任。  
开源仅作为安全研究之用！切勿用作实战用途！