# Iris Flower Classification with MongoDB, Python & Machine Learning

Dự án được thực hiện trong môn **Nhập Môn Công Nghệ Thông Tin – HCMUS**, với mục tiêu xây dựng một pipeline gồm:
- Lưu trữ dữ liệu trên **MongoDB Atlas**
- Kết nối & xử lý dữ liệu bằng **PyMongo + Python**
- Áp dụng **Machine Learning (Scikit-learn)** để phân loại 3 giống hoa Iris

Dự án sử dụng quy trình **Scrum**, có phân chia vai trò rõ ràng, và được xây dựng bởi Nhóm 2.

---

## 1. Mục tiêu dự án
- Xây dựng hệ thống lưu trữ – xử lý dữ liệu với **MongoDB**
- Làm sạch dữ liệu & chuẩn hóa
- Train/test mô hình học máy (ML)
- Đánh giá độ chính xác và rút ra kết luận
- Tổng hợp quy trình thành một sản phẩm hoàn chỉnh

---

## 2. Công nghệ sử dụng
### **Backend & Database**
- MongoDB Atlas  
- MongoDB Compass  
- PyMongo  

### **Data Processing**
- Python  
- NumPy, Pandas

### **Machine Learning**
- Scikit-learn  
- SGDClassifier  
- MultinomialNB  

### **Development Tools**
- Jupyter Notebook  
- Visual Studio Code  

---

## 3. Quy trình thực hiện

### **Bước 1 – Khởi tạo hệ thống**
- Tạo Cluster trên MongoDB Atlas  
- Tạo Database & Collection  
- Import dataset vào DB  

### **Bước 2 – Kết nối Python ↔ MongoDB**
```python
from pymongo import MongoClient
client = MongoClient(connection_string)
db = client['iris_db']
collection = db['iris']
```

### **Bước 3 – Data Cleaning**
- Loại bỏ dòng lỗi
- Chuẩn hóa kiểu dữ liệu
- Chuyển sang DataFrame để xử lý

### **Bước 4 – Train/Test Split**
```python
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3)
```

### **Bước 5 – Train mô hình**
```python
from sklearn.linear_model import SGDClassifier
model = SGDClassifier()
model.fit(X_train, y_train)
```

### **Bước 6 – Đánh giá kết quả**
| Model         | Accuracy  |
| ------------- | --------- |
| SGDClassifier | **73.3%** |
| MultinomialNB | **53.3%** |

## 4. Vai trò của tôi (Nguyễn Minh Đạt – Scrum Master/Tester)
- Phân chia và theo dõi tiến độ nhóm
- Kiểm thử & đánh giá kết quả mô hình
- Tham gia xử lý dữ liệu, chạy mô hình ML
- Tổng hợp final, chuẩn bị báo cáo và phản biện
- Hỗ trợ các thành viên về công cụ kỹ thuật

## 5. Tài liệu đính kèm
Từ thư mục /docs:
- Project Plan (PDF)
- Reflective Report (PDF)
- Work Assignment (PDF)

## 6. Cách chạy dự án
### 1. Clone repo
```{bash}
git clone https://github.com/your-username/project-iris-mongodb-ml.git
cd project-iris-mongodb-ml
```
### 2. Cài đặt thư viện
```{bash}
pip install -r requirements.txt
```
### 3. Chạy notebook
```{bash}
jupyter notebook
```

## 7. Hướng phát triển
- Cải thiện phần trực quan hóa dữ liệu
- Thử nghiệm thêm các mô hình ML tiên tiến
- Tăng độ chính xác bằng GridSearchCV
- Tạo UI web dự đoán theo input người dùng

## 8. Tác giả
Nhóm 2 – Đại học Khoa học Tự Nhiên – HCMUS
- Nguyễn Minh Đạt
- Lê Nguyễn Quỳnh Anh
- Nguyễn Công Tiến Dũng
- Ngô Thị Mỹ Duyên
