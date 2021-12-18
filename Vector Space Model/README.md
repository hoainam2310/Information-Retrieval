# VECTOR SPACE MODEL

## 1. Giới thiệu

> Biểu diễn văn bản và các câu truy vấn dưới dạng **Vector** trong một không gian đa chiều.
 
> Tính toán giữa truy vấn và tài liệu dựa trên chiều dài và hướng của vector tương ứng của chúng.

> Khoảng cách giữa hai vector tài liệu và truy vấn được xem là độ tương đồng giữa tài liệu và truy vấn. 

> Khoảng cách này được dùng để xếp hạng tài liệu.

## 2. Chọn term (xử lý dữ liệu)

> **Tách từ (Tokenization)**: Tách các câu hoặc văn bản thành các đơn vị nhỏ hơn, các đơn vị nhỏ hơn được gọi là “token”.

> **Loại bỏ Stopword**: Loại bỏ những token xuất hiện nhiều hoặc không có nghĩa để giảm thời gian tính toán, lưu trữ. Các token sẽ bị loại bỏ có thể là các mạo từ (“a”, “an”, “the”, ...) hay các danh xưng sở hữu (“its”, ...)

> **Stemming**: Loại bỏ một số kí tự ở cuối từ để đưa về dạng từ gốc.

## 3. Trọng số term và lập chỉ mục

**Trọng số**

> Trọng số mỗi term tính bằng **TF-IDF** (Term Frequency - Inverse Document Frequency)

> **TF**: Tần số xuất hiện của mỗi từ trong tài liệu (tính bằng số lượng term **k** xuất hiện trong tài liệu **i**)

> **IDF**: Ngịch đảo tần suất tài liệu của term (log_10(tổng số tài liệu / số tài liệu chứa term **K**) )

> **TF-IDF**: giá trị **TF** nhân với **IDF** tương ứng.

**Lập chỉ mục**: Đưa tài liệu về dạng vector

> Mỗi vector sẽ có số chiều bằng tổng các term có trong tài liệu.

> Giá trị mỗi chiều bằng giá trị **TF-IDF** tương ứng.

## 4. Xử lý truy vấn

> Xử lý văn bản tương tự Bước 2

> Tính giá trị **TF** của truy vấn.

> Tính giá trị **TF-IDF** của truy vấn thông qua giá trị **IDF** của tài liệu.

> Chuyển thành vector truy vấn.

## 5. Xếp hạng tài liệu - cách tính

> Tính toán độ tương đồng bằng công thức **Cosine Similarity**

> Tính giá trị giữa vector truy vấn với từng vector tài liệu.

> Xếp giảm dần độ tương đồng của tài liệu.

## 6. Đánh giá dựa trên kết quả trả về

- Dữ liệu:
