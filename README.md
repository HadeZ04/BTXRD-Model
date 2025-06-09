=========================================
README - Huấn luyện phân đoạn u xương bằng YOLOv8
=========================================

I. Danh sách thư viện cần thiết
-------------------------------
Dự án sử dụng các thư viện chính sau:

- ultralytics
- opencv-python
- albumentations
- numpy
- matplotlib
- tqdm
- shapely
- glob
- os, shutil, json (thư viện chuẩn của Python)

II. Hướng dẫn cài đặt thư viện và thiết lập môi trường
-------------------------------------------------------

 Cài đặt các thư viện cần thiết:

    pip install -r requirements.txt

Nếu không có file `requirements.txt`, có thể cài đặt thủ công:

    pip install ultralytics opencv-python albumentations numpy matplotlib tqdm shapely

III. Hướng dẫn chạy lại quá trình huấn luyện
--------------------------------------------

1. Mở tập tin notebook:

    yolo8segmentbonetumor.ipynb

2. Đảm bảo cấu trúc thư mục dữ liệu đúng như sau:

    /content/BTXRD/images  
    /content/BTXRD/Annotations

3. Chạy tuần tự các ô (cell) trong notebook. Quá trình huấn luyện bao gồm:

    - Tiền xử lý dữ liệu
    - Chuyển polygon sang mask + định dạng YOLO
    - Tăng cường dữ liệu (augmentation)
    - Thiết lập và huấn luyện mô hình YOLOv8


