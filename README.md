# Matrix_CSV

Chương trình C đọc 2 ma trận từ file CSV và thực hiện các phép toán cộng, trừ, nhân ma trận. Người dùng chọn file CSV khi chạy chương trình thông qua tham số dòng lệnh.

---

## 1. Cấu trúc thư mục

```
Matrix_CSV/
│── main.c          // mã nguồn C
│── Book1.csv       // dữ liệu ma trận mẫu
│── Book2.csv       // dữ liệu ma trận mẫu
│── output/         // file thực thi sau khi build
│── README.md
```

---

## 2. Định dạng file CSV

Mỗi file CSV chứa 2 ma trận, phân cách bằng dòng chữ `matran1` và `matran2`.

Ví dụ:
```
matran1
11,6,0
9,7,-3
4,-7,10
matran2
3,0,12
8,-4,60
5,-13,0
```

- Các phần tử cách nhau bằng dấu `,`
- Không có khoảng trắng thừa
- Số hàng và cột có thể thay đổi (chương trình tự kiểm tra điều kiện)

---

## 3. Cách biên dịch chương trình

Yêu cầu: đã cài gcc (MinGW-w64 trên Windows).

Tại thư mục chứa `main.c`, chạy:

```bash
gcc main.c -o main
```

---

## 4. Cách chạy chương trình

Chạy với file CSV mong muốn:

```bash
./main Book1.csv
```
hoặc
```bash
./main Book2.csv
```

Chương trình sẽ in ra:
- Ma trận A
- Ma trận B
- Kết quả A + B (nếu hợp lệ)
- Kết quả A - B (nếu hợp lệ)
- Kết quả A * B (nếu hợp lệ)

Nếu không thực hiện được phép toán, chương trình sẽ thông báo rõ lý do (khác số hàng, khác số cột, sai điều kiện nhân).

## Lưu ý về vị trí file CSV

Do chương trình được chạy từ thư mục `output`, nên **file CSV (Book1.csv, Book2.csv) phải được đặt trong cùng thư mục `output` với file thực thi**.

Ví dụ cấu trúc khi chạy chương trình:

output/
│── main.exe
│── Book1.csv
│── Book2.csv


---

## 5. Ví dụ kết quả

```
Dang doc du lieu tu file: Book1.csv

Ma tran A:
11   6   0
9    7  -3
4   -7  10

Ma tran B:
3    0  12
8   -4  60
5  -13   0

A + B:
14   6  12
17   3  57
9  -20  10
```

---

