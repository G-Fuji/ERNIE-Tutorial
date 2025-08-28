# ERNIE Tutorial Series

<div align="center">
  <a href="README_zh.md">
    <img src="https://img.shields.io/badge/语言-中文-blue?style=for-the-badge" alt="中文版">
  </a>
  <a href="README.md">
    <img src="https://img.shields.io/badge/Language-English-red?style=for-the-badge" alt="English">
  </a>
</div>

<br>

> A comprehensive tutorial series for ERNIE large language model development, covering pretraining, supervised fine-tuning, direct preference optimization, and practical applications.

## 🌟 Project Overview

This is a comprehensive tutorial series focused on **ERNIE large language model development**, designed to help developers master the complete workflow from model pretraining to practical deployment. Using **ERNIE-4.5-0.3B** as an example model, we provide detailed tutorials covering core training techniques, practical applications, and deployment strategies.

### 🎯 What You'll Learn
- **Core Training Techniques**: Pretraining, Supervised Fine-tuning (SFT), Direct Preference Optimization (DPO)
- **Practical Applications**: Sentiment analysis, text classification, dialogue systems
- **Development Tools**: ERNIEKit official toolkit, PaddlePaddle framework
- **Best Practices**: Data processing, model configuration, training optimization, deployment strategies

## 📖 Tutorial Series

### 🎯 Core Training Tutorials (`training-tutorials/`)

| Tutorial | Core Technology | Data Format | Learning Focus | Target Audience |
|----------|-----------------|-------------|----------------|------------------|
| 📚 [Pretraining Tutorial (PT)](training-tutorials/01-pretraining/) | Next Token Prediction<br/>Transformer Architecture | `.bin/.idx` format | Large-scale unsupervised training<br/>Building language models from scratch | Deep learning basics<br/>Understanding pretraining principles |
| 🎯 [Supervised Fine-tuning Tutorial (SFT)](training-tutorials/02-supervised-finetuning/) | Instruction tuning<br/>Dialogue template design | `jsonl` format<br/>`src`/`tgt` fields | Instruction data processing<br/>Dialogue capability training | Assistant app development<br/>Dialogue system construction |
| 🔄 [Direct Preference Optimization Tutorial (DPO)](training-tutorials/03-direct-preference-optimization/) | Human preference alignment<br/>DPO algorithm | Triplet format<br/>`prompt`/`chosen`/`rejected` | Reward-free training<br/>Output quality improvement | Model safety alignment<br/>Advanced optimization techniques |
| 💡 [Chinese Sentiment Analysis Tutorial](training-tutorials/04-sentiment-analysis/) | Text classification<br/>End-to-end application | Labeled sentiment data | Business scenario application<br/>Model deployment practice | Real project development<br/>NLP application implementation |

### 🚀 Deployment Tutorials (`deployment-tutorials/`)

| Tutorial | Technology Stack | Deployment Method | Learning Focus | Target Audience |
|----------|------------------|-------------------|----------------|------------------|
| 📦 [Ollama Deployment Tutorial](deployment-tutorials/Ollama/ollama_ernie_deployment_tutorial.ipynb) | Ollama + ERNIE-4.5-0.3B | Local deployment<br/>One-click setup | Quick model deployment<br/>Local inference service | Developers<br/>Local testing scenarios |
| ⚡ [vLLM Deployment Tutorial](deployment-tutorials/vLLM/vllm_ernie_deployment_tutorial.ipynb) | vLLM + PyTorch | High-performance inference<br/>Production deployment | GPU acceleration<br/>Batch processing optimization | Production environments<br/>High-throughput scenarios |
| 🚀 [SGLang Deployment Tutorial](deployment-tutorials/SGLang/sglang_ernie_deployment_tutorial.ipynb) | SGLang + PyTorch | High-performance inference | GPU acceleration<br/>Structured generation | Developers<br/>Research |

### Coming Soon
- 🎨 **Creative Applications**: Chatbots, content generation, code assistants

## 🛠️ Tech Stack

| Category | Component | Version | Description |
|----------|-----------|---------|-------------|
| **Core Framework** | PaddlePaddle | Latest | Deep learning training framework |
| | ERNIEKit | Latest | Baidu's official large model development toolkit |
| | ERNIE-4.5-0.3B | - | Example pretrained model (300M parameters) |
| **Data Format** | `.bin/.idx` | - | Pretraining data (mmap format) |
| | `jsonl` | - | SFT/DPO data (instruction-response pairs/preference triplets) |
| **Training Tech** | Full/LoRA Fine-tuning | - | Parameter update strategies |
| | DPO | - | Direct preference optimization |
| **Tools** | TensorBoard/VisualDL | - | Training visualization |

## 🚀 Quick Start

### Environment Requirements
- **Python**: 3.10
- **PaddlePaddle**: Latest version (GPU version)
- **ERNIEKit**: Latest version
- **GPU**: Recommended single 80GB A/H series GPU, minimum 24GB VRAM
- **Operating System**: Linux/Windows/macOS

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/ERNIE-Tutorial.git
cd ERNIE-Tutorial

# Install PaddlePaddle GPU version (recommended)
python -m pip install paddlepaddle-gpu==3.1.0 -i https://www.paddlepaddle.org.cn/packages/stable/cu126/

# Clone ERNIEKit repository
git clone https://github.com/PaddlePaddle/ERNIE.git -b develop

# Install ERNIEKit dependencies
cd ERNIE
pip install -r requirements/gpu/requirements.txt

# First install aistudio-sdk library
pip install --upgrade aistudio-sdk
# Use aistudio cli to download model
aistudio download --model PaddlePaddle/ERNIE-4.5-0.3B-Paddle --local_dir baidu/ERNIE-4.5-0.3B-Paddle
```


## 🤝 Contributing

We welcome all forms of contributions! Whether it's finding bugs, suggesting improvements, or contributing new tutorial content.

### Ways to Contribute
- 🐛 **Bug Reports**: Submit [Issues](https://github.com/G-Fuji/ERNIE-Tutorial/issues) for any problems found
- 💡 **Feature Suggestions**: Discuss ideas in [Discussions](https://github.com/G-Fuji/ERNIE-Tutorial/discussions)
- 📝 **Documentation**: Help improve tutorial content and code comments
- 🔧 **Code Contributions**: Submit Pull Requests for new features or fixes
- 🎓 **Tutorial Extensions**: Contribute new application scenarios and practical cases

### Contribution Process
1. Fork this project to your GitHub account
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Make your changes and ensure code quality
4. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
5. Push to your branch (`git push origin feature/AmazingFeature`)
6. Open a Pull Request with detailed description of your changes

### Code Standards
- Follow PEP 8 Python coding standards
- Add appropriate comments and documentation for new features
- Ensure all example code runs correctly
- Update relevant README and configuration files

## 📄 License

This project is licensed under the [Apache 2.0 License](LICENSE). You are free to use, modify, and distribute the code in this project, but please retain the original license statement.

## 📞 Contact Us

- **Project Maintainers**: ERNIE Tutorial Team
- **Technical Exchange**: Welcome to ask technical questions in Issues
- **WeChat Contact**: G_Fuji

## 🙏 Acknowledgments

Thanks to the following projects and teams for their support:
- [Baidu PaddlePaddle](https://github.com/PaddlePaddle/Paddle) - Deep learning framework
- [ERNIEKit](https://github.com/PaddlePaddle/ERNIE) - Official model development toolkit
- [ERNIE Model Team](https://aistudio.baidu.com/modelsoverview) - Providing powerful pretrained models
- All contributors and users for their feedback and support

---

⭐ **If this project helps you, please give us a Star! Your support motivates us to keep improving.**

🚀 **Start your ERNIE large model learning journey!**

🔗 **Related Links**
- [AI Studio](https://aistudio.baidu.com/)
- [PaddlePaddle Official Website](https://www.paddlepaddle.org.cn/)
- [ERNIEKit GitHub Repository](https://github.com/PaddlePaddle/ERNIE)