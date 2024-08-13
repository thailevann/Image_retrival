# Image Retrieval

## Giới thiệu
Dự án này xây dựng một chương trình có khả năng tìm kiếm và hiển thị các hình ảnh tương tự từ một bộ dữ liệu khi đưa vào một hình ảnh truy vấn. Chương trình áp dụng các phương pháp đo lường khác nhau để so sánh sự tương tự giữa hình ảnh truy vấn và các hình ảnh trong bộ dữ liệu, từ đó trả về danh sách các hình ảnh có độ tương đồng cao nhất.

## Yêu cầu
- **Input:** 
  - Hình ảnh truy vấn (Query Image).
  - Bộ dữ liệu hình ảnh (Images Library).
- **Output:** 
  - Danh sách các hình ảnh có độ tương tự cao với hình ảnh truy vấn.

## Phương pháp
Chương trình được triển khai với hai cách tiếp cận chính:

### 1. `image_retrival_basic.py`
- Thực hiện truy vấn sử dụng các độ đo:
  - L1 (Manhattan Distance)
  - L2 (Euclidean Distance)
  - Cosine Similarity
  - Hệ số tương quan Pearson (Correlation Coefficient)
- Không sử dụng vector embedding, mà chỉ dựa trên các đặc trưng cơ bản của hình ảnh.

### 2. `image_retrival_vector_embedding.py`
- Kết hợp các độ đo trên với vector embedding:
  - Sử dụng mô hình CLIP để tạo ra các vector embedding từ hình ảnh.
  - Truy vấn dựa trên các độ đo L1, L2, Cosine Similarity, và Correlation Coefficient.
- **Thử nghiệm nâng cao:**
  - Sử dụng cơ sở dữ liệu vector để quản lý các vector embedding, giúp tối ưu hóa quá trình truy vấn.
  - Dùng công cụ Chroma để cải thiện tốc độ trả kết quả, cho phép truy vấn nhanh hơn mà vẫn đảm bảo độ chính xác tương tự.

## Kết quả so sánh
Dưới đây là kết quả so sánh giữa các phương pháp:

![Comparison](https://github.com/user-attachments/assets/3b471501-a214-4bc1-81cd-12989c75468d)

![Result](https://github.com/user-attachments/assets/0dc82a50-456a-49d2-8ee2-f958b6de64d7)

![Performance](https://github.com/user-attachments/assets/c7758ff7-6159-460e-a898-da0b180684cd)

![Optimization](https://github.com/user-attachments/assets/b4e1e65a-678f-48ff-88d1-74284f36ae02)
