
# 🦴 YOLOv8 Bone Tumor Segmentation

## 📦 I. Danh sách thư viện cần thiết

Dự án sử dụng các thư viện chính sau:

- `ultralytics` – Huấn luyện và inference YOLOv8
- `opencv-python` – Xử lý ảnh
- `albumentations` – Tăng cường dữ liệu
- `numpy` – Tính toán ma trận
- `matplotlib` – Vẽ biểu đồ, trực quan hóa ảnh
- `tqdm` – Hiển thị tiến trình huấn luyện
- `shapely` – Xử lý polygon annotation
- `glob`, `os`, `shutil`, `json` – Thư viện chuẩn Python

---

## ⚙️ II. Cài đặt môi trường và thư viện

### 1. Cài đặt bằng file `requirements.txt`
```bash
pip install -r requirements.txt
```

### 2. Hoặc cài đặt thủ công:
```bash
pip install ultralytics opencv-python albumentations numpy matplotlib tqdm shapely
```

---

## 🧠 III. Hướng dẫn huấn luyện lại mô hình YOLOv8

### 1. Mở tập tin notebook:
```bash
yolo8segmentbonetumor.ipynb
```

### 2. Cấu trúc thư mục dữ liệu (trong Google Colab hoặc local):
```
/content/BTXRD/
├── images/            # Ảnh X-quang
└── Annotations/       # File polygon (json)
```

### 3. Chạy lần lượt các ô (cell) trong notebook gồm các bước:

- ✅ Tiền xử lý dữ liệu
- 🔄 Chuyển đổi polygon → mask → YOLO format
- 📈 Tăng cường dữ liệu (Augmentation)
- 🔧 Thiết lập và huấn luyện mô hình YOLOv8 segmentation

---

## 📊 IV. Kết quả huấn luyện (Ví dụ minh họa)

Bạn có thể thêm hình minh họa kết quả segmentation sau khi huấn luyện tại đây:

### 📌 Hình minh họa:

| ![IMG000164](https://github.com/user-attachments/assets/3e7b18fb-386d-4688-9b95-949d67479142)
 |![IMG000234](https://github.com/user-attachments/assets/68fef4db-91e6-4c6c-b34e-7ac3f9db65ad)
 |


---

## 📝 Ghi chú

- Mô hình sử dụng YOLOv8 segmentation để phân đoạn vùng u xương trên ảnh X-quang.
- Dữ liệu annotation gốc ở dạng polygon, được xử lý để tạo ra mask và bounding box tương ứng.
- Notebook tương thích tốt với **Google Colab**.



---

## 🗂️ V. Tập dữ liệu BTXRD

### 📌 Giới thiệu:

- **BTXRD (Bone Tumor X-ray Dataset)** là một tập dữ liệu ảnh X-quang dùng cho bài toán phân đoạn vùng u xương.
- Dữ liệu bao gồm các ảnh chụp X-quang và các annotation dạng polygon tương ứng với vùng có khối u.

### 📁 Cấu trúc thư mục:

```
BTXRD/
├── images/            # Ảnh X-quang (.jpg/.png)
└── Annotations/       # Annotation dạng polygon (.json)
```

### 📌 Đặc điểm:

- Mỗi ảnh có một file `.json` chứa thông tin các vùng u dạng polygon.
- Annotation cần được chuyển đổi sang định dạng mask rồi sang YOLO format để huấn luyện mô hình segmentation.
- Có thể kết hợp với thư viện `shapely` và `albumentations` để xử lý và augment dữ liệu hiệu quả.

### ⚠️ Lưu ý:

- Ảnh cần resize về kích thước phù hợp (thường là 640x640 hoặc 512x512).
- Các file annotation phải được đồng bộ chính xác với tên file ảnh.

---

