##  Bài học 

### Tổng 

Vào năm lớp 6 THCS (theo chương trình học Việt Nam ...), chúng ta đã quen thuộc với bài toán đếm tổng dãy từ 1 đến 100 huyền thoại mà ở đó nhà toán học người Đức Carl Gauss đã giải bằng một phương pháp thú vị . . . mà tổng tính được từ dãy đó là 5050

Nếu ta viết lại đáp án bài toán lại như sau

$$1+2+3+4+5+.... + 100 = 5050$$ 
thì sẽ rất dài. 

Kí hiệu tổng: 

```latex
\(\sum\)
```

$\sum$

được phát minh lần đầu bởi nhà toán học Euler vào năm 1755. 

. . . (? viết tiếp)

<div align="center">
<img src="LaTeX-Library-project-v1.0.0/Draft/draft img/1.1.jpg" alt="1.1">
Nguồn: https://thomaskojar.wordpress.com/2021/05/13/history-of-math-symbols/
</div>

$$
\sum^{100}_{n = 1} n = 5050 
$$

#### inline math

Để viết kí hiệu tổng (sigma) ta sẽ sử dụng lệnh: 

```tex
\sum  
```

Lệnh này đã được hệ thống cài đặt sẵn, nên ta không cần phải khai báo thêm package nào thêm cả.

Ví dụ về kí hiệu sigma không có điều kiện (? chuẩn thuật ngữ chưa nhỉ) 

```tex
\documentclass{article}

\begin{document}

\[
     \sigma C_n = . . .  
\]

\end{document}
```

>[!WARNING]
> Nếu như chúng ta viết sát biểu thức (? đúng chưa nhỉ, còn gì nữa nhỉ) với lệnh `\sigma`, hệ thống sẽ báo lỗi **Undefined control sequence**. 

```tex
\documentclass{article}

\begin{document}

\[
     \sigmaC_n = . . .  
\]

\end{document}
```

Ví dụ về kí hiệu sigma có điều kiện (? chuẩn thuật ngữ chưa nhỉ) 

```tex
\(\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s}\)
```

$\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s}$

So với việc viết kí hiệu tổng không điều kiện (?) ở trên, ta có thể viết liền chúng mà không bị hệ thống báo lỗi.

```tex
\(\zeta(s) = \sum_{n=1}^{\infty}\frac{1}{n^s}\)
```

Tuy vậy, chúng ta nên cách ra để khi đọc đoạn mã sẽ dễ dàng hơn. (? . . . vì sao thế nhỉ) 

Để có thể căn chỉnh kí hiệu tổng sao cho đẹp, ta có thể sử dụng lệnh: 

```tex
\displaystyle
```

vào trước lệnh `\sum`

```tex
\documentclass{article}

\begin{document}

\(\zeta(s) = \displaystyle\sum_{n=1}^{\infty} \frac{1}{n^s}\)

\end{document}
```

$\zeta(s) = \displaystyle\sum_{n=1}^{\infty} \frac{1}{n^s}$  

Ngoài lệnh `\displaystyle` để căn chỉnh trên ta còn có các lệnh sau: 

|Lệnh|Mô tả|Ghi chú thêm|
|:---|:----|:-----------| 
|`\textstyle`|Kích thước dành cho các phương trình được viết ở chế độ toán học **inline math**|Vì kích thước của chúng đã hệ thống mặc định như ban đầu, nên ta không cần phải sử dụng trong việc viết chúng trong toán học ở chế độ| 

Để dễ hình dung, ta quay lại với ví dụ ban đầu, nếu ta thêm lệnh `textstyle`: 

```tex
\documentclass{article}

\begin{document}

\(\zeta(s) = \textstyle\sum_{n=1}^{\infty} \frac{1}{n^s}\)

\end{document}
```

Kết quả cho ra được cũng ra giống hệt với lúc ban đầu:  

$\zeta(s) = \textstyle\sum_{n=1}^{\infty} \frac{1}{n^s}$  

Vậy nên ta chỉ cần viết như cách ban đầu là được, mà không cần phải sử dụng lệnh `\textstyle`. 

**Câu hỏi**: Vậy lệnh `\textstyle` nên được sử dụng vào lúc nào ? 

Nếu chúng ta viết một đoạn văn dài, có chứa bên trong đoạn văn công thức tổng sử dụng lệnh `\displaystyle`, chẳng hạn như ví dụ sau: 

```tex
\documentclass{article}

\begin{document}

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Ut purus elit, vestibulum ut, placerat ac, adipiscing vitae, felis. Curabitur dictum gravida mauris. Donec vehicula augue eu neque. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas
\(
     \displaystyle\sum^{100}_{n = 1} k = 5050 
\)
Nam arcu libero, nonummy eget, consectetuer id, vulputate a, magna.Donec vehicula augue eu neque. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas

\end{document}
```

Có thể thấy, một khoảng cách rộng giữa dòng trong đoạn văn bản chứa kí hiệu tổng sử dụng lệnh `\displaystyle` và dòng không chứa kí hiệu tổng đó. 

**Câu hỏi**: Điều này làm ảnh hưởng gì đến với người đọc ?

**Câu hỏi**: Làm thế nào để giải quyết vấn đề trên ?

. . .

Vấn đề này bạn cũng sẽ gặp rất nhiều đối với các bài học . . . (? gồm những phần bài học nào có gặp vấn đề trên)

---

#### display math

```latex
\[\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s}\]
```

$$
\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s}
$$

Giả sử, cho $s = 2$, thay vào . . . ta được: 

$$
\zeta(2) = \sum_{n=1}^{\infty} \frac{1}{n^s} = \frac{1}{1^2} + \frac{1}{2^2} + \frac{1}{3^2} + \dots
$$
. . . (đọc đầy đủ định lý ở đây https://pkg.yihui.org/bookdown/markdown-extensions-by-bookdown#theorems) 

Từ những kiến thức đã trình bày ở trên về cách viết kí hiệu tổng trên, ta viết gọn lại bài toán tổng ở đầu bài như sau: 

```latex
\[\sum_{n = 1}^{100} = 5050\]
```

$$
\sum^{100}_{n = 1} n = 5050 
$$

#### Mở rộng: 



---

## Câu hỏi: 

**Câu hỏi 1**: Tại lại là lệnh `\sum` mà không phải là lệnh `\Sigma`, để viết kí hiệu tổng (sigma). 