### **Phần 1: Phân tích và thiết kế giải pháp**

**1. Phân tích I/O:**

-   **Input:** Thông tin CLB rời rạc từ Zalo: tên CLB, danh sách các ban, email trưởng ban, các bước gia nhập, checklist việc cho newbie, deadline nội quy.
-   **Output:** 1 file `README.md` duy nhất trên GitHub, khi render phải ra trang Wiki có H1/H2 rõ ràng, bảng bấm được email, code block copy được lệnh git, task list tick được, blockquote nổi bật cảnh báo.

**2. Đề xuất giải pháp :**

-   **Phần 1 Giới thiệu:** Dùng `#` cho tên CLB (H1 duy nhất), `##` cho mô tả, `**in đậm**` cho điểm nổi bật.
-   **Phần 2 Danh sách Ban:** Dùng `Table` 3 cột với `| --- |`, cột email dùng cú pháp link `[text](mailto:...)` để bấm được.
-   **Phần 3 Hướng dẫn gia nhập:** Dùng `Ordered List 1. 2. 3.` + `Code Block ```bash` để chứa lệnh git.
-   **Phần 4 Checklist:** Dùng `Task List - [x]` và `- [ ]` mix nhau.
-   **Phần 5 Lưu ý:** Dùng `> Blockquote` để làm nổi bật deadline.

**3. Các bước thực hiện:**

-   Bước 1: Gom thông tin từ Zalo vào 1 file nháp
-   Bước 2: Tạo repo `clb-lap-trinh-ptit` và tạo file `README.md` trống
-   Bước 3: Soạn 5 phần trên StackEdit theo thứ tự H1 -> Table -> List -> Task List -> Blockquote
-   Bước 4: Test render Preview và test click vào link mailto
-   Bước 5: Push lên GitHub và ghim link Wiki lên nhóm Zalo

### **Phần 2: Triển khai và chống lỗi**

# CLB Lập Trình PTIT - PTIT Coding Club

## :rocket: Giới thiệu CLB

CLB Lập trình PTIT là nơi quy tụ các sinh viên đam mê **Thuật toán, Web Fullstack và AI**.
Chúng tôi hoạt động với phương châm **Code - Share - Grow Together**.

## Danh sách Ban

| Tên Ban | Trưởng Ban | Liên hệ |
| :--- | :---: | :---: |
| Ban Kỹ Thuật | Thiện| [a.nv@ptit.edu.vn](mailto:a.nv@ptit.edu.vn) |
| Ban Truyền Thông | đệ của thiện | [b.tt@ptit.edu.vn](mailto:b.tt@ptit.edu.vn) |
| Ban Nhân Sự | đệ của thiện | [c.lv@ptit.edu.vn](mailto:c.lv@ptit.edu.vn) |

## Hướng dẫn Gia nhập

1. Fork repo này về tài khoản của bạn
2. Clone repo về máy
   ```bash
   git clone https://github.com/ptit-coding-club/wiki.git
   cd wiki
   ```

#### Tạo nhánh mới và tạo file giới thiệu bản thân
``` PowerShell
   git checkout -b member/ten-cua-ban
   ```
   **Bẫy 1 Email:** Phải dùng `[email](mailto:email)` mới bấm được để gửi mail. Gõ chữ thường thì chỉ là text, không click được.

**Bẫy 2 URL sai:** Nếu paste URL sai `htttps://...` thì Markdown vẫn render nhưng bấm vào sẽ ra trang 404. Hệ thống không tự sửa, nên phải test click ở Preview trước khi commit.
