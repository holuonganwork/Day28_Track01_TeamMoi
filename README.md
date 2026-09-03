# Day28_Track01_TeamMoi

## 1. Thành viên

| Họ tên | MSSV | Phần phụ trách | Góp ý đã đưa cho nhóm bạn |
|---|---|---|---|
| Hiển | TODO | Gartner-Lite (readiness) + AS-IS/TO-BE + kiến trúc tin cậy + setup repo/README | TODO — điền sau Chặng 3, ghi rõ tên nhóm phản biện |
| Hồ Lương An | 2A202601332 | Mollick (phân chia người–AI) + ADKAR (người dùng) + Lộ trình 30-60-90 + Dashboard v2/Memo | Chưa có tên nhóm phản biện trong dữ liệu đầu vào; cần bổ sung tên nhóm và góp ý thực tế sau Chặng 3 |

> Lưu ý: 3 framework (Gartner-Lite, Mollick, ADKAR) phải cùng trỏ về **1-2 nguyên nhân gốc chung**, không phải 2 kết luận riêng ghép lại — thống nhất trước khi điền mục 3.

## 2. Phạm vi

- Sản phẩm AI: ChatGPT dùng viết content marketing cho TUV Nord.
- Nhóm người dùng chính: Nhân viên marketing.
- 4 quy trình liên quan: tham khảo content đã viết trước đó → đọc brief/yêu cầu mới → viết content bằng AI → kiểm chứng trước khi dùng/xuất bản.
- Vấn đề quan sát được: đầu ra AI dài dòng, có phần thừa và làm tăng công sức biên tập lại.

## 3. Nguyên nhân gốc

- Nguyên nhân 1: ChatGPT chưa nằm trong một workflow có ranh giới người–AI, điểm bàn giao và tiêu chí hoàn thành rõ (framework: Mollick + ADKAR Ability/Reinforcement; bằng chứng: quan sát trực tiếp cho thấy người viết phải tự xử lý đầu ra dài dòng sau khi AI viết).
- Nguyên nhân 2: Chưa có guardrail chất lượng bắt buộc — brief, độ dài mục tiêu, nguồn/phiên bản và checklist QA — nên AI không biết phần nào cần giữ hoặc loại bỏ (framework: ADKAR Desire/Knowledge + Mollick; bằng chứng: vấn đề được quan sát trực tiếp trong workflow là nội dung thừa, kéo theo biên tập thủ công).

## 4. Cách làm mới

- Nguồn kiểm chứng: brief mới + kho content đã duyệt (kèm link/phiên bản/ngày cập nhật); claim kỹ thuật phải đối chiếu nguồn được duyệt.
- Người chịu trách nhiệm: AI chỉ tạo bản nháp; nhân viên marketing kiểm chứng; chủ quy trình content phê duyệt cuối và chịu trách nhiệm xuất bản; An theo dõi dashboard/feedback.
- Khi AI không chắc chắn hoặc thiếu nguồn: gắn cờ `[CẦN KIỂM CHỨNG]`, không xuất bản, chuyển người duyệt claim; ghi log lỗi để cập nhật prompt, checklist hoặc kho nguồn.
- Phân chia theo Mollick: người giữ quyền phê duyệt và ngoại lệ; AI hỗ trợ tham khảo, đọc brief, tạo và rút gọn nháp; chỉ tự động hóa kiểm tra định dạng/độ dài thấp rủi ro, không tự động xuất bản.

## 5. Chỉ số

Xem chi tiết tại [`dashboard/dashboard_hanh_dong_v2.xlsx`](dashboard/dashboard_hanh_dong_v2.xlsx) (bản trước phản biện: [`v1/dashboard_hanh_dong_v1.xlsx`](v1/dashboard_hanh_dong_v1.xlsx)).

- Product metric: tỷ lệ bản nháp đạt checklist chất lượng ngay lần QA đầu — T0 đo 20 bài gần nhất; mục tiêu ≥80% ngày 60 và ≥85% ngày 90; nguồn bảng QA; owner An + QA content.
- Workflow metric: thời gian từ brief hợp lệ đến bản nháp gửi QA — T0 đo 10 brief hiện tại; mục tiêu ≤70% baseline ngày 60; nguồn log timestamp brief/draft; owner chủ quy trình content.
- Chỉ số kiểm soát bổ sung: tỷ lệ claim/ý chính có nguồn kiểm chứng ≥95% và tỷ lệ phải sửa vì dài dòng/không bám brief ≤20% ngày 60; khi xấu thì mổ lỗi mẫu, cập nhật prompt/checklist và giữ pilot.

## 6. Quyết định

**Sửa** — chưa mở rộng ngay; trước hết chạy pilot 30 ngày với prompt template, checklist QA, nguồn có phiên bản và human handoff. So với v1, v2 (1) đổi từ nhãn chỉ số chung sang metric chất lượng product + thời gian/rework theo workflow, có T0/target/source/owner; (2) thêm ngưỡng và hành động khi chỉ số xấu, gồm chặn xuất bản và chuyển người.
Xem chi tiết tại [`memo/memo_quyet_dinh.md`](memo/memo_quyet_dinh.md).

## 7. Phần An — Mollick, ADKAR và lộ trình 30-60-90

### Mollick — phân chia quyền hạn

| Vùng | Cách áp dụng cho content marketing |
|---|---|
| Người giữ quyền | Chọn góc nội dung, duyệt giọng thương hiệu/claim, xử lý ngoại lệ và chịu trách nhiệm bản cuối trước khi xuất bản. |
| AI hỗ trợ, người kiểm | Tham khảo content đã duyệt, bóc tách brief, tạo bản nháp, rút gọn và đề xuất biến thể; người marketing kiểm tra từng đầu ra theo brief và nguồn. |
| AI tự động có kiểm soát | Chỉ kiểm tra định dạng, độ dài và các mục checklist có tiêu chí rõ; không tự động duyệt claim hoặc xuất bản. |

### ADKAR — điểm nghẽn và can thiệp

| Bước | Chẩn đoán | Can thiệp trong pilot |
|---|---|---|
| Awareness | Người dùng thấy AI viết dài nhưng chưa có chuẩn chung để nhận diện đây là vấn đề workflow. | Chia sẻ baseline về thời gian/rework và checklist “đúng brief, đủ ý, ngắn gọn, có nguồn”. |
| Desire | Đầu ra dài làm giảm niềm tin và khiến người viết quay về cách chỉnh thủ công. | Cho người dùng cùng thiết kế prompt template; chứng minh bằng thời gian xử lý và số vòng sửa giảm. |
| Knowledge | Chưa có cách đưa brief, content tham chiếu và giới hạn độ dài vào prompt. | Quick guide 1 trang cho 4 bước và ví dụ đầu ra đạt/không đạt. |
| Ability | Chưa thực hành human handoff trong brief thật. | Pilot trên brief thật, QA mẫu hằng tuần, hỗ trợ ngay khi có lỗi và cho phép chuyển người. |
| Reinforcement | Chưa có log lỗi, phản hồi và chỉ số gắn với quyết định. | Review dashboard hằng tuần; cập nhật prompt/kho nguồn/checklist khi chỉ số xấu; chỉ mở rộng sau hai tuần đạt gate. |

### Lộ trình 30-60-90 — ba cổng quyết định

| Giai đoạn | Việc chính | Owner | Dấu hiệu hoàn thành / cổng quyết định |
|---|---|---|---|
| 0-30 ngày — chứng minh vấn đề | Vẽ AS-IS/TO-BE; chọn nhóm marketing pilot; chốt kho content đã duyệt; đo T0 trên 20 bài và 10 brief; ban hành prompt template + checklist. | Trưởng nhóm content + Hiển (nguồn/workflow) + An (đo lường) | Có baseline, data owner, nguồn có version và log được 4 bước. Chưa đủ thì sửa phạm vi/nguồn, chưa mở rộng. |
| 31-60 ngày — chứng minh chất lượng | Chạy pilot; QA mẫu 10 bài/tuần; log thời gian, vòng sửa, claim thiếu nguồn; review ADKAR hằng tuần và điều chỉnh prompt. | Chủ quy trình content + QA content | Tỷ lệ đạt QA lần đầu ≥80%, claim có nguồn ≥95%, sửa vì dài dòng/không bám brief ≤20% và không có claim chưa duyệt được xuất bản. Không đạt thì quay lại chỉnh workflow. |
| 61-90 ngày — quyết định mở rộng | So sánh với T0; chốt SOP, owner vận hành và quy tắc handoff; kiểm tra governance; đề xuất mở rộng theo loại content hoặc giữ pilot. | Trưởng nhóm marketing + An (dashboard/memo) | Chỉ mở rộng nếu mục tiêu chất lượng, thời gian và rủi ro đạt liên tiếp 2 tuần; nếu không, sửa tiếp hoặc dừng use case. |
