# BÀI LÀM – HACKATHON 02

- **Mã đề:** 08
- **Họ tên:** Võ Thị Thanh Thùy
- **Lớp:** HCMKS26CNTT2
- **Link repository:** https://github.com/TT-IT108/HCM_KS26_CNTT2_Nhap-mon-CNTT_Hackathon02.git
- **Hệ điều hành (Windows/macOS):** Windows

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
# Ghi lần lượt các lệnh đã chạy, mỗi lệnh một dòng
pwd
ls -Force
mv .\quy_trinh_thu_am.txt .\docs\
 mkdir backup
 cp .\data\lich_thu_thang_8.xlsx .\backup\
 rm *.tmp
 cd .\logs
 ls 
 cd ..
 ls -Force

```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        11/11/2026   2:03 PM                backup
d-----        11/11/2026   1:57 PM                data
d-----        11/11/2026   2:02 PM                docs
d-----        11/11/2026   1:38 PM                evidence
d-----        11/11/2026   1:57 PM                logs
d-----        11/11/2026   1:57 PM                web
-a----         11/3/2026   7:08 AM             74 .env
-a----         11/3/2026   7:08 AM           2409 bai_lam.md


```

## 4.3. Lọc log truy cập website

### a) Lệnh lọc các dòng status=500

```shell
 Get-Content .\logs\studio.log | Select-String "status=500" > .\logs\loi_500.txt
  Get-Content .\logs\loi_500.txt

```

### 2 dòng đầu tiên trong logs/loi_500.txt

```text
2026-08-28 08:25:34 POST /api/dat-lich status=500
2026-08-28 08:34:07 POST /api/thanh-toan status=500

```

### b) Lệnh đếm số dòng status=404 và kết quả

```shell
(Get-Content .\logs\studio.log | Select-String "status=404").Count

```

```text
4

```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
.\logs\tong_hop.ps1
```

### Nội dung file logs/tong_hop.txt

```text
 " Script: tong_hop.ps1
>> # Tac gia: Vo Thi Thanh Thuy
>> # Ngay tao: 11-11-2026
>> Write-Host "Dang tao bao cao..."
>> "=== BAO CAO SU CO WEBSITE ===" > logs/tong_hop.txt
>> Get-Content logs/studio.log  | Select-String "status=404"  >> logs/tong_hop.txt
>> Get-Content logs/studio.log  | Select-String "status=500" | Measure-Object >> logs/tong_hop.txt
>> Write-Host "Hoan thanh!"


```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [ ] README.md: Heading 1, mô tả có **in đậm** và *in nghiêng*, bảng, code block, task list, blockquote
- [ ] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [ ] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | --- | --- | --- |
| 1 | network  | logo-sound.png | sửa thành logo-sound.png trong web\images\logo-soundlab.png |
| 2 |  |  |  |

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

### Báo cáo lỗi gửi trưởng nhóm

- **Context:** 
- **Expected:** 
- **Actual:** 
- **Log:** 

### Câu tìm kiếm Google

```text
site:stackoverflow.com "ERR_FILE_NOT_FOUND"

```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/lich_thu_thang_8.xlsx`, không cần ghi vào đây.
