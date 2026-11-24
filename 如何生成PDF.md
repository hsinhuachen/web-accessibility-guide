# 如何生成無亂碼的PDF文件

## 方法一：使用瀏覽器列印（推薦）✨

這是最簡單且保證中文完美顯示的方法：

### 步驟：

1. **開啟HTML文件**
   - 雙擊 `文化帶路網站無障礙標章送審教學.html` 檔案
   - 或在瀏覽器中按 Ctrl+O（Mac: Cmd+O）選擇該檔案

2. **等待字體載入**
   - 等待 2-3 秒讓 Google Fonts 中文字體完全載入

3. **開啟列印對話框**
   - Windows/Linux: 按 `Ctrl + P`
   - Mac: 按 `Cmd + P`

4. **設定列印選項**
   - 目的地：選擇「**另存為PDF**」或「**儲存成 PDF**」
   - 版面配置：縱向
   - 邊界：預設
   - 選項：✅ 勾選「背景圖形」

5. **儲存PDF**
   - 點選「儲存」按鈕
   - 選擇儲存位置
   - 完成！

### 推薦瀏覽器：
- ✅ **Google Chrome**（推薦）
- ✅ **Microsoft Edge**
- ✅ **Firefox**
- ⚠️ Safari（可能需要調整設定）

---

## 方法二：使用自動化腳本

如果需要經常生成PDF，可以使用自動化腳本：

### 安裝依賴：

```bash
# 建立虛擬環境
python3 -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# 安裝 Playwright
pip install playwright

# 安裝瀏覽器
playwright install chromium
```

### 執行腳本：

```bash
python3 generate_pdf.py
```

---

## 預期結果

✅ 完美的中文字體顯示（使用 Noto Sans TC）
✅ 完整的排版和樣式
✅ 所有顏色和背景
✅ 適合列印的格式

---

## 故障排除

### 問題：中文字體看起來很細或不清楚
**解決方法**：確保在列印設定中勾選「背景圖形」選項

### 問題：排版跑掉
**解決方法**：等待網頁完全載入後（約 3 秒）再列印

### 問題：檔案太大
**解決方法**：在列印設定中可以調整品質，選擇「標準」品質即可

---

## 注意事項

- HTML 文件已內建 Google Fonts 中文字體，不需要額外安裝字體
- 生成 PDF 時需要網路連線（用於載入 Google Fonts）
- 建議使用 Chrome 或 Edge 瀏覽器以獲得最佳效果
