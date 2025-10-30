# 🔍 ScaNN – Tăng tốc tìm kiếm gần đúng (Approximate Nearest Neighbors)

## 🧠 Giới thiệu
Đề tài hiện thực và đánh giá thuật toán **ScaNN (Scalable Nearest Neighbors)** – giải pháp tìm kiếm vector gần đúng hiệu quả và có khả năng mở rộng, được phát triển bởi **Google Research**.  
ScaNN được ứng dụng trong Google Search, TensorFlow và các hệ thống gợi ý (recommendation systems) quy mô lớn.

Dự án này giúp sinh viên tiếp cận với các kỹ thuật hiện đại cho bài toán truy xuất vector hiệu suất cao.

---

## 🎯 Mục tiêu
- Nghiên cứu kiến trúc và nguyên lý hoạt động của ScaNN:  
  **Partitioning → Scoring → Reordering**
- So sánh hiệu năng giữa ScaNN và phương pháp **brute-force**.
- Đánh giá:
  - Thời gian truy vấn trung bình
  - Độ chính xác (recall@K)
  - Dung lượng bộ nhớ và khả năng mở rộng

---

## ⚙️ Công nghệ sử dụng
- **Ngôn ngữ:** Python  
- **Thư viện chính:**
  - [`scann`](https://github.com/google-research/google-research/tree/master/scann)
  - `numpy`
  - `matplotlib`
  - `scikit-learn`
  - `sentence-transformers` *(dùng để tạo vector từ văn bản)*

---

## ▶️ Chạy thử trực tiếp trên Google Colab
Bạn có thể mở và chạy project này trực tiếp tại đây:

👉 **[Mở trong Google Colab](https://colab.research.google.com/drive/1Acu0lcUkqRo1vTJ8JKcC8mFNkFFYBjFP)**

---

## 💻 Cài đặt thủ công (tuỳ chọn)
Nếu bạn muốn chạy trên máy cá nhân:

```bash
# Clone repository
git clone https://github.com/hoanganh1105/ScaNN.git
cd ScaNN

# Cài đặt các thư viện cần thiết
pip install scann numpy matplotlib scikit-learn sentence-transformers
```

---

## 🚀 Cách chạy
Chạy notebook chính:
```bash
jupyter notebook ScaNN.ipynb
```

Hoặc mở file `.ipynb` trong Google Colab và chạy từng cell.

---

## 📊 Kết quả đánh giá
Project cung cấp:
- **So sánh tốc độ** giữa ScaNN và brute-force.
- **Độ chính xác (recall@K)** của ScaNN.
- **Biểu đồ trực quan** về thời gian truy vấn, độ chính xác, và tốc độ.

Ví dụ minh họa:
```
K = 10
ScaNN Recall@K: 0.94
ScaNN Time (ms): 5.3
Brute-force Time (ms): 48.7
```

---

## 📁 Cấu trúc thư mục
```
ScaNN/
│
├── ScaNN.ipynb           # Notebook chính (Google Colab)
├── README.md             # Tài liệu hướng dẫn (bạn đang đọc)
└── data/ (tùy chọn)      # Dữ liệu vector nếu có
```

---

## 📹 Video minh họa
Video trình bày ý tưởng, cách chạy chương trình và kết quả:
> (Thêm link YouTube hoặc Google Drive tại đây khi có)

---

## 👨‍💻 Thành viên thực hiện
| Họ tên | Vai trò |
|--------|----------|
| **Huỳnh Hoàng Anh** | Nhóm trưởng – hiện thực ScaNN & đánh giá hiệu năng |
| **Ngô Trung Tín** | Phụ trách xử lý dữ liệu và trực quan hóa kết quả |
| **Huỳnh Tấn Tiến** | Phụ trách báo cáo, so sánh hiệu năng và video demo |

---

## 📚 Tài liệu tham khảo
- Google Research: [ScaNN: Efficient Vector Similarity Search](https://github.com/google-research/google-research/tree/master/scann)  
- Paper: *ScaNN: Efficient Vector Similarity Search at Scale* (Google AI Blog)  
- TensorFlow Similarity Documentation  

---

## 🏁 Giấy phép
Project chỉ sử dụng cho **mục đích học tập và nghiên cứu** trong học phần *Cấu trúc dữ liệu và Giải thuật – KSTN*.

---
