<h3 align="center">中文 | <a href="README.en.md">English</a></h3>

# 一、软件简介

HiOCR 是一款面向新手的傻瓜式批量 OCR（文字识别）工具，专为零基础用户处理大量 PDF 文档和图片设计：Windows系统下，双击exe文件打开界面，拖入文件/文件夹即可自动排队，一键开始后全程可视化进度，识别完成自动导出 Markdown或txt文件，无需学习复杂参数与命令。

- 软件名称：HiOCR
- 适配系统：Windows 10/11等系统
- 开发者：马光 （[http://www.maguang.net](http://www.maguang.net/) | [www.haijiaoshi.com](http://www.haijiaoshi.com/)）
- 下载与更新地址1：<https://github.com/maguang/HiOCR>
- 下载与更新地址2：<https://gitee.com/guangma/HiOCR/releases> 

**本软件完全免费！API Key等费用，由各公司收取，和本软件没任何利益关联。**

# 二、功能详解

- API 配置：在配置面板提供多个AI 模型服务商选项。支持"自定义模型"功能：选择下拉列表末尾的"自定义模型"，可输入任意兼容的模型 ID。
- 批量处理：支持拖拽文件夹或多个文件，自动队列处理，实时显示进度，识别成功的文件自动移出列表。
- 智能识别：利用大模型能力识别文字、保留表格结构，部分模型擅长处理中外文古籍和手写体。
- 灵活配置：可调整并发线程数（提高速度）和PDF渲染DPI（提高清晰度）。
- 结果导出：自动保存为Markdown (.md)或txt格式，输出到自定义目录（默认为exe同目录下的"OCR输出"文件夹）。

# 三、模型选择指南

**[推荐配置]**  
* 中外文普通文档：推荐MinerU、智谱 GLM、Paddle-OCR；DPI≤200。  
* 中文古籍和手写体：推荐通义千问、豆包、Gemini；DPI≥300。  
* 外文古籍和手写体：推荐Gemini；DPI≥300。

国内收费模型，2-10元/百万token；Gemini 3，4-20美元/百万token。不同模型各有千秋，建议根据文档类型选择：

| 模型名称 | 费用 | 优点 | 缺点 | API key申请地址 |
|---|---|---|---|---|
| MinerU | 免费 | 每天免费2000页；专为PDF优化 | 古籍识别较差；单文件≤200M、≤600页 | https://mineru.net/apiManage/token |
| OpenRouter | 部分免费 | 模型最全，Gemini3可在大陆使用 | 免费模型可能拥堵，连接困难 | https://openrouter.ai/settings/keys |
| 硅基流动 | 部分免费 | 免费额度高，速度快 | DeepSeek-OCR中文古籍识别较差 | https://cloud.siliconflow.cn |
| 字节豆包 | 付费 | 古籍识别良好 | 有敏感词监测 | https://console.volcengine.com/ark |
| 通义千问 | 付费 | 古籍识别较好 | 敏感词监测严格 | https://bailian.console.aliyun.com |
| 智谱 GLM | 部分免费 | 性价比高 | 极高分辨率精细识别略逊 | https://open.bigmodel.cn |
| Google Gemini | 付费 | 识别最佳 | 国内需VPN；价昂 | https://aistudio.google.com |

# 四、常见问题 (FAQ)

**Q1: 如何升级？**  
A: 可访问Gitee页面：<https://gitee.com/guangma/HiOCR/releases>，或Github页面：<https://github.com/maguang/HiOCR/releases>，或点击"帮助"→"检查更新"。  
下载文件后，解压缩即可。软件加载后，会在根目录下自动生成"user_config.json"配置文件，API key会保存在此处。版本比较大的升级，如添加或删减模型，则需要删除旧版本，然后重新填入API key。
注意：版本比较大的升级，比如从v2.3升级到v2.5.6，因添加或删减了模型，则需要先删除旧版本配置文件，然后重新填入API key。

**Q2: 点击"开始处理"没有反应？**  
A: 请检查是否添加了文件，且 API key 是否已正确设置并通过测试。  
文件上传和PDF拆分预处理，都需要一定的时间，所以大的PDF文档加载也需要一定的时间，请耐心等待。

**Q3: 识别结果乱码或为空？**  
A: 可能是 PDF 每页图片过大导致模型拒识，尝试调低 DPI (如 150)。  
此外，有些模型，比如Qwen内嵌有敏感词检测，触发时，也会无法识别，这个和大语言模型有关，无法避免。

# 五、HiOCR v2.6 更新说明

**✨ 新增功能与外观**

- 新增精简版和完全版两个版本。精简版适合新Windows系统；完全版自带各类安装包，适合缺失各种依赖包的旧电脑。
- 增加检测电脑环境是否缺失的问题。如果缺失，会提示下载和安装方法。
- 优化MinerU输出文件，保留images文件夹下的图片。
- 新增下载地址为gitee.com，确保中国可直接使用。

**🤖 模型生态更新**

- 接入硅基流动两个新模型：PaddleOCR-VL-1.5（免费），Qwen2.5-VL-7B-lnstruct。
- 接入智谱两个新模型：GLM-OCR（性价比较高）和GLM-4.6V-FlashX。

# 六、LICENSE 声明（非商业使用许可）

HiOCR 为免费公开软件，但默认不授予商业用途的使用许可。本软件采用 PolyForm Noncommercial License 1.0.0（SPDX: PolyForm-Noncommercial-1.0.0）授权：

1．允许个人/学校/科研/公益等非商业目的使用与分发。

2．禁止任何商业目的使用（包括但不限于：将本软件/源码集成到收费产品、以本软件提供收费服务、为商业项目交付/代跑/代处理等）。如需商业授权（个人免费 + 企业付费），请联系作者取得书面商业许可。

3．如有需要授权或定制开发，请联系作者。

Copyright © 2025. All Rights Reserved.
