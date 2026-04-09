# Individual reflection — Huỳnh Thái Bảo (AI20K001)

## 1. Role
Test speech to text model. Phụ thiết kế flow chatbot.

## 2. Đóng góp cụ thể
- Tìm và test các model speech to text, build logic cho model speech to text.
- Viết và test các test case cho speech to text model.

## 3. SPEC mạnh/yếu
- Mạnh nhất (Failure Modes): Nhận diện rủi ro khi user cung cấp địa chỉ chung chung (VD: "Đến chợ Bến Thành" nhưng không rõ cổng). Giải pháp: AI tự động hỏi follow-up để chốt tọa độ/vị trí đón chính xác, tránh tài xế hủy cuốc.
- Yếu nhất (ROI): Các kịch bản tài chính hiện chỉ khác nhau về số lượng cuốc xe. Cần tách rõ giả định: Thận trọng (chỉ áp dụng cho khách dùng app) và Lạc quan (thay thế hoàn toàn tổng đài truyền thống bằng AI Voice).

## 4. Đóng góp khác
- fix bug hallucination cho model speech to text

## 5. Điều học được
Trước hackathon nghĩ precision và recall chỉ là metric kỹ thuật.
Sau khi thiết kế AI triage mới hiểu: chọn recall cao hơn cho khoa cấp cứu
(bỏ sót nguy hiểm hơn false alarm) nhưng precision cao hơn cho khoa chuyên sâu
(gợi ý sai gây lãng phí thời gian bệnh nhân). Metric là product decision,
không chỉ engineering decision.

## 6. Nếu làm lại
Sẽ test prompt sớm hơn — ngày đầu chỉ viết SPEC, đến trưa D6 mới bắt đầu test prompt.
Nghĩ và test các trường hợp worst case nhiều hơn happy case.
Nghĩ ra nhiều test case hơn.

## 7. AI giúp gì / AI sai gì
- **Giúp:** dùng Gemini để brainstorm failure modes. Dùng Gemini để test prompt nhanh qua AI Studio.
- **Sai/mislead:** Gemini gợi ý và fix bug nhưng vẫn còn thiếu sót nhiều chỗ.
