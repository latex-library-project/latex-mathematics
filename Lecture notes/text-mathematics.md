## Bài học:

Ta đã tìm hiểu cách để chèn toán học vào cùng với văn bản thông thường ở bài học [mở đầu](/Lecture%20notes/Mở%20đầu.md). Vậy nếu ngược lại, làm sao để ta có thể chèn văn bản thông thường vào lệnh hoặc môi trường toán học ?

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

Để viết văn bản vào trong môi trường toán học ta sẽ sử dụng lệnh: 

```tex
\text{}
```

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