<h3 align="center"><a href="README.md">中文</a> | English</h3>

# 1. Overview

HiOCR is a beginner-friendly, drag-and-drop batch OCR (text recognition) tool built for people who need to process large numbers of PDFs and images without dealing with complex parameters or command-line workflows. On Windows, simply double-click the `.exe` to launch the app, drag files or folders to create a queue automatically, click Start, and follow the visual progress. When finished, HiOCR exports results automatically as Markdown or plain text.

- Name: HiOCR
- Latest version: v2.5.6
- Supported OS: Windows 10/11
- Developer: Guang Ma ([maguang.net](http://www.maguang.net/) | [haijiaoshi.com](http://www.haijiaoshi.com/))
- Download & updates (GitHub): https://github.com/maguang/HiOCR
- Download & updates (Baidu Netdisk): https://pan.baidu.com/s/1WchKiuVp9kKkqj4yqSBg4Q?pwd=6666 (code: 6666)
- Last updated: 2026-01-18

**HiOCR itself is completely free.** Any API-key or usage fees are charged by the model providers, and are not affiliated with this software.

# 2. Features

- API configuration: Choose from multiple AI model providers in the settings panel. HiOCR also supports a **Custom model** option—select it at the bottom of the dropdown and enter any compatible model ID.
- Batch processing: Drag and drop folders or multiple files. HiOCR queues them automatically, shows real-time progress, and removes successfully processed items from the list.
- Smart recognition: Uses multimodal/LLM-based OCR to extract text while preserving table structure. Some models are particularly good at historical documents and handwriting (Chinese and non-Chinese).
- Flexible tuning: Adjust the number of concurrent workers (for speed) and PDF render DPI (for clarity).
- Export: Automatically saves results as Markdown (`.md`) or plain text (`.txt`) to a chosen output folder (default: an `OCR输出` folder next to the `.exe`).

# 3. Model Selection Guide

**Recommended settings**
- Modern Chinese & English documents: MinerU, Zhipu GLM, DeepSeek-OCR; DPI ≤ 200.
- Chinese classics & handwriting: Qwen, Doubao, Gemini; DPI ≥ 300.
- Non-Chinese classics & handwriting: Gemini; DPI ≥ 300.

Most China-based paid models cost around 2–9 CNY per 1M tokens; Gemini 3 costs around 4–20 USD per 1M tokens. Each model has its own strengths—choose based on document type.

| Model | Pricing | Pros | Cons | API key |
|---|---|---|---|---|
| MinerU | Free | 2,000 pages/day free; optimized for PDFs | Weak on classics; single file ≤ 200 MB / ≤ 600 pages | https://mineru.net/apiManage/token |
| OpenRouter | Partly free | Broadest model catalog; Gemini 3 can be used in Mainland China | Free models may be congested; connectivity can be unstable | https://openrouter.ai/settings/keys |
| SiliconFlow | Partly free | Large free quota; fast | DeepSeek-OCR may struggle with Chinese classics | https://cloud.siliconflow.cn |
| ByteDance Doubao | Paid | Good for classics | Sensitive-content filtering | https://console.volcengine.com/ark |
| Qwen (Tongyi) | Paid | Strong on classics | Strict sensitive-content filtering | https://bailian.console.aliyun.com |
| Zhipu GLM | Partly free | Great value for money | Slightly weaker for very high-resolution fine details | https://open.bigmodel.cn |
| Google Gemini | Paid | Best recognition quality | VPN required in Mainland China; expensive | https://aistudio.google.com |

# 4. FAQ

**Q1: How do I upgrade?**  
A: Visit https://github.com/maguang/HiOCR/releases, or click **Help → Check for updates** in the app.  
After downloading, unzip and run. On first launch, HiOCR creates a `user_config.json` file in the root directory, and your API key is stored there. For major upgrades that add or remove models, delete the old version and re-enter the API key.  
Note: For larger jumps (e.g., v2.3 → v2.5.6) where models were added/removed, delete the old configuration file first, then re-enter the API key.

**Q2: Nothing happens after I click “Start”.**  
A: Check that you have added files and that your API key is set correctly and passes the connection test.  
Uploading files and PDF splitting/preprocessing can take time—large PDFs may appear to “hang” while loading, so please wait.

**Q3: The output is garbled or empty.**  
A: This may happen if the images embedded in the PDF are too large and the model refuses to process them—try lowering the DPI (e.g., 150).  
Also note that some models (such as Qwen) include sensitive-content filtering; when triggered, recognition may fail. This is model-side behavior and cannot be fully avoided.

# 5. HiOCR v2.5.6 Release Notes

**✨ New features & UI**
- Added `.txt` export (default remains `.md`).
- Faster model switching via asynchronous pre-warm (near-instant switching).
- Added update checking (VPN may be required in some regions).
- Default output folder is now relative: an `OCR输出` folder next to the `.exe`.
- Improved UI compatibility on low-resolution displays (not guaranteed on every setup).

**🤖 Model ecosystem updates**
- Added new OpenRouter models: a new free model `GLM-4.6V-Flash`, plus higher-tier `gemini-3-pro-preview` and `gemini-3-flash-preview` to cover different accuracy needs.
- Removed deprecated models: `doubao-1-5-vision-lite-250315` and `doubao-1-5-vision-pro-250328` (officially discontinued), and added the latest `doubao-seed-1-8-251228`.

# 6. License (Noncommercial)

HiOCR is free and publicly available, but it does **not** grant default permission for commercial use. This project is licensed under the PolyForm Noncommercial License 1.0.0 (SPDX: `PolyForm-Noncommercial-1.0.0`). 

1. You may use and redistribute it for noncommercial purposes (e.g., personal use, schools, research, and public-interest projects).  
2. Commercial use is prohibited, including (but not limited to) integrating this software/source into paid products, selling paid services based on it, or delivering/running it for commercial projects. If you need a commercial license (free for individuals + paid for companies), contact the author for written permission.  
3. For licensing or custom development, please contact the author.

Copyright © 2025. All Rights Reserved.
