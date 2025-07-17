# Agentic AI - OpenManus

有留意開AI发展的應該都知道, 最新的AI技術發展已經由「傳統RAG」轉向多模態嘅Agentic AI同MCP工具。 對我嚟講，用Agents去從多個來源收集實時數據，比起用一個幾年前訓練好、只靠歷史數據嘅大型語言模型，更加合理同有意義。

其中由中國人開發的Manus是其中一個比較受人关注的項目。

今天我分享一個open source 项目, 其功能類似Manus, 可以本地部署, 安裝簡單, 對硬件的要求不高, 我都是安裝在工作用的普通電腦上, 運行暢順。

#### 要安裝, 首先在github clone下source code "OpenManus".
<code>git clone https://github.com/FoundationAgents/OpenManus.git
cd OpenManus</code>

#### Install須要元件
<code>pip install -r requirements.txt</code>

#### 安裝Playwright
Agentic AI用它來在Internet 搜尋資料
<code>playwright install</code>

#### 設定LLM
<code>cp config/config.example.toml config/config.toml</code>

編輯 config/config.toml，加入你的 API 金鑰並自訂設定。

#### 安裝完成。最後就是試用了。
<code>python main.py</code>

我嘗試叫openmanus搜集関于香港個人资料私隱條例, 並summarize, 最後以HTML形式保存。

以下錄影可見"它"動用Chrome瀏覽器在網上搜集資料, 並以HTML保存結果。
![OpenManus locally](https://github.com/justinlaw360/agentic-openmanus/blob/main/openmanus_mcp.gif)

當然Agentic AI最優勝的地方是可以建立自己的Tools,  並以MCP協定加以調用。有動手能力的, 可以試下。
