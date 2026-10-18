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
\sum^{100}_{n = 1} k = 5050 
$$

**inline math**

```latex
\(\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s}\)
```

$\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s}$

Hoặc có thể thêm lệnh 

```latex
\displaystyle
```

vào trước lệnh `\sum`

```latex
\(\zeta(s) = \displaystyle\sum_{n=1}^{\infty} \frac{1}{n^s}\)
```

$\zeta(s) = \displaystyle\sum_{n=1}^{\infty} \frac{1}{n^s}$  

**display math**

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

Từ những kiến thức đã trình bày về cách viết kí hiệu tổng trên, ta viết gọn lại bài toán tổng ở đầu bài như  sau: 

```latex
\[\sum_{n = 1}^{100} = 5050\]
```

$$
\sum^{100}_{n = 1} k = 5050 
$$

### Tích phân 

Kí hiệu tích phân: 

```latex
\int
```

$\int$

Cách viết tương tự như viết tổng. 

**inline math** (sau thay bằng bài học mẹo tính tích phân của nhà vật lý học Richard Feynman)

```latex
\(\int_a^b f(x) \mathrm{d}x = F(b) - F(a)\)
```

$\int_a^b f(x) \mathrm{d}x = F(b) - F(a)$

```latex
\(\displaystyle\int_a^b f(x) \mathrm{d}x = F(b) - F(a)\)
```

$\displaystyle\int_a^b f(x) \mathrm{d}x = F(b) - F(a)$ 

**display math** 

$$
\int_a^b f(x) \mathrm{d}x = F(b) - F(a)
$$

Một cách khác để viết tích phân. (thật ra là rất quen thuộc)

Trước tiên cần khai báo package `amsmath` và để thêm tùy chọn (options) là `intlimits`:

```latex
\usepackage[intlimits]{amsmath}
```

**inline math** 

```latex
\(\int\limits_a^b f(x) \mathrm{d}x = F(b) - F(a)\)
```

$\int\limits_a^b f(x) \mathrm{d}x = F(b) - F(a)$  

hoặc

```latex
\(\displaystyle\int\limits_a^b f(x) \mathrm{d}x = F(b) - F(a)\)
```

$\displaystyle\int\limits_a^bb f(x) \mathrm{d}x = F(b) - F(a)$

**display math** 

```latex
\[\int\limits_a^b f(x) \mathrm{d}x = F(b) - F(a)\]
```

$$
\int\limits_a^b f(x) \mathrm{d}x = F(b) - F(a)
$$

Khai triển tích phân của một hàm số: 
. . . 

```latex
\[\int\limits_a^b f(x) \mathrm{d}x = f(x)|^a_b = F(b) - F(a)\]
```

$$
\int\limits_a^b f(x) \mathrm{d}x = f(x)|^a_b = F(b) - F(a)
$$

. . .

```latex
\[\int\limits_2^3 x^2 \mathrm{d}x = \left.\frac{x^3}{3}\right|^3_2 = \frac{3^3}{3} - \frac{2^3}{3} = \frac{19}{3}\]
```

$$
\int\limits_2^3 x^2 \mathrm{d}x = \left.\frac{x^3}{3}\right|^3_2 = \frac{3^3}{3} - \frac{2^3}{3} = \frac{19}{3}
$$

## Câu hỏi: 

