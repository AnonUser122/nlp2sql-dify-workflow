# NLP2SQL 数据库查询助手 Dify 工作流

这是 `NLP2SQL数据库查询助手` 的 GitHub 项目框架，用于存放 Dify 应用 DSL、工作流截图和效果展示图片。

当前仓库先搭建项目结构和说明文档，DSL 文件与截图后续可自行补充。

## 项目文件

```text
.
├── README.md
├── dsl/
│   └── README.md                 # DSL 文件存放说明
└── assets/
    └── README.md                 # 图片素材存放说明
```

建议后续补充后的目录结构：

```text
.
├── README.md
├── dsl/
│   └── nlp2sql-assistant.yml     # Dify DSL 文件，后续自行上传
└── assets/
    ├── app-home.png              # 应用首页截图
    ├── workflow-canvas.png       # 工作流编排截图
    ├── query-demo.png            # 自然语言查询效果截图
    └── sql-result.png            # SQL/查询结果展示截图
```

## 应用简介

应用名称：`NLP2SQL数据库查询助手`

应用类型：Dify 应用 / 工作流应用

项目目标：让用户通过自然语言描述查询需求，由助手理解问题、生成或辅助生成 SQL，并返回数据库查询结果或查询建议。

## 预期能力

- 理解用户自然语言查询意图。
- 识别涉及的数据表、字段和筛选条件。
- 根据问题生成 SQL 查询语句。
- 执行或辅助执行数据库查询。
- 对查询结果进行自然语言解释。
- 对复杂问题给出澄清提示或查询建议。

## 典型使用场景

- 业务人员用自然语言查询数据。
- 数据分析场景下快速生成 SQL。
- 数据库表结构问答。
- 查询结果解释与总结。
- 企业内部数据助手原型演示。

## DSL 文件位置

请将导出的 Dify DSL 文件放到 `dsl/` 目录下，推荐命名为：

```text
dsl/nlp2sql-assistant.yml
```

上传 DSL 后，可在 Dify 中通过“导入 DSL 文件”的方式恢复应用。

> 注意：请不要提交数据库密码、API Key、Token 等敏感信息。如果 DSL 中包含敏感配置，请先脱敏后再上传。

## 图片展示

请将截图放到 `assets/` 目录，然后替换或使用下面的路径。

### 应用首页截图

![应用首页截图](assets/app-home.png)

### 工作流编排截图

![工作流编排截图1](assets/workflow-canvas.png)
![工作流编排截图2](assets/workflow-canvas1.png)
![工作流编排截图3](assets/workflow-canvas2.png)
![工作流编排截图4](assets/workflow-canvas3.png)
![工作流编排截图5](assets/workflow-canvas4.png)

### 自然语言查询效果截图

![自然语言查询效果截图1](assets/query-demo.png)
![自然语言查询效果截图2](assets/query-demo1.png)
![自然语言查询效果截图3](assets/query-demo2.png)
![自然语言查询效果截图4](assets/query-demo3.png)
![自然语言查询效果截图5](assets/query-demo4.png)

## 导入说明

1. 打开 Dify 控制台。
2. 进入应用列表页面。
3. 选择导入 DSL。
4. 上传 `dsl/nlp2sql-assistant.yml`。
5. 根据本地环境重新配置模型供应商、数据库连接、工具权限和环境变量。
6. 保存并运行测试。

## 配置提醒

导入后通常需要重新配置：

- 大模型供应商与模型名称
- 数据库连接信息
- 工具或插件权限
- 环境变量
- API Key / Token
- SQL 执行安全策略

## 安全建议

NLP2SQL 应用涉及数据库访问，建议：

- 使用只读数据库账号。
- 限制可查询的数据表范围。
- 禁止执行 `INSERT`、`UPDATE`、`DELETE`、`DROP` 等写入或破坏性 SQL。
- 对生成的 SQL 做白名单或人工确认。
- 避免在截图、DSL、README 中暴露真实数据库地址、账号、密码和业务敏感数据。
