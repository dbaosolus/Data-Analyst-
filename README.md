# 🍎 Fruit Journey Sales Analysis

## 📌 Project Overview

Dự án phân tích dữ liệu bán hàng **Fruit Journey** nhằm khám phá các xu hướng kinh doanh, hành vi khách hàng và hiệu quả vận hành. Thông qua Exploratory Data Analysis (EDA) và phân tích dữ liệu, dự án cung cấp các insight hỗ trợ doanh nghiệp trong việc ra quyết định về tồn kho, chiến lược giá, phân bổ nguồn lực và chăm sóc khách hàng.

---

## 🎯 Objectives

### 1. Time Series & Inventory Planning
- Phân tích xu hướng doanh thu và sản lượng theo thời gian.
- Phát hiện tính mùa vụ (Seasonality).
- Hỗ trợ lập kế hoạch tồn kho và dự báo nhu cầu.

### 2. Product & Pricing Strategy
- Xác định các sản phẩm mang lại doanh thu cao nhất.
- Phân loại sản phẩm theo doanh thu và số lượng bán.
- Đánh giá tác động của chính sách chiết khấu (Discount) đến doanh số.

### 3. Country & Logistical Performance
- Xác định thị trường có nhiều khách hàng nhất.
- Phân tích doanh thu theo quốc gia.
- Đánh giá hiệu quả kinh doanh của từng thị trường.

### 4. Logistics Efficiency
- Phân tích mối quan hệ giữa chi phí vận chuyển và số lượng hàng bán.
- Đánh giá hiệu quả logistics theo từng kênh bán hàng.

### 5. Customer Segmentation
- Xây dựng mô hình RFM (Recency - Frequency - Monetary).
- Phân nhóm khách hàng:
  - VIP Customers
  - Loyal Customers
  - New Customers
  - At Risk Customers
  - Lost Customers

---

# 📂 Dataset

Dataset sử dụng là **FruitJourney.csv**, bao gồm hơn **10,000 giao dịch bán hàng**.

### Order Information
- InvoiceNo
- InvoiceDate
- Quantity
- UnitPrice
- Discount
- Revenue

### Product Information
- StockCode
- Description
- Category

### Customer & Logistics Information
- CustomerID
- Country
- SalesChannel
- ShippingCost
- WarehouseLocation

---

# 🧹 Data Preprocessing

Các bước tiền xử lý dữ liệu gồm:

### 1. Remove Invalid Records
- Loại bỏ các giao dịch có Quantity < 0.
- Xóa các dòng thiếu Description.

### 2. Missing Value Handling
- Median Imputation:
  - Discount
  - ShippingCost
- Mode Imputation:
  - Category
  - OrderPriority

### 3. Outlier Treatment
- Áp dụng phương pháp IQR.
- Capping giá trị ngoại lai cho Discount.

### 4. Data Cleaning
- Loại bỏ dữ liệu trùng lặp.
- Xóa cột ReturnStatus.

### 5. Feature Engineering
Tạo thêm các biến:

- Revenue = Quantity × UnitPrice
- Year
- Quarter
- Month
- Date
- Time
- Year_Month

---

# 📊 Analysis

Dự án thực hiện các phân tích:

- Sales Trend Analysis
- Monthly Revenue Analysis
- Seasonal Pattern Detection
- Product Performance
- Category Analysis
- Discount Impact Analysis
- Country Performance
- Customer Distribution
- Shipping Cost Analysis
- Correlation Analysis
- RFM Customer Segmentation

---

# 🛠 Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- Scikit-learn
- Jupyter Notebook

---

# 📁 Project Structure

```
Fruit-Journey-Sales-Analysis/
│
├── data/
│   └── FruitJourney.csv
│
├── notebooks/
│   └── FruitJourney_EDA.ipynb
│
├── images/
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

# 🚀 How to Run

Clone repository

```bash
git clone https://github.com/<your-username>/Fruit-Journey-Sales-Analysis.git
```

Di chuyển vào thư mục dự án

```bash
cd Fruit-Journey-Sales-Analysis
```

Cài đặt thư viện

```bash
pip install -r requirements.txt
```

Khởi động Jupyter Notebook

```bash
jupyter notebook
```

Mở notebook

```
notebooks/FruitJourney_EDA.ipynb
```

---

# 📈 Expected Outcomes

- Hiểu rõ xu hướng doanh thu theo thời gian.
- Xác định sản phẩm và thị trường trọng điểm.
- Đánh giá hiệu quả của chính sách giảm giá.
- Phân tích hiệu quả logistics.
- Phân nhóm khách hàng bằng mô hình RFM.
- Đề xuất các quyết định kinh doanh dựa trên dữ liệu.

---

# 👤 Author

**Dinh Bao**

GitHub: https://github.com/dbaosolus
