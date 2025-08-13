# Footstep Sound Classification with CNN

本專案是一個使用 **TensorFlow** 實作卷積神經網路 (CNN) 來分類腳步聲的小型專題。  
模型可辨識 **兩位不同人 ("瑋" 和 "媽")** 在 **三種不同鞋類/腳步狀況** 下的聲音類別。  

## 專案內容

- **資料增強程式碼**：包含對音檔進行增強處理的程式（如隨機變化音高、速度、加入雜訊等）。
- **模型實作程式碼**：使用 TensorFlow 撰寫 CNN 模型，進行腳步聲分類。
- **音檔資料集**：
  - 每位人物在三種不同穿著/狀態下的 `.wav` 檔。
  - 資料增強後，每種類別各 **300 個音檔**。
  - 檔案以資料夾名稱區分類別。
  - `ALL` 資料夾整合了 **共 1800 個音檔**。
- **訓練完成的模型**：
  - `Model.h5` — 已訓練完成的 CNN 模型，可直接載入進行預測。
- **虛擬環境需求**：
  - `requirements.txt` — Python 環境套件需求（pip）。
  - `audioCNN.yml` — Conda 虛擬環境設定檔（適用於 Anaconda / Miniconda）。
- **資料集分割**：
  - `train_data` — 預設訓練資料夾。
  - `val_data` — 預設驗證資料夾。
  - `test_data` — 預設測試資料夾。  
  需要注意的是**如果想自行重新分類請clone下來後刪除這三個資料夾再重新運行一次模型實作程式碼**

## 環境建置

### 使用 pip(先自行創建虛擬環境再進行)
```bash
pip install -r requirements.txt
```

### 使用 Conda
```bash
conda env create -f audioCNN.yml
conda activate audioCNN
```

## 備註
- CNN 模型使用 TensorFlow 實作。
- 音檔格式為 `.wav`，採用單聲道與固定取樣率處理。
- 資料夾名稱即為分類標籤(`襪子`資料夾為存放瑋穿著襪子之腳步聲之音檔)。
