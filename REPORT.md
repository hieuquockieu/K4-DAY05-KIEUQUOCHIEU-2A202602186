# Báo cáo Day 5 — điền trực tiếp trong fork của bạn

**Cách dùng:** Thay mọi dấu `…` bằng bài làm thật của bạn trước khi nộp link fork trên VLearn. Giữ nguyên bốn mục và bảng để coach đọc nhanh. Viết ngắn, cụ thể theo ảnh/vùng; không cần thuật ngữ chuyên sâu. Ví dụ trong [hướng dẫn mẫu](reports/REPORT_TEMPLATE.md) chỉ giúp hiểu cách điền, không phải câu trả lời để chép lại.

- Mã học viên theo lớp: 2A202602186
- Ngày / CVAT local: 17/09/2026 / export từ CVAT local
- Công cụ đã dùng: CVAT local; công cụ vẽ cụ thể không được lưu trong file export

Mã học viên là mã lớp cấp; không cần ghi họ tên trong report nếu kênh VLearn đã nhận diện bạn. Chỉ ghi công cụ thật sự đã dùng; không có SAM vẫn làm bài bình thường.

## 1. Bài đã nộp

Ghi tên ZIP đúng như file trong `submissions/` và số ảnh đã vẽ, Save. Chưa làm hoặc export lỗi thì ghi `chưa có`, không tạo ZIP rỗng. Cột điểm là điểm tối đa của task, **không phải điểm tự chấm**.

| Task | File ZIP đúng tên | Hoàn thành mấy ảnh | Điểm tối đa (coach chấm sau) |
| --- | --- | ---: | ---: |
| easy_semantic | Chưa có ZIP; export thư mục `job_6_annotations_2026_09_17_10_20_07_segmentation mask 1.1` | 3 / 3 | 20 |
| medium_instance | Chưa có ZIP; export thư mục `submissions/medium` | 3 / 3 | 32 |
| hard_panoptic | Chưa có ZIP; export thư mục `submissions/hard` | 2 / 2 | 30 |
| cp1_holes | chưa có | 0 / 1 | 3 |
| cp2_slice | chưa có | 0 / 1 | 3 |
| cp5_occlusion | chưa có | 0 / 1 | 3 |
| cp3_thin | chưa có | 0 / 1 | 3 |
| cp4_curb | chưa có | 0 / 1 | 3 |
| cp6_coverage | chưa có | 0 / 1 | 3 |
| **Tổng tối đa** | | | **100** |

Nếu export lỗi, ghi task, dữ liệu đã Save đến đâu và lỗi đã báo coach.

## 2. Một quyết định trước khi dùng gợi ý

Chọn object đầu tiên bạn tự vẽ ở `medium_instance`, trước khi xem bất kỳ đề xuất tự động nào cho object đó. Ghi ảnh/vị trí đủ để tìm lại; “quy tắc biên” là lý do bạn chọn hoặc dừng mask ở ranh đó.

- Ảnh, vị trí và object Medium đầu tiên tự vẽ: Chưa xác minh được từ export; file COCO không lưu thứ tự thao tác.
- Class và quy tắc tôi dùng để chọn biên: Chưa có ghi chép thao tác để đối chiếu; cần bổ sung trước khi nộp.
- Nếu dùng gợi ý sau đó: Chưa xác minh được từ export; không tự kết luận có hoặc không dùng gợi ý.
- Nếu không dùng gợi ý: Chưa xác minh được từ export.

## 3. Một lỗi tôi tìm thấy và sửa

Chọn một lỗi **có thật** trong bài. Nếu công cụ lỗi khiến bạn chưa sửa được, ghi rõ đã thử gì và cần coach hỗ trợ gì; không ghi “đã sửa” khi chưa sửa.

- Task/ảnh/vùng: …
- Lỗi thuộc loại: sai lớp / thiếu-thừa vật / gộp-tách / biên / phủ vùng / khác: …
- Bằng chứng tôi nhìn thấy: …
- Quy tắc và hành động sửa: …
- Sau sửa đã Save và export lại chưa? …

Nếu bạn **đã xem Summary tự đánh giá trên GitHub Actions hoặc tự chạy script**, ghi ngắn một kết quả liên quan lỗi vừa sửa (ví dụ task, metric trước/sau nếu có): … / chưa có điểm. Scorecard ba tier tối đa **82**, không phải điểm cuối trên 100. Không tự ghi PASS/top 3/bonus; người phụ trách xác nhận theo tiêu chí lớp. Không đưa file ground truth vào fork.

## 4. Ba ca chưa chắc hoặc đã cân nhắc

Mỗi ca là một **vùng cụ thể** khiến bạn phải cân nhắc hai cách hiểu. Ghi dấu hiệu nhìn thấy hoặc quy tắc đã dùng, rồi nêu quyết định hoặc câu hỏi cho coach. Không cần ba lỗi; ca đã quyết định được cũng hợp lệ.

| Ảnh/vị trí | Hai cách hiểu có thể | Quy tắc/chứng cứ | Quyết định hoặc câu hỏi cho coach |
| --- | --- | --- | --- |
| `medium/000000181542.jpg`, xe máy tiền cảnh và người đi bộ ở giữa | Gộp các pixel của xe máy và người / tách thành các object theo vật | Biên vật thể bị chồng lấp trong ảnh; Medium yêu cầu mỗi vật là một instance riêng | Chọn tách theo từng vật và chỉ vẽ phần nhìn thấy; cần người học xác nhận đây là quyết định đã dùng |
| `medium/000000373353.jpg`, xe buýt đỏ và xe vàng ở trung tâm | Gán cả vùng xe vàng vào xe buýt / tách thành hai object | Hai phương tiện có đường biên và màu khác nhau, dù đứng sát nhau | Chọn hai instance riêng; kiểm lại khe/biên giữa hai xe trước khi Save |
| `hard/000000460147.jpg`, dải phân cách cây ở giữa đường | Gán dải cây vào road / gán thành vegetation và giữ road hai bên | Dải cây là vùng có vật thể thực; Hard cần phân biệt stuff theo lớp | Chọn vegetation cho dải cây, road cho mặt đường; cần coach xác nhận tại vùng biên |
