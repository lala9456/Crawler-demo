# Crawler-demo
## Azure Document Intelligence
### 1. 執行 Notebook
在 Jupyter Notebook 中運行 `demo.ipynb`，該 Notebook 會：
1. 讀取 PDF 檔案 (`TSMC_4Q24ManagementReport.pdf`)
2. 呼叫 Azure Document Intelligence API 解析文件
3. 輸出文件的版面配置與文字內容
4. 將表格整理成pandas的dataframe

### 2. 修改文件路徑
若要分析其他 PDF，請修改程式碼中的 `path_to_sample_documents` 變數：
```python
path_to_sample_documents = "your_pdf_file.pdf"
```

## 主要功能
- 解析 PDF 資訊（頁面尺寸、單詞位置等）
- 提取文本與置信度分數
- 非結構化資料轉成結構化

## GPT 抓取非結構化數據並格式化輸出 (以圖片為例)
### 功能
- 透過 **Azure OpenAI API** 分析圖片內容
- 解析 **財務報告** 或 **其他結構化數據**
- 自動提取關鍵數據，並以 **BaseModel** 定義的結構化格式輸出
- 表格較複雜GPT 4O容易看錯

## GPT 抓取非結構化數據並格式化輸出 (以 Markdown 為例)
### 功能
- 讀取 **Markdown 檔案**，提取重要內容
- 使用 **GPT 解析財務報告或特定章節**
- 將資訊結構化，方便存入資料庫
- 可以先用Azure Document Intelligence 轉成markdown再給LLM閱讀，正確率較高


## 參考
- [Azure Document Intelligence 官方文件](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/)
- [Azure Document Intelligence python SDK](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/quickstarts/get-started-sdks-rest-api?view=doc-intel-4.0.0&pivots=programming-language-python)
- [範例資料來源(TSMC官網)](https://investor.tsmc.com/chinese/quarterly-results/2024/q4)
- [Document Intelligence價格](https://azure.microsoft.com/en-us/pricing/details/ai-document-intelligence/)