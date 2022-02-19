---
template: blog-post
title: "Cách chuyển hệ cơ số 2 sang hệ cơ số 8, 10, 16 và ngược lại - siêu dễ  "
slug: /cach-chuyen-he-co-so-2-sang-he-co-so-10-va-nguoc-lai
date: 2022-02-19 16:44
description: chuyển hệ cơ số, kiến trúc máy tính
featuredImage: /assets/screenshot-2022-02-19-165028.png
---
Hi, hôm nay mình bắt đầu một môn học có tên là lập trình hợp ngữ - assemply. Bắt đầu buổi học, cố giáo có ôn lại cho chúng mình kiến thức về chuyển đổi hệ cơ số này sang hệ cơ số khác ( rất nhiều môn cơ sở nền tảng rất hay gặp tiêu biểu là môn kiến trúc máy tính). Khi cô giáo hỏi thì hầu như cả làm là cũng quên sạch kiến thức cũ ^^.  Khi được tìm hiểu lại thì mình thấy cũng rất dễ  hiểu nên muốn chia sẻ lại cho mọi  người. Oke bắt đầu thôi !!

Đầu tiên mình muốn các bạn nhớ một mẹo nhỏ đó là : 2 Nhân 10 Chia

vậy 2 nhân 10 chia là cái gì?

### Chuyển hệ cơ số 2 sang hệ cơ số khác

Cách đổi: Tổng của "các bit" nhân với "

### Chuyển hệ cơ số 10 sang hệ cơ số khác

> Cách đổi: Lấy "số cần đổi" chia liên tiếp cho 'hệ cơ số cần đổi", dừng khi số bị chia bằng 0. Kết quả là các số dư lấy theo chiều ngược lại

```
vd: chuyển số 12 từ hệ cơ số 10 sang hệ cơ số 2

12 : 2  = 6
   0        6 : 2 = 3
              0         3 : 2  = 1
                         1           1 : 2  =  0    dừng
                                           1
 vậy kết quả là: 12(10) = 1100(2)
 
 // chuyển sang hệ cơ số  8 hay 16 thì cũng tương tự vậy.
 // mình sẽ thêm ví dụ chuyển sang hệ cơ số 8
 
 12 : 8  = 1 // chia cho hệ cơ số cần chuyển đổi, ở đây là 8
   4        1 : 8 = 0 dừng // dừng khi số chia là 0
              1        
 vậy kết quả là: 12(10) = 14(8) // kết quả là số dư theo chiều ngược lại
 

```

rất đơn giản phải không nào :))

### Chuyển hệ cơ số khác sang hệ cơ số 10

> Cách đổi: Lấy "lần lượt n các chữ số" nhân với "hệ cơ số ban đầu mũ n-1".  kết quả là tổng của dãy số.  Giải thích chuối quá. Xem vd để hiểu hơn nhé.

```
vd: chuyển số 1010 từ hệ cơ số 2 sang hệ cơ số 10
  1*2^3  + 0*2^2 + 1*2^1 + 0*2^0 //>  Lấy "lần lượt n các chữ số" nhân với "hệ cơ số ban đầu mũ n-1".
  = 8 + 0 + 2 + 0
  = 10

 vậy kết quả là: 1010(2) = 10(10)
 
 // chuyển từ hệ cơ số 8 hay 16 sang hệ cơ số 10 cũng tương tự vậy.
 // mình sẽ thêm ví dụ chuyển từ hệ cơ số 16 sang hệ cơ số 10
 1A(16) = ? (10)
   1*16^1 + 10*16^0 // Chữ A hệ 16 tương đương số 10 hệ 10
   = 16 + 10
   = 26
 
 vậy kết quả là: 1A(16) = 26(10) 
 

```

rất đơn giản phải không nào :))