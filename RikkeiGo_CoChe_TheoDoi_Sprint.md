# Cơ chế theo dõi kế hoạch Sprint cho đội RikkeiGo

**Người thiết kế:** Lan (Scrum Master)  |  **Người dùng cơ chế:** Đức (Product Owner) và Developers

## Mục tiêu và nguyên tắc

Cơ chế này giải quyết ba vấn đề lặp lại của đội:

| Vấn đề | Giải quyết bằng |
|---|---|
| Đến ngày cuối Sprint mới biết Sprint Goal không đạt | Thành phần 2 và 3 (theo dõi hằng ngày và điểm kiểm tra giữa Sprint) |
| Mỗi buổi Sprint Planning lại tranh luận nên nhận bao nhiêu SP | Thành phần 1 (cách dự báo cố định, có số liệu) |
| Quản lý muốn dùng Velocity để xếp hạng đội | Thành phần 4 và nguyên tắc dưới đây |

**Nguyên tắc áp dụng cho cả cơ chế:**
- **Không quy đổi SP sang giờ.** SP đo độ lớn tương đối, Capacity tính bằng giờ chỉ để tham khảo.
- **Không dùng Velocity hay Burndown làm KPI** hoặc để so sánh các đội. Số liệu là để đội tự dự báo và tự điều chỉnh.
- **Sprint Goal là điểm tham chiếu** khi quyết định giữ, đổi hay bỏ bớt phạm vi trong Sprint.
- Chỉ **PBI đạt 100% Definition of Done** mới được tính là Done (cho Velocity và cho Burndown).

---

## Phần 1. Thiết kế cơ chế (4 thành phần)

```
Planning (1)  →  Mỗi ngày (2)  →  Giữa Sprint (3)  →  Cuối Sprint (4)  →  dữ liệu cho Planning tiếp theo
```

### Thành phần 1: Bảng dự báo phạm vi Sprint

| Mục | Nội dung |
|---|---|
| **Dữ liệu đầu vào** | Velocity các Sprint gần nhất (hiện tại 18, 20, 19, 15, 13), Capacity thực tế của Sprint tới (giờ), danh sách PBI đã đủ rõ theo thứ tự PO, Sprint Goal đề xuất |
| **Ai cập nhật** | Lan chuẩn bị số liệu. Developers dự báo và chốt. Đức đưa Sprint Goal và thứ tự ưu tiên |
| **Khi nào** | Trước và trong mỗi buổi Sprint Planning |
| **Giúp quyết định** | Nhận **bao nhiêu SP và những PBI nào**, mà không phải tranh luận lại từ đầu |

**Cách tính cố định (4 bước):**
1. Tính **Average Velocity** và **Velocity Range** (hiện tại: trung bình 17 SP, khoảng 13 đến 20; trung bình 3 Sprint gần nhất khoảng 15,7).
2. So **Capacity** Sprint tới với Sprint trước. Nếu giảm thì tham khảo mức giảm, nhưng **không nhân máy móc**.
3. Chọn một **khoảng dự báo** (không chỉ một con số), thường nghiêng về phía thấp nếu Capacity giảm.
4. Chọn **PBI đã đủ rõ và phục vụ Sprint Goal** vào khoảng đó, kèm 1 PBI nhỏ dự phòng. Developers chốt cuối cùng.

### Thành phần 2: Burndown hằng ngày

| Mục | Nội dung |
|---|---|
| **Dữ liệu đầu vào** | Số SP còn lại cuối mỗi ngày (**chỉ trừ PBI đã Done theo DoD**), đường lý tưởng, danh sách vướng mắc (impediment) |
| **Ai cập nhật** | **Developers** cập nhật khi có PBI Done. **Lan** xem biểu đồ và nêu câu hỏi |
| **Khi nào** | Mỗi ngày, trước hoặc trong Daily Scrum (tối đa 15 phút) |
| **Giúp quyết định** | Có nguy cơ không đạt Sprint Goal không, và cần **gỡ vướng mắc nào** ngay |

**Tín hiệu cảnh báo:**

| Hình dạng | Ý nghĩa | Phản ứng |
|---|---|---|
| Thực tế **trên** đường lý tưởng | Đang trễ | Hỏi nguyên nhân, cân nhắc giảm phạm vi |
| **Nằm ngang từ 2 ngày liên tiếp** | Có thể đang tắc | Lan xử lý ngay (xem tình huống 1) |
| Thực tế **dưới** đường lý tưởng | Đang vượt tiến độ | Có thể thêm PBI nhỏ từ Backlog (sau khi hỏi Đức) |

### Thành phần 3: Điểm kiểm tra Sprint Goal giữa Sprint

| Mục | Nội dung |
|---|---|
| **Dữ liệu đầu vào** | Burndown đến ngày 5, PBI nào đã Done, PBI nào **thiết yếu cho Sprint Goal** và PBI nào chỉ là phần thêm |
| **Ai cập nhật** | **Developers** đánh giá khả năng đạt Goal. **Đức** quyết định về phạm vi. **Lan** điều phối |
| **Khi nào** | **Ngày 5** của Sprint 10 ngày, tận dụng buổi Daily Scrum (không thêm cuộc họp mới) |
| **Giúp quyết định** | **Giữ, đổi hay bỏ bớt phạm vi** dựa trên Sprint Goal |

**Cách quyết định theo Sprint Goal:**
- **Giữ** PBI thiết yếu cho Goal.
- **Bỏ bớt** PBI không phục vụ Goal (ưu tiên thấp nhất bỏ trước) để bảo vệ Goal.
- **Đổi** một PBI lớn bằng phần nhỏ hơn vẫn phục vụ Goal, nếu hai bên thống nhất.
- **Sprint Goal giữ nguyên**, chỉ phạm vi được thương lượng.

### Thành phần 4: Sổ Velocity, Capacity qua các Sprint

| Mục | Nội dung |
|---|---|
| **Dữ liệu đầu vào** | Velocity (SP Done), Capacity (giờ), **Sprint Goal đạt hay không**, ghi chú nguyên nhân (người mới, nghỉ phép, vướng mắc kéo dài...) |
| **Ai cập nhật** | **Lan** nhập số liệu. **Developers** bổ sung ghi chú nguyên nhân |
| **Khi nào** | Cuối mỗi Sprint, sau Sprint Review và trong Retrospective |
| **Giúp quyết định** | Dự báo Sprint sau có căn cứ, và **cải tiến cách làm** của đội |

**Cách dùng:** mỗi dòng là một Sprint với các cột Velocity, Capacity, Sprint Goal đạt hay không, ghi chú. Sổ này chỉ dành cho **chính đội** để dự báo và cải tiến, không dùng để báo cáo xếp hạng.

---

## Phần 2. Xử lý tình huống

### Tình huống 1: Ngày 4 đến 6 Burndown nằm ngang dù Developers vẫn làm đủ giờ

**Phát hiện:** thành phần 2 cảnh báo khi Burndown không giảm **2 ngày liên tiếp**, và thành phần 3 kiểm tra lại ở ngày 5. **Phản ứng:** Lan không yêu cầu làm thêm giờ mà hỏi nguyên nhân ngay trong Daily Scrum, vì Burndown chỉ trừ PBI đã Done nên "làm đủ giờ mà không giảm" thường có nghĩa là nhiều PBI đang làm dở cùng lúc, PBI quá lớn, bị chặn hoặc đang chờ review. Sau đó đội gỡ vướng mắc, tập trung hoàn thành từng PBI một (chia nhỏ phần lớn để có phần Done sớm), và nếu Goal đang bị đe dọa thì Developers và Đức thống nhất bỏ bớt PBI ưu tiên thấp, giữ nguyên Sprint Goal.

### Tình huống 2: Sprint tới 2 trong 4 Developers nghỉ mỗi người 3 ngày, Capacity giảm khoảng 15%

**Kiểm tra số:** Capacity 4 người × 10 ngày = 40 người-ngày, trừ 6 ngày nghỉ còn 34, tức 34/40 = 85%, đúng giảm khoảng 15%.

**Phát hiện:** Lan tính Capacity ở bước 2 của thành phần 1 **trước buổi Planning** và so với Sprint trước. **Phản ứng:** đội không nhân máy móc Velocity với 0,85 mà chỉ dùng làm mốc tham khảo (17 × 0,85 ≈ 14,5; 15,7 × 0,85 ≈ 13,3), chọn khoảng dự báo nghiêng về phía thấp khoảng 13 đến 14 SP, chọn PBI đã đủ rõ phục vụ Sprint Goal kèm một PBI nhỏ dự phòng. Nguyên nhân (nghỉ phép) được ghi vào sổ Velocity để sau này không hiểu nhầm là đội làm kém.

### Trả lời đề nghị xếp hạng đội theo Velocity của quản lý

> SP là thước đo tương đối riêng của từng đội (mỗi đội ước lượng theo mốc riêng của mình), nên không so được đội đặt xe với đội ứng dụng tài xế, và nếu dùng để xếp hạng thì đội sẽ có xu hướng ước lượng cao lên cho "đẹp số". Quản lý nên theo dõi **Sprint Goal có đạt không, phản hồi của người dùng và các bên liên quan sau Sprint Review, các vướng mắc đội đang gặp và chất lượng bàn giao (ví dụ số lỗi nghiêm trọng còn mở)**.
