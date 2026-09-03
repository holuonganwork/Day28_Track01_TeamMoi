# Memo quyết định — Day28 Track 01

> Bản v2 cho use case ChatGPT viết content marketing cho TUVNORD. Các mục tên nhóm phản biện/MSSV cần nhóm bổ sung từ biên bản Chặng 3 nếu có.

## 1. Vấn đề và nguyên nhân gốc

- Vấn đề: ChatGPT tạo content marketing dài dòng, có phần thừa; nhân viên marketing phải cắt và biên tập lại, làm giảm giá trị của công cụ.
- Nguyên nhân gốc (đã thống nhất giữa Hiển & An): (1) ChatGPT chưa được đặt trong workflow có ranh giới người–AI, handoff và tiêu chí hoàn thành; (2) chưa có guardrail bắt buộc về brief, độ dài, nguồn/phiên bản và QA.

## 2. Framework đã dùng và bằng chứng

| Framework | Dùng để trả lời câu hỏi gì | Kết luận | Bằng chứng |
|---|---|---|---|
| Gartner-Lite | Nhóm đã sẵn sàng để mở rộng chưa? | Direction đạt vì sản phẩm, người dùng và 4 bước đã rõ; Readiness/Absorption chưa đủ vì thiếu chuẩn QA, nguồn có version, owner và vòng phản hồi. | Scope nhóm + quan sát trực tiếp workflow; dashboard v1 chưa có metric content-specific và hành động khi xấu. |
| Mollick | Phần nào giao cho người, AI hỗ trợ và tự động có kiểm soát? | AI tham khảo, bóc tách brief, tạo/rút gọn nháp; người marketing kiểm chứng và duyệt cuối; chỉ tự động hóa kiểm tra định dạng/độ dài, không tự động xuất bản. | Quan sát đầu ra dài dòng và công sức biên tập lại cho thấy ranh giới/tiêu chí bàn giao hiện chưa rõ. |
| ADKAR | Điểm nghẽn của người dùng là gì và cần hỗ trợ nào? | Nghẽn chính ở Desire/Ability: đầu ra dài làm giảm niềm tin, còn người dùng chưa có cách dùng prompt/checklist trong brief thật; Knowledge và Reinforcement cần được xây trong pilot. | Quan sát trực tiếp vấn đề đầu ra dài, thừa phần không cần thiết trong workflow viết content. |

## 3. Thay đổi sau phản biện (≥2)

1. V1 dùng các nhãn chung như “mức dùng”, “mục tiêu nhóm” và “đo tuần 1”, chưa chứng minh vấn đề dài dòng; v2 đổi thành product metric về tỷ lệ đạt QA lần đầu và workflow metric về thời gian brief → draft, kèm T0, target, source và owner.
2. V1 chưa quy định hành động khi chỉ số xấu; v2 thêm tỷ lệ claim có nguồn, tỷ lệ sửa vì dài dòng/không bám brief, ngưỡng chặn xuất bản và human handoff để dashboard dẫn tới quyết định sửa/giữ pilot/mở rộng.
3. Nhóm phản biện Vũ Nguyễn Bảo Sơn góp ý chưa hiểu chỉ số "thời gian brief → draft" là gì → làm rõ định nghĩa: tính bằng giờ, từ timestamp brief được duyệt đến timestamp bản nháp đầu gửi QA.
4. Nhóm phản biện Vũ Nguyễn Bảo Sơn gợi ý viết system prompt rõ ràng hơn để ChatGPT hiểu đúng và tránh sai sót → thêm yêu cầu system prompt (vai trò, giới hạn độ dài, tone, cấu trúc, bám sát brief) vào mục "Cách làm mới".

## 4. Quyết định

**Sửa**

## 5. Lý do, bước tiếp theo và owner

- Lý do: Bằng chứng hiện tại xác nhận vấn đề nhưng chưa có baseline định lượng; cần sửa workflow và guardrail trước khi đánh giá mở rộng.
- Bước tiếp theo: Trong 30 ngày, đo T0 trên 20 bài gần nhất và 10 brief hiện tại; chạy pilot với prompt template, nguồn có version, checklist QA và log human handoff. Ngày 31-60 kiểm tra mục tiêu hai tuần liên tiếp; ngày 61-90 mới quyết định mở rộng, sửa tiếp hoặc dừng.
- Owner: Trưởng nhóm content (pilot và quyết định vận hành); Hiển (nguồn, AS-IS/TO-BE, trust); An (ADKAR, dashboard v2, review metric và memo).
