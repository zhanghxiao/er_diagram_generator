# ER图生成器 🎨

> 一个让数据库设计变得简单有趣的在线工具

## 简介

厌倦了在白板上画乱七八糟的ER图？受够了复杂的建模软件？这个ER图生成器就是为懒人程序员量身定制的神器！只需要几行简单的代码，就能生成漂亮的实体关系图。
<img width="1892" height="1503" alt="image" src="https://github.com/user-attachments/assets/9efa6859-487d-4c96-9541-724ef7bca1ab" />
<img width="1910" height="923" alt="image" src="https://github.com/user-attachments/assets/b0c7a56a-39a7-4ee9-9394-1fe941f7c385" />
<img width="1910" height="923" alt="image" src="https://github.com/user-attachments/assets/3f4977d2-868f-4d11-b721-eca732ede67c" />

## 特性

**核心功能**
- 简洁的DSL语法，比画图快100倍
- 实时预览，所见即所得
- 现代化的UI设计，颜值在线
- 智能布局算法，自动避免重叠
- 支持SVG和PNG导出

**AI加持**
- 集成AI助手，用自然语言描述需求即可生成ER图
- 支持多种AI服务提供商（OpenAI、Anthropic、自定义API）
- 一键生成，告别手工建模

**用户体验**
- 响应式设计，手机电脑都能用
- 缩放功能，细节一览无余
- 自动保存，再也不怕浏览器崩溃
- 横向滚动支持，大图也不怕

## 快速开始

### 在线使用

直接在浏览器中打开 `index.html`，无需安装任何依赖。

### 基础语法

```
// 定义实体
entity: 用户
  pk: 用户ID
  attr: 用户名
  attr: 邮箱
  attr: 密码

entity: 订单
  pk: 订单号
  attr: 订单金额
  attr: 创建时间

// 定义关系
relation: 下单
  from: 用户 (1)
  to: 订单 (N)
```

### AI生成示例

在AI助手框中输入：
```
创建一个学生选课系统的ER图，包含学生、课程、教师等实体
```

点击"AI生成"，坐等奇迹发生。

## 语法说明

### 实体定义
```
entity: 实体名称
  pk: 主键字段      # 黄色椭圆显示
  attr: 普通属性1   # 灰色椭圆显示
  attr: 普通属性2
```

### 关系定义
```
relation: 关系名称
  from: 源实体 (基数)
  to: 目标实体 (基数)
```

基数支持：`1`、`N`、`M`、`0..1`、`1..*` 等

## AI配置

### 支持的提供商

**OpenAI**
- 模型：gpt-3.5-turbo、gpt-4等
- 需要OpenAI API Key

**Anthropic**
- 模型：claude-3-opus、claude-3-sonnet等
- 需要Anthropic API Key

**自定义API**
- 支持兼容OpenAI格式的任意API端点
- 适配各种开源模型

### 配置步骤

1. 点击顶部"AI配置"按钮
2. 选择提供商并填写API Key
3. 保存配置（仅存储在本地浏览器）
4. 开始使用AI功能

## 导出选项

**SVG格式**
- 矢量图形，无损放大
- 适合打印和进一步编辑

**PNG格式**
- 位图格式，即开即用
- 支持1-5倍缩放，满足不同质量需求

## 技术栈

- 纯HTML/CSS/JavaScript，无需框架
- 现代CSS特性（Grid、Flexbox、CSS Variables）
- SVG动态生成和渲染
- Canvas API用于PNG导出
- LocalStorage用于配置持久化

## 浏览器兼容性

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

基本上，只要不是IE，都能完美运行。

## 项目结构

```
er-diagram-generator/
├── index.html          # 主页面，包含所有功能
├── README.md          # 你正在看的这个文件
└── LICENSE            # MIT协议
```

## 贡献指南

欢迎各种形式的贡献！无论是bug修复、新功能开发还是文档改进。

### 提交Issue

遇到问题？发现bug？有功能建议？直接提Issue，我们会认真对待每一个反馈。

### 提交PR

1. Fork本项目
2. 创建功能分支：`git checkout -b feature/amazing-feature`
3. 提交修改：`git commit -m 'Add some amazing feature'`
4. 推送分支：`git push origin feature/amazing-feature`
5. 创建Pull Request

## 开发计划

**即将到来的功能**
- 更多实体样式选项
- 关系属性支持
- 团队协作功能
- 模板库

**可能会做的功能**
- 从数据库逆向生成ER图
- 导出为其他格式（PDF、Visio等）
- 主题定制
- 插件系统

## FAQ

**Q: 为什么选择单文件架构？**
A: 简单就是美。一个HTML文件包含所有功能，部署方便，学习成本低。

**Q: AI功能是否收费？**
A: 工具本身免费开源，但AI服务需要您自己的API Key，产生的费用由AI服务商收取。

**Q: 数据安全吗？**
A: 所有数据都在您的浏览器本地处理，不会上传到任何服务器。API Key也只存储在本地。

**Q: 支持离线使用吗？**
A: 除了AI功能需要网络外，其他功能都可以离线使用。

## 许可证

本项目基于 [MIT许可证](LICENSE) 开源。

简单来说：你可以随意使用、修改、分发这个项目，甚至用于商业用途，只需要保留原始许可证声明即可。

## 致谢

感谢所有为这个项目提供灵感和帮助的开发者们。特别是那些在Stack Overflow上回答SVG相关问题的英雄们，没有你们就没有这个项目。

---

**如果这个工具帮到了你，记得给个Star⭐**

让更多人发现这个宝藏工具，一起告别手绘ER图的痛苦！
