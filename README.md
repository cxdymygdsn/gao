# 稿 — gao

**文稿字幕处理工具 — CrispASR GGUF + Qwen3 ASR + Wav2Vec2 **

本项目当前以**闭源包**形式分发，本仓库主要作为产品介绍、版本发布、使用说明及反馈中心。

一键字幕生成、文稿匹配、洗稿、智能分段。支持 9 种语音识别语言，内置 LLM 接口用于文字纠错和翻译。

教程：https://www.bilibili.com/video/BV1UWN46uEiZ/?spm_id_from=333.1387.0.0&vd_source=d6228340c5ff7cd0059e035c8943ee02

---

## 支持语言

| 语言 | 识别引擎 | 对齐模型 |
|------|---------|---------|
| 中文 | qwen3-asr-0.6b | wav2vec2-aligner-zh |
| 英文 | qwen3-asr-0.6b | wav2vec2-aligner-en |
| 日文 | qwen3-asr-0.6b | wav2vec2-aligner-ja |
| 法文 | qwen3-asr-0.6b | wav2vec2-aligner-fr |
| 德文 | qwen3-asr-0.6b | wav2vec2-aligner-de |
| 西班牙文 | qwen3-asr-0.6b | wav2vec2-aligner-es |
| 意大利文 | qwen3-asr-0.6b | wav2vec2-aligner-it |
| 葡萄牙文 | qwen3-asr-0.6b | wav2vec2-aligner-pt |

- 长音频自动静音分块，逐块识别
- CTC 强制对齐生成逐字时间戳

```

### 配置文件

配置文件存储在 `config/` 目录下，每个模块独立文件：

| 文件 | 内容 |
|------|------|
| `env.json` | 模型下载状态、推理引擎设置 |
| `advanced.json` | 高级参数（线程数、GPU 等） |
| `llm.json` | LLM 账户配置 |
| `prompts.json` | 提示词模板 |
| `ui.json` | 主题、界面设置 |

---

## 系统要求

- **Windows 10 / 11**（GPU: NVIDIA CUDA / Vulkan）
- **Python 3.11+**

---

## 注意事项

- 软件目录和模型目录请放在没有中文和空格的路径下
- 首次运行自动生成 `config/` 配置文件
- DaVinci Resolve 推送仅支持 18.5+ Studio 版，不支持 Studio Beta 版本
