## Xử lý bảng chữ cái
Cần chia tệp ra thành các tệp khác nhau dựa trên bảng chữ cái Tiếng Việt: a, ă, â, b, c, d, đ, e, ê, g, h, i, k l, m, n, o, ô, ơ, p, q, r, s, t, u, ư, v, x, y

Những chữ sẽ có dấu: a, ă, â, e, ê, i, o, ô, ơ, u, ư (Nguyên âm)

a, à, á, ả, ã, ạ
ă, ằ, ắ, ẳ, ẵ, ặ
â, ầ, ấ, ẩ, ẫ, ậ

e, è, é, ẻ, ẽ, ẹ
ê, ề, ế, ể, ễ, ệ

i, ì, í, ỉ, ĩ, ị

o, ò, ó ,ỏ, õ, ọ
ô, ồ, ố, ổ, ỗ, ộ
ơ, ờ, ớ, ở, ỡ, ợ

u, ù, ú, ủ, ũ, ụ
ư, ừ, ứ, ử, ữ, ự

- Bảng chữ cái nếu bỏ qua nguyên âm: b, c, d, đ, g, h, k, l, m, n, p, q, r, s, t, v, x, y
- Chia thành các tệp theo bảng chữ cái Latin không dấu: a, b, c, d, e, g, h, i, k, l, m, n, o, p, q, r, s, t, u, v, x, y (Tệp đặt tên "{chữ cái}".json)
- Các định nghĩa có được đặt theo thứ tự không? [Không]
- Còn các từ không tìm được định nghĩa thì sao? -> Tạo thành một tệp riêng tên là `khac.json`

## Thuật toán

Input: Một tệp JSON chứa toàn bộ từ vựng và định nghĩa 
Output: Một thư mục + Tất cả các tệp JSON đã được tách dựa trên bảng chữ cái.

Đọc thẳng và ghi thẳng ra tệp mới thay vì dùng bộ nhớ đệm để lưu toàn bộ dữ liệu vào.
Đọc bằng = Không dùng Library mà đọc trực tiếp bằng BufReader (Rồi tự Format tay bằng Sublime Text). -> Xong

Đọc từng Line một -> Trim line (dạng không có whitespace)
Cách tìm:

"an toàn": "an tâm"
"bạn đời": "an dưỡng"

Lấy Index của String, nếu glossary[1] = "a" -> cho nó vào trong tệp a.json

Những chữ có dấu -> Cho cùng vào tệp với chữ cái không dấu

## Xử lý lọc từ về tệp
Đặt thành một match, check từng chữ cái một, các chữ cái cùng loại nén vào thành một array (Tự tìm cách xử lý).

## Đưa line vào trong tệp thế nào?
Tìm hiểu cách ghi trực tiếp line vào trong tệp tương ứng với bảng chữ cái

## Chia ra thành các Function nào.

## Flow của ứng dụng 


