## 1️ Vấn đề

VietFast (sản xuất đồ chơi) liên tục bị **gián đoạn sản xuất (Downtime)** trong giai đoạn 2013–2014 do nguyên vật liệu lỗi (Defect) từ nhà cung cấp. Downtime dao động rất mạnh — từ **2,138 phút** đến **12,332 phút/tháng** — gây giảm năng suất, tăng chi phí vận hành, ảnh hưởng tiến độ giao hàng. Công ty cần tìm ra **nguyên nhân gốc rễ** để có giải pháp xử lý đúng chỗ.


## 2️ Phương pháp sử dụng

- Thu thập & tổng hợp dữ liệu Defect và Downtime theo **tháng, nhà cung cấp, nhà máy, mã lỗi**.
- Đối chiếu tương quan giữa **số lượng lỗi** và **thời gian dừng máy** → phân tách 2 nhóm nguyên nhân khác bản chất:
  - Lỗi số lượng lớn (đại trà)
  - Lỗi hiếm nhưng nghiêm trọng (chí mạng)
- Trực quan hóa bằng Power BI: biểu đồ xu hướng, donut/treemap theo khu vực, biểu đồ cột & bong bóng theo mã lỗi, bảng xếp hạng nhà cung cấp.
- Tính chỉ số **MTTR** (Mean Time To Repair – thời gian sửa chữa trung bình) theo từng nhà máy để đánh giá tốc độ xử lý sự cố.


## 3️ Số liệu tính ra Insight

| Nhóm lỗi | Số lượng lỗi | Downtime | Vendor liên quan |
|---|---|---|---|
| Lỗi đại trà (3 tháng đỉnh điểm) | ~12 triệu | 28,198 phút | 177 |
| Lỗi chí mạng | ~2 triệu | 11,000 phút | 93 |
| **Tổng cộng** | **~14 triệu** | **~39,200 phút (~653 giờ)** | — |

**Insight rút ra từ số liệu:**
- **Illinois** chiếm **53.73%** downtime nhóm lỗi đại trà, nặng nhất tại **Plant 22 – Skokie**.
- **Indiana, Illinois, Michigan** cộng lại chiếm **71%** downtime nhóm lỗi chí mạng, nặng nhất tại **Plant 16** (2,250 phút).
- **Vendor 1 + Vendor 2** chiếm gần **1/4 tổng downtime** toàn hệ thống — là 2 nguồn rủi ro lớn nhất ở cả 2 nhóm lỗi.
- Một nhóm Vendor và 2 bang (**IA**, **WI**) có downtime gần bằng 0 → đang vận hành cực kỳ hiệu quả, có thể dùng làm chuẩn tham chiếu.


## 4️ Kết luận hỗ trợ business

- **Rủi ro tập trung, không dàn trải:** Chỉ 2 Vendor và 2 khu vực (Illinois, Indiana) gây ra phần lớn thiệt hại → xử lý đúng 2 điểm này sẽ cắt giảm ngay hơn 50% downtime toàn hệ thống.
- **Cần chiến lược khác nhau cho 2 loại lỗi:** lỗi đại trà cần cải tiến tốc độ xử lý (quy trình sục rửa, kiểm tra nhanh); lỗi chí mạng cần quy trình xử lý chuyên sâu và dự phòng vật tư.
- **Hướng hành động đề xuất:**
  - Đàm phán lại/siết kiểm soát chất lượng với Vendor 1, Vendor 2; thay thế dần bằng nhóm nhà cung cấp ổn định.
  - Tăng cường nhân sự kỹ thuật và dự phòng vật tư tại Plant 22 (Illinois) và Plant 16 (Indiana).
  - Nhân rộng mô hình vận hành xuất sắc (nhà máy/kho tại IA, WI, nhóm Plant có MTTR tốt) sang khu vực yếu.

---
