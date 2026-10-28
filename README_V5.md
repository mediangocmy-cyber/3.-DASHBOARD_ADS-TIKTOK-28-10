# Dashboard TikTok Shop Ngọc Mỹ – V5 (bản tối ưu tải trang)

## Sửa lỗi treo khi khởi chạy
- Thay `st.tabs()` bằng điều hướng chọn trang ở thanh bên trái. Streamlit trước đây vẫn tính cả 9 tab, dù người dùng chỉ xem một tab. Bản này chỉ dựng biểu đồ và bảng cho trang đang chọn.
- Chỉ xử lý dữ liệu phân tích Creative chuyên sâu khi vào trang Video hoặc Thẻ sản phẩm.
- Đọc Excel từ bộ nhớ bằng `openpyxl`; đọc CSV với parser C và dấu phân cách phẩy; log lỗi đọc file rõ ràng.
- Không thay đổi các công thức ROAS, CTR và SKU/Click đã có.

## Cài đặt
`pip install -r requirements.txt`

`streamlit run streamlit_app.py`

Đưa `streamlit_app.py` và `requirements.txt` lên thư mục gốc của GitHub repo. Trong Streamlit Cloud: Manage app → Reboot app; kiểm tra Logs nếu vẫn treo. Chỉ tải các file Excel/CSV xuất từ TikTok; không tải file nén ZIP vào ứng dụng.

## Lưu ý
Bản sửa đã được kiểm tra cú pháp Python. Chưa chạy thử trực tiếp trên Streamlit Cloud trong môi trường hiện tại. Nếu treo ngay cả khi chưa tải file, hãy kiểm tra log khởi tạo/dependencies và tình trạng app trên Streamlit Cloud.
