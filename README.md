<h1>HiOCR批量文字识别工具免费下载与说明</h1>
<hr />

<h2>一、软件简介</h2>
<hr />
<p>HiOCR 是一款面向新手的傻瓜式批量 OCR（文字识别）工具，专为零基础用户处理大量 PDF 文档和图片设计：拖入文件/文件夹即可自动排队，一键开始后全程可视化进度，识别完成自动导出 Markdown文件，无需学习复杂参数与命令。</p>

<h3>[核心亮点]</h3>
<ul>
    <li><strong>批量处理</strong>：支持拖拽文件夹或多个文件，自动队列处理。</li>
    <li><strong>多模型支持</strong>：集成硅基流动（DeepSeek-OCR）、MinerU、阿里通义千问、字节豆包、Google Gemini等。</li>
    <li><strong>智能识别</strong>：利用大模型能力，识别文字、保留表格结构。</li>
    <li><strong>结果导出</strong>：自动保存为 Markdown (.md) 格式，方便编辑和阅读。.md文件可以右键使用“记事本”打开，也可以下载安装Typora、MarkText、VS Code等打开。</li>
</ul>

<h2>二、功能详解</h2>
<hr />
<ul>
    <li><strong>API 配置</strong><br />在右侧面板配置不同的 AI 模型服务商。</li>
    <li><strong>参数调整</strong><br />支持调整并发线程数（提高速度）、PDF 渲染 DPI（提高清晰度）。</li>
    <li><strong>任务管理</strong>
        <ul>
            <li>添加文件：点击按钮或拖拽文件/文件夹到左上角区域。</li>
            <li>进度监控：左下角实时显示总进度、当前文件进度、页数进度。</li>
            <li>自动清理：识别成功的文件自动移出列表，失败的文件保留以便重试。</li>
        </ul>
    </li>
    <li><strong>结果查看</strong><br />默认输出到用户自定义目录或上级目录的 "dist" 文件夹中。</li>
</ul>

<h2>三、模型选择指南</h2>
<hr />
<p>不同模型各有千秋，建议根据文档类型选择：</p>

<h3>1. 硅基流动 (DeepSeek-OCR)</h3>
<ul>
    <li><strong>[参考地址]</strong>: <a href="https://siliconflow.cn/pricing" target="_blank">https://siliconflow.cn/pricing</a></li>
    <li><strong>[推荐场景]</strong>: 通用文档 / 代码识别 / 高性价比方案。</li>
    <li><strong>[ 优  点 ]</strong>: 免费额度高，推理速度快。</li>
    <li><strong>[ 缺  点 ]</strong>: 复杂版面还原度稍逊，精确度不高，中文古籍识别效果较差。</li>
</ul>

<h3>2. MinerU (官方 API)</h3>
<ul>
    <li><strong>[参考地址]</strong>: <a href="https://www.aipintai.com/mineru.html" target="_blank">https://www.aipintai.com/mineru.html</a></li>
    <li><strong>[推荐场景]</strong>: 学术图书论文 / 复杂 PDF 布局 / 导出 Markdown。</li>
    <li><strong>[ 优  点 ]</strong>: 免费，每天至少2000页额度；由 OpenDataLab 开发，专为 PDF 版面分析优化，公式与表格提取能力强。</li>
    <li><strong>[ 缺  点 ]</strong>: 中文古籍识别效果较差。文件有大小和页码限制：200M，600页。</li>
</ul>

<h3>3. 字节豆包 (Doubao)</h3>
<ul>
    <li><strong>[参考地址]</strong>: <a href="https://www.volcengine.com/docs/82379/1399009" target="_blank">https://www.volcengine.com/docs/82379/1399009</a></li>
    <li><strong>[推荐场景]</strong>: 中文文档 / 日常图片 / 快速识别。</li>
    <li><strong>[ 优  点 ]</strong>: 中文语义理解能力强，响应速度快，对常规古籍识别效果良好。</li>
    <li><strong>[ 缺  点 ]</strong>: 有敏感词监测。</li>
</ul>

<h3>4. 阿里通义千问 (Qwen)</h3>
<ul>
    <li><strong>[参考地址]</strong>: <a href="https://help.aliyun.com/zh/model-studio/what-is-model-studio" target="_blank">https://help.aliyun.com/zh/model-studio/what-is-model-studio</a></li>
    <li><strong>[推荐场景]</strong>: 综合首选 / 中文古籍 / 复杂排版还原。</li>
    <li><strong>[ 优  点 ]</strong>: 识别率顶尖，对古籍、手写体和竖排文字支持极好，版面还原度最高。</li>
    <li><strong>[ 缺  点 ]</strong>: 监测较严，会拒绝识别带有敏感词的整页内容。</li>
</ul>

<h3>5. 智谱 GLM (ZhipuAI)</h3>
<ul>
    <li><strong>[参考地址]</strong>: <a href="https://bigmodel.cn/" target="_blank">https://bigmodel.cn/</a></li>
    <li><strong>[推荐场景]</strong>: 政企办公 / 中文长文档处理。</li>
    <li><strong>[ 优  点 ]</strong>: 国产自研，API 兼容性好（OpenAI 接口风格），综合语义理解稳健；商用性价比高。</li>
    <li><strong>[ 缺  点 ]</strong>: 在极高分辨率图片的精细识别上，相较于 Qwen3-Max 略有差距。</li>
</ul>

<h3>6. Google Gemini</h3>
<ul>
    <li><strong>[参考地址]</strong>: <a href="https://ai.google.dev/gemini-api/docs/ai-studio-quickstart?hl=zh-cn" target="_blank">https://ai.google.dev/gemini-api/docs/ai-studio-quickstart?hl=zh-cn</a></li>
    <li><strong>[推荐场景]</strong>: 外文文档 / 多语言混合 / 极长文本。</li>
    <li><strong>[ 优  点 ]</strong>: 全球领先多模态能力，多语言支持极佳，支持超长上下文（整本书处理）。</li>
    <li><strong>[ 缺  点 ]</strong>: 在国内使用需要特殊的网络环境 (VPN)。</li>
</ul>

<hr />
<p><strong>[推荐配置]</strong></p>
<ul>
    <li>识别中文古籍：强烈推荐通义千问或豆包。</li>
    <li>识别普通文档：可以使用MinerU、 DeepSeek-OCR、或智谱 GLM。</li>
</ul>

<h2>四、API 申请与配置教程</h2>
<hr />
<p>本软件基于大模型 API，需要您自行申请 API Key。</p>

<h3>1. 硅基流动 (DeepSeek/VLM)</h3>
<ol>
    <li>访问：<a href="https://cloud.siliconflow.cn/" target="_blank">https://cloud.siliconflow.cn/</a></li>
    <li>注册账号（通常有免费额度）。</li>
    <li>生成 API Key 并填入软件。</li>
</ol>

<h3>2. MinerU（官方 API）</h3>
<ol>
    <li>访问：<a href="https://mineru.net/" target="_blank">https://mineru.net/</a> ，注册并登录。</li>
    <li>在官网申请 Token（API Token）。</li>
    <li>将 Token 填入软件的 API Key（或 Token）字段。</li>
    <li>如软件需要填写鉴权方式，请使用：Authorization: Bearer &lt;Token&gt;</li>
    <li>注意：如遇失败，请检查文件大小与页数是否超限（例如：200MB、600页等限制）。</li>
</ol>

<h3>3. 字节豆包</h3>
<ol>
    <li>访问：<a href="https://console.volcengine.com/ark/" target="_blank">https://console.volcengine.com/ark/</a></li>
    <li>创建推理接入点，获取 API Key。</li>
    <li>将 API Key 填入软件。</li>
</ol>

<h3>4. 阿里云通义千问 (Qwen)</h3>
<ol>
    <li>访问：<a href="https://bailian.console.aliyun.com/" target="_blank">https://bailian.console.aliyun.com/</a></li>
    <li>登录并开通“模型服务”。</li>
    <li>在“API-KEY 管理”中创建新的 API Key。</li>
    <li>复制 Key 填入软件，Base URL 默认即可。<br />默认地址：<a href="https://dashscope.aliyuncs.com/compatible-mode/v1" target="_blank">https://dashscope.aliyuncs.com/compatible-mode/v1</a></li>
</ol>

<h3>5. 智谱 GLM（ZhipuAI / GLM）</h3>
<ol>
    <li>访问：<a href="https://open.bigmodel.cn/" target="_blank">https://open.bigmodel.cn/</a> ，注册并获取 API Key。</li>
    <li>将 API Key 填入软件。</li>
    <li>Base URL（OpenAI 兼容方式）填写：<br /><a href="https://open.bigmodel.cn/api/paas/v4/" target="_blank">https://open.bigmodel.cn/api/paas/v4/</a></li>
    <li>说明：智谱提供 OpenAI API 兼容接口，迁移时通常只需替换 api_key 与 base_url。</li>
</ol>

<h3>6. Google Gemini</h3>
<ol>
    <li>访问 Google AI Studio: <a href="https://aistudio.google.com/" target="_blank">https://aistudio.google.com/</a>，在“API Keys”页面创建并管理 Gemini API Key。</li>
    <li>将 Key 填入软件（或按软件要求设置环境变量）。</li>
    <li>如需按 REST 方式调用，可参考接口形式：<br />https://generativelanguage.googleapis.com/v1beta/models/&lt;model&gt;:generateContent</li>
</ol>

<h2>五、常见问题 (FAQ)</h2>
<hr />
<p><strong>Q: 如何打开md文档？</strong><br />
右键 ->使用windows系统自带的记事本打开。<br />
或下载 Typora、MarkText、VS Code等打开。</p>

<p><strong>Q: 点击"开始处理"没有反应？</strong><br />
A: 请检查是否添加了文件，且 API Key 是否已正确设置并通过测试。<br />
文件上传和PDF拆分预处理，都需要一定的时间，所以大的PDF文档加载也需要一定的时间，请耐心等待。</p>

<p><strong>Q: 识别结果乱码或为空？</strong><br />
A: 可能是 PDF 每页图片过大导致模型拒识，尝试调低 DPI (如 150)。<br />
此外，有些模型，比如Qwen内嵌有敏感词检测，触发时，也会无法识别，这个和大预言模型有关，无法避免。</p>

<p><strong>Q: 文件名乱码？</strong><br />
A: 本软件全程支持 UTF-8，确保您的系统路径没有特殊偏僻字符。</p>

<h2>六、关于软件</h2>
<hr />
<ul>
    <li><strong>软件名称</strong>：HiOCR</li>
    <li><strong>版本</strong>：v2.0</li>
    <li><strong>开发</strong>：马光 （<a href="http://www.maguang.net" target="_blank">http://www.maguang.net</a>，<a href="http://www.haijiaoshi.com" target="_blank">www.haijiaoshi.com</a>）</li>
    <li><strong>开源地址</strong>：<a href="https://github.com/maguang/HiOCR" target="_blank">https://github.com/maguang/HiOCR</a></li>
    <li><strong>版本更新地址</strong>： <a href="https://pan.baidu.com/s/1WchKiuVp9kKkqj4yqSBg4Q?pwd=6666" target="_blank">百度网盘下载</a> 提取码: 6666</li>
    <li><strong>构建日期</strong>：2025-12-25</li>
</ul>

<h2>七、LICENSE 声明（非商业使用许可）</h2>
<hr />
<p>HiOCR 为免费公开软件，但默认不授予商业用途的使用许可。</p>
<p>本项目代码采用 PolyForm Noncommercial License 1.0.0（SPDX: PolyForm-Noncommercial-1.0.0）授权：</p>
<ol>
    <li>允许个人/学校/科研/公益等非商业目的：使用、修改与分发。</li>
    <li>禁止任何商业目的使用（包括但不限于：将本软件/源码集成到收费产品、以本软件提供收费服务、为商业项目交付/代跑/代处理等）。</li>
    <li>如需商业授权（个人免费 + 企业付费）：请联系作者取得书面商业许可。</li>
</ol>

<hr />
<p>Copyright © 2025. All Rights Reserved.</p>
