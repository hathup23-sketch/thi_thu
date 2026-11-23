# BÀI LÀM PHA 2 (ĐỀ LUYỆN TẬP CHỦ ĐỀ TÀI CHÍNH CÁ NHÂN)

- **Họ tên:**PHẠM THỊ THU HÀ
- **Lớp:**CNTT3
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**Gemini

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đăng ký hội thảo ra JSON

**KET QUA AI**

```text
[
  {
    "ma_goi": "DT",
    "ngay_hoi_thao": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "hang_ve": "thuong",
    "ghi_chu": null
  },
  {
    "ma_goi": "CB",
    "ngay_hoi_thao": "2027-01-10",
    "nguoi_lon": 3,
    "tre_em": 0,
    "hang_ve": null,
    "ghi_chu": "dùng xe lăn cần lối đi riêng"
  },
  {
    "ma_goi": "VIP",
    "ngay_hoi_thao": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "hang_ve": "vip",
    "ghi_chu": "mắt kém cần ngồi bàn đầu gần màn hình chiếu"
  }
]
```

**Link trò chuyện:**https://share.gemini.google/RKP9NrlQqANu

## 4.3. Báo giá vé hội thảo bằng Chain-of-Thought

**KET QUA AI**

```text
Tiền người lớn:
Nhóm có 4 người lớn, chọn gói DT (1.500.000 đồng/người):4 × 1.500.000 = 6.000.000 (đồng).

Tiền trẻ em:

Có 2 trẻ em trong độ tuổi từ 6 đến 12 (8 tuổi và 11 tuổi), mỗi bé tính 50% giá người lớn (50% × 1.500.000 = 750.000 đồng/bé).

1 bé 4 tuổi (dưới 6 tuổi) được miễn phí (0 đồng).

Phép tính: 2 × (50% × 1.500.000) + 1 × 0 = 2 × 750.000 + 0 = 1.500.000 (đồng).

Tiền vé:
Cộng tiền người lớn và tiền trẻ em:6.000.000 + 1.500.000 = 7.500.000 (đồng).

Giảm giá nhóm:
Nhóm có 4 người lớn (đủ điều kiện từ 4 người lớn trở lên), được giảm 10% trên tiền vé:10% × 7.500.000 = 750.000 (đồng).(Tiền vé sau giảm: 7.500.000 - 750.000 = 6.750.000 đồng).

Phụ thu sổ tay:
Nhóm mua 2 bộ sổ tay, giá 200.000 đồng/bộ (không giảm giá):2 × 200.000 = 400.000 (đồng).

Tổng tiền:
Tiền vé sau giảm cộng phụ thu sổ tay:(7.500.000 - 750.000) + 400.000 = 6.750.000 + 400.000 = 7.150.000 (đồng).

[RESULT: 7.150.000 đồng]
```

**Link trò chuyện:**https://share.gemini.google/0diSqbAohXOL

### b) Kiểm tra kết quả AI

AI đã trả lời đúng 
## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "sai_khu_vuc",
  "so_khach": 2,
  "so_phien_bi_anh_huong": 2,
  "tom_tat": "Khách mua vé gói DT bị xếp ngồi ghế phụ thiếu bàn viết trong 2 phiên đầu."
}
```

**Link trò chuyện:**https://share.gemini.google/ER6Ko3VmlqiZ

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
Tiêu chíĐiểmMinh chứngĐề xuất sửaĐúng thông tin (50% - Tối đa 5.0đ)5.0 / 5.0Nhân viên đã cung cấp thông tin giá vé (1.200.000đ/người) và chính sách hoàn hủy (báo hủy trước 4 ngày hoàn 100%). Lưu ý: Do đề bài không đính kèm tài liệu thông tin chuẩn của ban tổ chức để đối chiếu, tiêu chí này tạm tính điểm tối đa dựa trên việc nhân viên đã nêu đủ các thông số chính sách.(Giữ nguyên nội dung thông số nếu đã khớp với quy định của ban tổ chức)Đầy đủ (30% - Tối đa 3.0đ)1.5 / 3.0- Đạt: Đã trả lời được 2 câu hỏi của khách hàng về giá vé và chính sách hủy vé.- Câu bị lỗi: "cứ yên tâm chốt đơn đi ạ!"- Lý do sai: Thiếu thông tin mời khách hàng cung cấp ngày hội thảo và số lượng vé muốn đăng ký theo đúng yêu cầu của thang điểm."Anh/chị vui lòng cho bên em xin thông tin về ngày tham dự hội thảo và số lượng vé muốn đăng ký để bên em hỗ trợ giữ chỗ cho mình nhé."Giọng điệu (20% - Tối đa 2.0đ)0.5 / 2.0- Câu bị lỗi 1: "Dạ chào anh/chị nha!", "hoàn lại đủ 100% tiền vé nha, cứ yên tâm chốt đơn đi ạ!"- Lý do sai 1: Sử dụng các từ ngữ mang tính suồng sã, thiếu trang trọng trong giao tiếp dịch vụ khách hàng chuyên nghiệp ("nha", "chốt đơn").- Câu bị lỗi 2: "đi học về đầu tư chứng khoán lời khủng luôn ạ."- Lý do sai 2: Cam kết, hứa hẹn lợi nhuận quá đà ("lời khủng luôn"), gây rủi ro về mặt truyền thông và uy tín trong lĩnh vực đào tạo đầu tư tài chính.- Sửa lỗi 1: "Dạ chào anh/chị!" và "hoàn lại 100% chi phí vé ạ."- Sửa lỗi 2: "Khóa học sẽ trang bị cho anh/chị kiến thức nền tảng và phương pháp đầu tư chứng khoán bài bản, hiệu quả ạ
TỔNG ĐIỂM7.0 / 10
```

**Link trò chuyện:**https://share.gemini.google/enOI6ZRRiuwL
