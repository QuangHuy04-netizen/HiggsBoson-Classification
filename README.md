# Higgs Boson Classification – Tái hiện & Cải tiến bài báo IRJET 2021

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/HiggsBoson-Classification/blob/main/HiggsBoson_IRJET_Full.ipynb)
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/YOUR_USERNAME/HiggsBoson-Classification/HEAD)

##  Tổng quan

Dự án này tái hiện và cải tiến bài báo *"Higgs Boson Discovery using Machine Learning"* (Vinay Chaukate et al., IRJET Vol.08 Issue 12, 2021).  
Nhiệm vụ chính: **phân loại sự kiện `signal (s)` – tín hiệu hạt Higgs – và `background (b)`** dựa trên các đặc trưng mô phỏng từ máy gia tốc hạt.

##  Mục tiêu

- **Phần A** – Tái hiện đúng kết quả bài báo gốc:  
  - Dữ liệu 8 features, 250.000 events.  
  - Các mô hình: **Logistic Regression**, **Decision Tree**, **LSTM**.
- **Phần B** – Cải tiến mở rộng:  
  - Nâng cấp lên 28 features, 300.000 events.  
  - Sử dụng **PySpark**, **Random Forest**, **GBT**, **XGBoost**, **DNN 5‑layer** với GPU.

##  Nguồn dữ liệu

Bộ dữ liệu được lấy từ:
- **UCI Machine Learning Repository – HIGGS Dataset**  
  [https://archive.ics.uci.edu/ml/datasets/HIGGS](https://archive.ics.uci.edu/ml/datasets/HIGGS)  
  (11 triệu sự kiện, 28 đặc trưng vật lý hạt)
- **Kaggle Higgs Boson Machine Learning Challenge 2014**  
  [https://www.kaggle.com/c/higgs-boson](https://www.kaggle.com/c/higgs-boson)  
  (250.000 mẫu huấn luyện, 550.000 mẫu kiểm tra)

> *Lưu ý:* Dữ liệu thô không được đưa lên GitHub vì dung lượng lớn. Bạn có thể tải trực tiếp từ liên kết trên.

##  Các mô hình đã triển khai

| Phần | Mô hình | Accuracy (tái hiện) | Accuracy (cải thiện) |
|------|---------|--------------------|----------------------|
| A    | Logistic Regression | 85.4% | – |
| A    | Decision Tree       | 83.6% | – |
| A    | LSTM                | 89.3% | – |
| B    | Random Forest       | –     | 89.1% |
| B    | GBT (PySpark)       | –     | 91.1% |
| B    | XGBoost (GPU)       | –     | 92.2% |
| B    | DNN 5‑layer (CUDA)  | –     | 92.1% |
