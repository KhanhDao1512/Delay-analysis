# 🚚 Supply Chain Delay Prediction System

Dự án Machine Learning dự đoán nguy cơ giao hàng trễ trong chuỗi cung ứng bằng cách kết hợp:
* Phân tích dữ liệu (EDA)
* Feature Engineering
* Ensemble Learning

---

## 📌 Tổng Quan
Mục tiêu của dự án là xây dựng hệ thống hỗ trợ phát hiện các đơn hàng có rủi ro giao trễ dựa trên:
* Nhà cung cấp
* Lead time
* Phương thức vận chuyển
* Metadata vận hành
* Interaction giữa nhiều yếu tố

Dự án tập trung vào:
* Tư duy nghiệp vụ thực tế
* Chống data leakage
* Xử lý dữ liệu mất cân bằng
* Temporal validation
* Tối ưu hóa cho vận hành kho bãi

---

## 📂 Cấu Trúc Dự Án
* `01_Preprocess.ipynb`
* `02_Feature_Engineering.ipynb`
* `03_Modeling.ipynb`

---

## 📊 Exploratory Data Analysis (EDA)
Trong quá trình EDA, dự án tập trung phân tích:
* Class imbalance của dữ liệu giao trễ
* Outlier của lead time dựa trên domain knowledge
* High-cardinality categorical features
* Interaction giữa supplier, ship mode và lead time

Từ đó đưa ra các quyết định xử lý dữ liệu phù hợp thay vì chỉ áp dụng các kỹ thuật thống kê thông thường.

---

## ⚙️ Feature Engineering
Pipeline feature engineering bao gồm:
* Time-based features
* Lead time engineering & capping
* Rare entity grouping
* Frequency encoding
* Feature crossing

Toàn bộ pipeline tuân thủ nguyên tắc: **Fit trên train → transform trên test** nhằm tránh data leakage.

---

## 🤖 Modeling
Dự án sử dụng kiến trúc Ensemble gồm:
* LightGBM
* CatBoost

Kết hợp với:
* Weighted soft voting
* Threshold sweeping
* Temporal validation
* Incremental learning experiments

Mục đích nhằm mô phỏng sát hơn bài toán vận hành thực tế.

---

## 🚀 Hướng Phát Triển
Một số hướng mở rộng trong tương lai:
* SHAP Explainability
* MLflow Tracking
* Hyperparameter Tuning
* Real-time Inference API
* Drift Monitoring

---

## 👨‍💻 Tác Giả
* **Khanh Dao**
* **MSSV:** 24520778
