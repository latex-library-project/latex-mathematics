## Bài học:

Ta đã tìm hiểu cách để chèn toán học vào cùng với văn bản thông thường ở bài học [mở đầu](/Lecture%20notes/Mở%20đầu.md). Vậy nếu ngược lại, làm sao để ta có thể chèn văn bản thông thường vào lệnh hoặc môi trường toán học ?

Khi viết văn bản trong toán học, chẳng hạn . . . (nên viết lại thành một vấn đề ví dụ mới)

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\usepackage{amsmath}
\begin{document}
\[
Văn bản trong toán học
\]
\end{document}
```

Kết quả cho ra được là các từ sẽ được hệ thống sắp in nghiêng và bị dính vào nhau

$$
Văn bản trong toán học 
$$

Để viết được văn bản trong toán học, người dùng cần sử dụng lệnh 

```tex
\text{}
``` 

để ngăn cách phần toán học với phần văn bản.  

Áp dụng điều này vào lại ở ví dụ trên ta có 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\usepackage{amsmath}
\begin{document}
\[
\text{Văn bản trong toán học}
\]
\end{document}
```

Kết quả lúc này sẽ khác hoàn toàn so với khi chưa thêm văn bản vào trong lệnh `\text`

$$
\text{Văn bản trong toán học}
$$

Bên cạnh việc viết văn bản vào trong toán học, một số hàm trong toán học chẳng hạn như hàm lượng giác, . . vv . . được khuyến nghị . . . (? bởi ai, điều gì) soạn thảo ở dạng phông chữ thẳng đứng . . . (viết sau) 

Chẳng hạn, khi viết công thức . . . , nếu như người dùng chỉ viết hàm $\cos$. $\sin$ thông thường như ở ví dụ sau đây

```latex
\[cos(2 \alpha) = cos^2(\alpha) - sin^2(\alpha)\]
```

thì người dùng có thể thấy, chúng sẽ bị in nghiêng khi xuất sang trang tài liệu. 

Theo phản xạ nhanh, người dùng sẽ đặt các hàm đó vào trong lệnh `\text`

```latex
\[\text{cos}(2 \alpha) = \text{cos}^2(\alpha) - \text{sin}^2(\alpha)\]
```

. . . (kết quả từ ví dụ)

Một cách khác để viết các hàm toán học như $\cos$, $\sin$  . . . như ở ví dụ trên một cách ngắn gọn hơn, người dùng chỉ cần thêm dấu `\` bên cạnh hàm đó: 

```latex
\[\cos(2 \alpha) = \cos^2(\alpha) - \sin^2(\alpha)\]
```

Với một số hàm toán học đã được LaTeX cung cấp . . ., nếu như người dùng sử dụng dấu `\` để viết cho một . . . khác thì chúng sẽ báo lỗi . . . (? gì)  

```latex
\[\nam\]
```

Người dùng có thể xem đầy đủ các kí hiệu được LaTeX cài đặt sẵn . . . (? LaTeX làm sao) tại [danh sách các kí hiệu toán học, chữ cái Hy Lạp](). 

Một ví dụ toán học cụ thể trong việc viết văn bản thông thường vào lệnh hoặc môi trường viết toán học: 

```latex
\documentclass{letter}
\usepackage[utf8]{vietnam}
\usepackage{amsmath}
\usepackage{amssymb}
\usepackage{amsthm} 
\theoremstyle{definition}
\newtheorem*{definition}{Định nghĩa}

\begin{document}
\begin{definition}
    Cho \(c, d \in \mathbb{R}, c \neq d\) (thường lấy \(c=1\) và \(d = 0\)). Hàm Dirichlet được định nghĩa bởi: 
    \[
    D(x) = 
        \begin{cases}
        c \quad nếu \ x \in \mathbb{Q}\\ 
        d \quad nếu \ x \notin \mathbb{Q} 
        \end{cases}
    \]
    và không liên tục ở mọi nơi. Hàm Dirichlet có thể được viết dưới dạng giải tích như sau:
    \[
    D(x) = \lim\limits_{m \to \infty} \lim\limits_{n \to \infty} \cos^{2n}(m! \pi x)
    \]
\end{definition}

\end{document}
```

Người dùng có thể thấy, từ "nếu" được viết vào bên trong môi trường toán học sẽ bị in nghiêng. 

Sửa lại đoạn mã trên bằng lệnh `\text` ta được: 

```latex
\documentclass{letter}
\usepackage[utf8]{vietnam}
\usepackage{amsmath}
\usepackage{amssymb}
\usepackage{amsthm} 
\theoremstyle{definition}
\newtheorem*{definition}{Định nghĩa}
\begin{document}
\begin{definition}
    Cho \(c, d \in \mathbb{R}, c \neq d\) (thường lấy \(c=1 \ \text{và} \ d = 0\)). Hàm Dirichlet được định nghĩa bởi: 
    \[
    D(x) = 
        \begin{cases}
        c \quad \text{nếu} \ x \in \mathbb{Q}\\ 
        d \quad \text{nếu} \ x \notin \mathbb{Q} 
        \end{cases}
    \]
    và không liên tục ở mọi nơi. Hàm Dirichlet có thể được viết dưới dạng giải tích như sau:
    \[
    D(x) = \lim\limits_{m \to \infty} \lim\limits_{n \to \infty} \cos^{2n}(m! \pi x)
    \]
\end{definition}
\end{document}
```

<div align="center">
	
<img src="LaTeX-Library-project-v1.0.0/Draft/draft img/Dirichlet.jpg">

Nhà toán học người Đức Johann Peter Gustav Lejeune Dirichlet

</div>

Khi người dùng viết lệnh `\text` ở sau một số hay một từ nào đó như ở ví dụ sau: 

```latex
\documentclass{article}
\usepackage{amsmath}
\usepackage[utf8]{vietnam}
\begin{document}
\[500 \text{quả táo} \times 100 \text{quả cam} = \text{Siuuu}^2\]
\end{document}
```

$$
500 \text{quả táo} \times 100 \text{quả cam} = \text{Siuuu}^2
$$

Người dùng có thể thấy từ quả táo sẽ bị dính liền với số 500, còn từ quả cam cũng sẽ bị dính liền với số 100. Dù người dùng đã phím cách tạo khoảng trống giữa các số với lệnh `\text` tương ứng.  

Để khắc phục được điều này, người dùng chỉ cần nhấn phím cách văn bản trong lệnh `\text` so với dấu `{`  

```latex
\documentclass{article}
\usepackage{amsmath}
\usepackage[utf8]{vietnam}
\begin{document}
\[500 \text{ quả táo} \times 100 \text{ quả cam} = \text{Siuuu}^2\]
\end{document}
```

$$
500 \text{ quả táo} \times 100 \text{ quả cam} = \text{Siuuu}^2
$$

## Thực hành: 

https://en.wikipedia.org/wiki/Divergence_of_the_sum_of_the_reciprocals_of_the_primes#Partial_sums (viết văn bản thông thường vào toán học).

