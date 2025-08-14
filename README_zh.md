# ERNIE 大语言模型教程系列

<div align="center">
  <a href="README_zh.md">
    <img src="https://img.shields.io/badge/语言-中文-blue?style=for-the-badge" alt="中文版">
  </a>
  <a href="README.md">
    <img src="https://img.shields.io/badge/Language-English-red?style=for-the-badge" alt="English">
  </a>
</div>

<br>

> 🚀 基于 ERNIEKit 的完整大语言模型开发教程，从理论到实践的全方位指南

## 📖 教程概览

本项目是一个全面的 ERNIE 大语言模型教程系列，旨在为开发者提供从基础理论到实际应用的完整学习路径。我们以 **ERNIE-4.5-0.3B** 作为示例模型，深入探索大语言模型的核心技术和应用实践。

### 🎯 教程特色

- **理论与实践并重**：每个教程都包含详细的理论解释和完整的代码实现
- **循序渐进**：从基础的预训练到高级的偏好优化，逐步深入
- **官方工具链**：基于百度官方的 ERNIEKit 开发套件和 PaddlePaddle 框架
- **实战导向**：包含真实场景的应用案例和项目实践
- **中文友好**：专门针对中文语言模型的优化和应用
- **资源友好**：所有教程都可在单张消费级GPU上完成

## 🗂️ 教程系列

### 核心训练教程 (`training-tutorials/`)

| 教程 | 核心技术 | 数据格式 | 学习重点 | 适合人群 |
|------|----------|----------|----------|----------|
| 📚 [预训练教程 (PT)](training-tutorials/01-pretraining/) | Next Token Prediction<br/>Transformer架构 | `.bin/.idx` 格式 | 大规模无监督训练<br/>从零构建语言模型 | 深度学习基础<br/>想了解预训练原理 |
| 🎯 [监督微调教程 (SFT)](training-tutorials/02-supervised-finetuning/) | 指令调优<br/>对话模板设计 | `jsonl` 格式<br/>`src`/`tgt` 字段 | 指令数据处理<br/>对话能力训练 | 助手类应用开发<br/>对话系统构建 |
| 🔄 [直接偏好优化教程 (DPO)](training-tutorials/03-direct-preference-optimization/) | 人类偏好对齐<br/>DPO算法 | 三元组格式<br/>`prompt`/`chosen`/`rejected` | 无奖励模型训练<br/>输出质量提升 | 模型安全对齐<br/>高级优化技术 |
| 💡 [中文情感分析实战教程](training-tutorials/04-sentiment-analysis/) | 文本分类<br/>端到端应用 | 标注情感数据 | 业务场景应用<br/>模型部署实践 | 实际项目开发<br/>NLP应用落地 |

### 即将推出

- **部署教程** (`deployment-tutorials/`)：模型量化、推理优化、服务部署
- **创意应用** (`creative-applications/`)：基于 ERNIE 的创新应用案例

## 🛠️ 技术栈

| 类别 | 技术组件 | 版本要求 | 用途说明 |
|------|----------|----------|----------|
| **核心框架** | PaddlePaddle | 最新版 | 深度学习训练框架 |
| | ERNIEKit | 最新版 | 百度官方大模型开发套件 |
| | ERNIE-4.5-0.3B | - | 示例预训练模型（300M参数） |
| **数据格式** | `.bin/.idx` | - | 预训练数据（mmap格式） |
| | `jsonl` | - | SFT/DPO数据（指令-回答对/偏好三元组） |
| **训练技术** | 全参数微调/LoRA | - | 参数更新策略 |
| | DPO | - | 直接偏好优化 |
| **工具** | TensorBoard/VisualDL | - | 训练可视化 |

## 🚀 快速开始

### 环境要求

- **Python**: 3.10
- **PaddlePaddle**: 最新版本 (GPU版本)
- **ERNIEKit**: 最新版本
- **GPU**: 推荐单张 80GB A/H 系列GPU，最低 24GB 显存
- **系统**: Linux/Windows/macOS

### 安装依赖

```bash
# 克隆项目
git clone https://github.com/your-username/ERNIE-Tutorial.git
cd ERNIE-Tutorial

# 安装 PaddlePaddle GPU 版本
pip install paddlepaddle-gpu==3.1.0 -i https://www.paddlepaddle.org.cn/packages/stable/cu126/

# 克隆 ERNIEKit 仓库
git clone https://github.com/PaddlePaddle/ERNIE.git -b develop

# 安装 ERNIEKit 依赖
cd ERNIE
pip install -r requirements/gpu/requirements.txt

# 首先请先安装aistudio-sdk库
pip install --upgrade aistudio-sdk
# 使用aistudio cli下载模型
aistudio download --model PaddlePaddle/ERNIE-4.5-0.3B-Paddle --local_dir baidu/ERNIE-4.5-0.3B-Paddle
```

### 选择学习路径

| 路径类型 | 学习顺序 | 适合人群 |
|----------|----------|----------|
| **🔰 初学者** | 预训练 → 监督微调 → 情感分析实战 | 深度学习基础，想系统学习 |
| **🚀 进阶者** | 基础概念 → 直接偏好优化 → 高级应用 | 有ML经验，关注前沿技术 |
| **💼 实战者** | 情感分析实战 → 按需回顾理论 → 业务应用 | 解决具体问题，快速上手 |

## 📁 项目结构

### 🎯 核心训练教程 (`training-tutorials/`)
| 教程目录 | 主要文件 | 数据格式 | 输出内容 |
|----------|----------|----------|----------|
| `01-pretraining/` | `pretraining_tutorial.ipynb` | `.bin/.idx` 格式 | 预训练模型权重、日志、检查点 |
| `02-supervised-finetuning/` | `supervised_finetuning.ipynb` | `.jsonl` 格式 | 微调模型、训练日志 |
| `03-direct-preference-optimization/` | `dpo_tutorial.ipynb` | 三元组格式 | DPO优化模型、结果 |
| `04-sentiment-analysis/` | `sentiment_analysis.ipynb` | 标注数据 | 分类模型、演示应用 |

### 🚀 即将推出的教程
| 目录 | 内容规划 |
|------|----------|
| `deployment-tutorials/` | 模型量化、推理优化、服务部署 |
| `creative-applications/` | 对话机器人、内容生成、代码助手 |
| `docs/` | 安装指南、问题排查、API参考 |
| `assets/` | 教程图片、演示视频 |

## 📚 教程特点

| 特点类别 | 核心优势 | 具体体现 |
|----------|----------|----------|
| **🎯 实用性强** | 真实场景应用 | OpenWebTextCorpus数据、端到端流程、官方ERNIEKit标准、性能优化技巧 |
| **🔬 技术深度** | 原理与实践并重 | Transformer/DPO算法解析、代码逐行详解、方法对比分析、前沿技术覆盖 |
| **🛠️ 易于上手** | 降低学习门槛 | 单GPU支持、详细文档、模块化设计、丰富示例代码 |

## 🤝 贡献指南

我们欢迎所有形式的贡献！无论是发现bug、提出改进建议，还是贡献新的教程内容。

### 贡献方式
- 🐛 **Bug 报告**: 发现问题请提交 [Issue](https://github.com/your-username/ERNIE-Tutorial/issues)
- 💡 **功能建议**: 有好想法请在 [Discussions](https://github.com/your-username/ERNIE-Tutorial/discussions) 中讨论
- 📝 **文档改进**: 帮助完善教程内容和代码注释
- 🔧 **代码贡献**: 提交 Pull Request 贡献新功能或修复
- 🎓 **教程扩展**: 贡献新的应用场景和实战案例

### 贡献流程
1. Fork 本项目到您的 GitHub 账户
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 进行您的修改并确保代码质量
4. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
5. 推送到您的分支 (`git push origin feature/AmazingFeature`)
6. 开启 Pull Request 并详细描述您的更改

### 代码规范
- 遵循 PEP 8 Python 代码规范
- 为新功能添加适当的注释和文档
- 确保所有示例代码都能正常运行
- 更新相关的 README 和配置文件

## 📄 许可证

本项目采用 [Apache 2.0 许可证](LICENSE)。您可以自由使用、修改和分发本项目的代码，但请保留原始许可证声明。

## 📞 联系我们

- **项目维护者**: ERNIE Tutorial Team
- **问题反馈**: [GitHub Issues](https://github.com/your-username/ERNIE-Tutorial/issues)
- **功能讨论**: [GitHub Discussions](https://github.com/your-username/ERNIE-Tutorial/discussions)
- **技术交流**: 欢迎在 Issues 中提出技术问题
- **微信联系**: G_Fuji

## 🙏 致谢

感谢以下项目和团队的支持：
- [百度 PaddlePaddle](https://github.com/PaddlePaddle/Paddle) - 深度学习框架
- [ERNIEKit](https://github.com/PaddlePaddle/ERNIE) - 官方模型开发套件
- [ERNIE 模型团队](https://wenxin.baidu.com/) - 提供强大的预训练模型
- 所有贡献者和使用者的反馈与支持

---

⭐ **如果这个项目对您有帮助，请给我们一个 Star！您的支持是我们持续改进的动力。**

🚀 **开始您的 ERNIE 大模型学习之旅吧！**

🔗 **相关链接**
- [ERNIE 官方文档](https://ernie-bot.baidu.com/)
- [PaddlePaddle 官网](https://www.paddlepaddle.org.cn/)
- [ERNIEkit GitHub](https://github.com/PaddlePaddle/ERNIE)