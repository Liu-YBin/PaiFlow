# PaiFlow

## 项目简介

PaiFlow（派派工作流）是一个面向企业场景的 AI Agent 工作流编排平台，基于可视化节点将大模型、工具、条件分支和业务逻辑组织成可执行流程。用户可以通过拖拽方式搭建工作流，配置模型和工具，实时查看执行过程，并将复杂的 AI 应用快速落地。

## 实现功能

- **可视化工作流编排**：支持拖拽式节点编排、参数配置、流程预览和调试。
- **LLM 节点**：统一接入 DeepSeek、OpenAI、通义千问等大模型，支持自定义提示词和模型参数。
- **工具与插件节点**：支持工具注册、MCP 协议和外部插件调用，扩展 Agent 的实际执行能力。
- **流程控制**：支持条件分支、节点依赖、DAG 链路解析和独立节点执行。
- **并行执行**：对无依赖节点进行并行调度，提高复杂工作流的执行效率。
- **实时流式输出**：基于 SSE 推送节点状态、模型输出和执行日志，支持边执行边查看结果。
- **Agent 编排**：支持将模型节点、工具节点和业务节点组合成可复用的智能体流程。
- **知识与记忆能力**：支持知识库、RAG 检索以及工作流上下文和执行状态管理。
- **多租户与权限管理**：提供用户、租户、模型配置和工作流资源的统一管理。

## 核心模块

```text
PaiFlow/
├── console/
│   ├── backend/                # Spring Boot 控制台服务
│   └── frontend/               # React 工作流编排界面
├── core-workflow-java/         # 工作流执行引擎
├── docker/                     # Docker Compose 部署配置
├── docs/                       # 项目文档
└── scripts/                    # 构建和运维脚本
```

## 技术栈

- **开发语言与框架**：Java 21、Spring Boot 3.5、Spring AI、LangGraph4J
- **前端交互**：React 18、TypeScript、Ant Design、ReactFlow、Monaco Editor、Vite
- **数据访问**：MyBatis-Plus、MySQL、Redis
- **对象存储**：MinIO
- **协议与通信**：REST、SSE、MCP、OpenTelemetry
- **部署方式**：Docker、Docker Compose、Nginx





