# BÀI TẬP SESSION 04 [Vận dụng chuyên sâu] Thiết kế giải pháp Prompting ứng dụng thực tế cho Kỹ thuật Prompting Nâng cao (Logic & Chuỗi)
## 1. Thiết kế giải pháp (I/O)
### Xác định rõ Input của bài toán gồm những gì, và cấu trúc Output mong muốn.

-  **Input:** Tin nhắn thô của khách hàng.
- **Output:** 
  
    - Trường hợp bị lỗi thì báo cáo ngắn gọn thông tin, bị thiếu hoặc bị sai vào một file để nhân viên nhân viên biết và hỏi lại khách hàng.

    - Trường hợp không bị lỗi: Có phiếu xác nhận đơn hàng gồm: Tên KH, SĐT, Sản phẩm đã mua, phí ship, tổng số tiền phait thanh toán.

## 2. Viết prompt và chạy thử
### Viết prompt hoàn chỉnh theo định dạng chuyên nghiệp và copy kết quả phản hồi của AI 

- "Bạn là một nhân viên kiểm duyệt của cửa hàng. Hãy đọc tin nhắn của khách hàng dưới đây và thực hiện kiểm tra thông tin theo đúng trình tự: 
   
  -> Kiểm tra đủ 3 thông tin: Tên sản phẩm, số lượng, số điện thoại. Nếu thiếu bất kỳ thông tin nào thì dừng lại và chỉ xuất ra dòng chữ: "LỖI THIẾU THÔNG TIN".

  -> Kiểm tra số lượng nếu số lượng bằng 0 thì dường lại và chỉ xuất ra dòng chữ: "LỖI DỮ LIỆU: số lượng đặt hàng không hợp lệ."

  -> Nếu dữ liệu hợp lệ hoàn toàn thì xuất ra bản tóm tắt gồm 4 dòng: Khách hàng, số điện thoại, sản phẩm, số lượng."

  [TIN NHẮN KHÁCH HÀNG]

  " Chào shop, mình là Minh. Cho mình đặt 2 con Chuột không dây của Logitech nhé. Đây là số điện thoại của mình 0903456789."


- **Kết quả chạy thử:**

   - Khách hàng: Minh
   - Số điện thoại: 0903456789
   - Sản phẩm: Chuột không dây của Logitech
   - Số lượng: 2
