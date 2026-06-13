# Git Safety Foundation Practice

**Họ và tên:** Văn Ngọc Tường Lân

**Mã sinh viên:** 25E1020029

## Mục tiêu thực hành
Dự án này được thực hiện nhằm mục đích nắm vững quy trình quản lý phiên bản với Git, đảm bảo an toàn cho mã nguồn trước khi tham gia khóa học Vibe Coding.

## Quá trình thực hiện
- **Quản lý Commit:** Đã thực hiện 10+ commits có ý nghĩa để ghi lại quá trình thay đổi file `text.txt`.
- **Làm việc với Branch:** Đã tạo và làm việc trên các nhánh `feature-nhanh-1` và `feature-nhanh-2` để cô lập tính năng.
- **Pull Request (PR):** Đã tạo 2 Pull Requests để merge các nhánh phụ vào nhánh `main`.
- **Xử lý Conflict:** Đã thực hành tạo xung đột bằng cách sửa cùng một dòng dữ liệu trên nhánh `main` và nhánh `feature`, sau đó thực hiện xử lý bằng cách sửa trực tiếp mã nguồn và commit lại.
- **Rollback/Revert:** Đã thực hiện lệnh `git revert` để hoàn tác một thay đổi không mong muốn trong lịch sử commit.

## Danh sách các lệnh Git đã sử dụng
- `git status`: Kiểm tra trạng thái hiện tại của các file
- `git init`: Khởi tạo repository.
- `git add .`: Đưa các thay đổi vào staging area.
- `git commit -m "..."`: Lưu lại các thay đổi.
- `git branch / git checkout -b`: Tạo và chuyển đổi nhánh.
- `git push origin <branch>`: Đẩy code lên GitHub.
- `git merge`: Gộp nhánh.
- `git log --oneline`: Xem lịch sử commit rút gọn.
- `git revert <hash>`: Hoàn tác commit.

## Nhật ký xử lý lỗi
### Tình huống Conflict (trên file text.txt - bài thơ Chị em Thúy Kiều)
- **Cách tạo:** Sửa cùng một dòng đầu tiên ("Đầu lòng hai ả tố nga") ở nhánh `main` và nhánh `feature-conflict-tho`.
- **Giải quyết:** Thực hiện `git merge`. Khi gặp conflict, đã mở file `text.txt`, xóa các tag đánh dấu của Git và giữ lại nội dung chỉnh sửa cuối cùng, sau đó thực hiện commit để hoàn tất merge.

### Tình huống Revert (trên file text.txt)
- **Mục tiêu:** Hoàn tác thay đổi tại commit "fix: resolve conflict bai tho".
- **Thực hiện:**
  1. Dùng `git log --oneline` để xác định hash commit cuối cùng.
  2. Chạy lệnh `git revert [Mã hash]`.
  3. Kiểm tra file `text.txt`: Bài thơ đã tự động trở về định dạng nguyên bản trước khi thực hiện commit fix conflict.

  
## Tôi sẽ dùng Git như thế nào khi Vibe Code với AI?
"Trong môi trường Vibe Coding, nơi AI hỗ trợ sinh code với tốc độ cao, em coi Git là 'phanh an toàn' không thể thiếu. Em sẽ luôn:
1. **Tạo nhánh mới:** Trước khi yêu cầu AI sinh bất kỳ tính năng nào.
2. **Commit nhỏ gọn:** Để dễ dàng kiểm soát và cô lập lỗi nếu code từ AI không ổn định.
3. **Merge có kiểm soát:** Chỉ thực hiện merge vào nhánh chính sau khi đã kiểm tra kỹ lưỡng (review) để đảm bảo hệ thống luôn ở trạng thái ổn định."

