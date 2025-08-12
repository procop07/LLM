# LLM - Large Language Model Development Repository

🚀 **Comprehensive LLM development pipeline with Google Colab integration**

This repository provides a complete toolkit for Large Language Model development, including optimized inference notebooks, reinforcement learning training methods, and production-ready Google Colab integration.

## 🎯 Features

- **T4-Safe Inference**: Optimized notebooks for Google Colab T4 GPUs with memory-efficient mixed precision
- **Multiple RL Training Methods**: PPO, DPO, and ORPO implementations for model alignment
- **Ready-to-Use Notebooks**: Pre-configured Colab notebooks for immediate deployment
- **Production-Ready Pipeline**: Error handling, memory optimization, and best practices
- **Comprehensive Dependencies**: Complete requirements.txt for reproducible environments

## 📁 Project Structure

```
LLM/
├── requirements.txt                    # Python dependencies for all notebooks
├── nb/                                # Notebook directory
│   ├── GPT_OSS_MXFP4_(20B)-Inference-T4-safe.ipynb  # GPT inference notebook
│   └── RL/                            # Reinforcement Learning notebooks
│       ├── PPO_colab_demo.ipynb       # Proximal Policy Optimization
│       ├── DPO_colab_demo.ipynb       # Direct Preference Optimization
│       └── ORPO_colab_demo.ipynb      # Odds Ratio Preference Optimization
└── README.md                          # This documentation
```

## 🛠️ Quick Start

### 1. Environment Setup

```bash
# Install dependencies
pip install -r requirements.txt
```

### 2. For Inference

1. Open the [GPT Inference notebook](nb/GPT_OSS_MXFP4_(20B)-Inference-T4-safe.ipynb) in Colab
2. Run all cells to install dependencies
3. Replace the model name with your desired model
4. Execute the inference pipeline

### 3. For Reinforcement Learning Training

1. Choose your preferred RL method:
   - **PPO**: [nb/RL/PPO_colab_demo.ipynb](nb/RL/PPO_colab_demo.ipynb)
   - **DPO**: [nb/RL/DPO_colab_demo.ipynb](nb/RL/DPO_colab_demo.ipynb)
   - **ORPO**: [nb/RL/ORPO_colab_demo.ipynb](nb/RL/ORPO_colab_demo.ipynb)
2. Open the corresponding notebook in Colab
3. Prepare your training data in the specified format
4. Run the training pipeline

## 📚 Notebook Documentation

### 🔥 Inference Notebook

**File**: `nb/GPT_OSS_MXFP4_(20B)-Inference-T4-safe.ipynb`

- **Purpose**: T4-safe inference for large language models (up to 20B parameters)
- **Features**:
  - Mixed precision (FP4) quantization
  - Memory-efficient loading
  - Error handling and safe inference
  - GPU compatibility: T4, P100, V100

### 🎯 Reinforcement Learning Notebooks

#### PPO (Proximal Policy Optimization)
- **Algorithm**: Reinforcement Learning from Human Feedback (RLHF)
- **Use Case**: Policy optimization with reward model integration
- **Features**: Stable training, reward model support

#### DPO (Direct Preference Optimization)
- **Algorithm**: Simpler alternative to RLHF without reward model
- **Use Case**: Preference-based training
- **Features**: No reward model required, stable optimization

#### ORPO (Odds Ratio Preference Optimization)
- **Algorithm**: Reference-model-free alignment
- **Use Case**: Memory-efficient single-stage training
- **Features**: Reduced memory usage, simplified pipeline

## 💡 Usage Tips

- **GPU Requirements**: T4 or higher recommended for inference, P100+ for training
- **Memory Management**: Use gradient checkpointing for large models
- **Batch Sizes**: Start small (1-2) and increase based on available memory
- **Monitoring**: Use wandb integration for experiment tracking

## 📈 Performance Guidelines

| Model Size | Method | T4 GPU | Training Time | Memory Usage |
|------------|--------|--------|---------------|-------------|
| 7B         | DPO    | ✅     | ~2 hours      | ~14GB       |
| 13B        | PPO    | ⚠️     | ~4 hours      | ~15GB       |
| 20B        | ORPO   | ❌     | N/A           | >16GB       |

**Legend**: ✅ Recommended, ⚠️ Possible with optimizations, ❌ Not recommended

## 🔧 Customization

### Adding New Models

1. Update the model name in the notebook configuration
2. Adjust quantization settings if needed
3. Modify generation parameters as required

### Custom Training Data

1. Follow the data format shown in the notebooks
2. Ensure proper prompt-response structure
3. Balance positive and negative examples

## 🚀 Colab Integration

All notebooks are optimized for Google Colab with:

- Automatic dependency installation
- GPU detection and optimization
- Memory management for T4 constraints
- Progress monitoring and logging
- Error handling and recovery

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is open source and available under the MIT License.

## 🔗 Related Resources

- [LLM-colab-pipeline](https://github.com/procop07/LLM-colab-pipeline) - Source repository for pipeline components
- [Issues](https://github.com/procop07/LLM/issues) - Report bugs and request features
- [Discussions](https://github.com/procop07/LLM/discussions) - Community discussions

---

⭐ **If you find this project helpful, please consider giving it a star!**

Made with ❤️ for the LLM community
