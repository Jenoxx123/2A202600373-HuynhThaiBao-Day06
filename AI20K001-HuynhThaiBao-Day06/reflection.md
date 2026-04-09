# Individual reflection — Huỳnh Thái Bảo (AI20K001)

## 1. Role
Test speech to text model. Phụ thiết kế flow chatbot.

## 2. Đóng góp cụ thể
- Tìm và test các model speech to text, build logic cho model speech to text.
- Viết và test các test case cho speech to text model.

## 3. SPEC mạnh/yếu
- Mạnh nhất: failure modes — nhóm nghĩ ra được case "triệu chứng chung chung"
  mà AI gợi ý quá rộng, và có mitigation cụ thể (hỏi thêm câu follow-up)
- Yếu nhất: ROI — 3 kịch bản thực ra chỉ khác số user, assumption gần giống nhau.
  Nên tách assumption rõ hơn (VD: conservative = chỉ dùng ở 1 chi nhánh,
  optimistic = rollout toàn hệ thống)

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