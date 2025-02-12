---
description: 本页罗列常用的训练云平台，python packages, 常用datasets,  一些NLP， 多模态模型版本等
---

# 0-Setup

## 1. Platforms



|              |   |   |
| ------------ | - | - |
| ModelScope魔方 |   |   |
| kaggle       |   |   |
| Google Colab |   |   |
| ali cloud    |   |   |

## 2. Packages



package 类型:

1. base package
2. data
3. model
   1. parameter
   2. model structure
4. training
   1. training strategy： DPO, PPO, GRPO,
   2. distillation:  CoT distillation
5. inference
   1. pruning
   2. serving speedup
   3. inference strategy:
      1. CoT

| 库                    | 类型                   | 描述                                                                                                                                                                                                      |
| -------------------- | -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| torch                | base package         | 基础深度学习库                                                                                                                                                                                                 |
| transformers         | training             | huggingface集成各种深度学习ai模型的包                                                                                                                                                                               |
| trl                  |  training            | <p>transformer reinforcement learning</p><p>强化学习策略包</p><p>(包括PPO, DPO, GRPO)</p><p><a href="https://github.com/huggingface/trl?tab=readme-ov-file">url</a></p>                                          |
| peft                 | training             | <p>parameter-efficient-FineTuning</p><p> 支持lora等小参数微调包</p><p><a href="https://github.com/huggingface/peft">url</a></p>                                                                                  |
| Accelerate           | training             | <p>huggingface 把各种训练推理加速优化的工具(deepspeed, megatron-LM等集成到accelerate这种即插即用的包里)</p><p><a href="https://huggingface.co/docs/accelerate/usage_guides/deepspeed">url</a></p>                                  |
| deepspeed            | training + inference | <p></p><p></p><ul><li>通常用于中小型企业或需要更灵活应用的场景，如教育、语音识别等领域。</li><li>更注重轻量化和高效性，适用于资源有限的情况。</li></ul><p><a href="https://github.com/deepspeedai/DeepSpeed">url</a></p>                                       |
| megatron             | training + inference | <p></p><ul><li>强大的训练性能，适合大规模模型构建和优化。</li><li>使用混合精度计算，提升浮点运算速度和稳定性。</li><li>支持多任务并行，优化模型的架构设计。</li></ul><p><a href="https://github.com/NVIDIA/Megatron-LM?tab=readme-ov-file#gpt-3-example">url</a></p> |
| RAG 部分               |                      |                                                                                                                                                                                                         |
| langchain            |                      | 更加高层的封装应用， 支持RAG部署， 请求接口，网络连接等等应用层接口                                                                                                                                                                    |
| huggingfaceEmbedding |                      | [http://www.hubwiz.com/blog/deepseek-r1-powered-rag-system-hands-on/](http://www.hubwiz.com/blog/deepseek-r1-powered-rag-system-hands-on/)                                                              |
| llama\_index         |                      | 向量化索引                                                                                                                                                                                                   |
| ipex\_index          |                      |                                                                                                                                                                                                         |
|                      |                      |                                                                                                                                                                                                         |



## 3. Datasets





## 4. Models





