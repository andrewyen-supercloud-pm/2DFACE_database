# 2D Face Database

一個用於管理和查詢 2D 人臉圖像的資料庫系統。

## 功能特點

- 人臉圖像存儲管理
- 人臉搜索功能
- 資料庫統計信息
- 可擴展的架構設計

## 安裝

1. 克隆此專案：
```bash
git clone <repository-url>
cd 2DFACE_database
```

2. 安裝依賴：
```bash
pip install -r requirements.txt
```

## 使用方法

運行主程式：
```bash
python main.py
```

## 專案結構

```
2DFACE_database/
├── main.py           # 主程式入口
├── requirements.txt  # Python 依賴套件
├── data/            # 人臉資料存儲目錄（自動創建）
└── README.md        # 專案說明
```

## 開發計劃

- [ ] 實現人臉圖像添加功能
- [ ] 實現人臉搜索算法
- [ ] 添加人臉特徵提取
- [ ] 實現資料庫持久化
- [ ] 添加 Web 界面

## 授權

MIT License