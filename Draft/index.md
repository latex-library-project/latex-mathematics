Nơi đây là nháp cho các bài học toán mà mình chưa viết vào bài học chính, vì thiếu sót hay chưa biết phải kết nối chung với phần chính như thế nào. 

## Gói `mathtools` 

. . . 

---

## Bổ sung bài học định nghĩa, định lý, ...vv..

(? . . .nêu nguyên nhân, giải thích vì sao)

(? . . . đi tìm một ví dụ mới sau)

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} 
% . . .
\usepackage{amssymb}

%  . . .
\theoremstyle{plain}
\newtheorem{proposition}{Mệnh đề}[section]

\begin{document}

\begin{proposition}
	\begin{enumerate}
	    \item Nếu \(a, b \in \mathbb{Z_+}\) là hai số nguyên dương nguyên tố cùng nhau thì ta có \(\phi(ab) = \phi(a)\phi(b)\)
	    \item Nếu \(n = p^m\) là lũy thừa bậc \(m\) của một số nguyên tố \(p\) thì ta có
	    \[
	        \phi(p^m) = (p-1)p^{m-1}
	    \]
	    \item Nếu \(n = p_1^{m_1} \dots p_r^{m_r}\) là lũy thừa bậc \(m\) của một số nguyên tố \(p\) thì ta có
	    \[
	        \phi(p^m) = \prod_{i = 1}^r (p_i - 1)p_i^{m_1 - 1}
	    \]
	\end{enumerate}
\end{proposition}

\end{document}
```


Để khắc phục được điều có hai cách cơ bản sau: 

**Cách 1**: Sử dụng lệnh `\hfill` được đặt bên trong môi trường `proposition` mà ta vừa định nghĩa và trước môi trường `enumerate` trên (? giải thích thêm lệnh `\hfill` này, tham khảo ở bài học đây https://www.overleaf.com/learn/latex/Line_breaks_and_blank_spaces):

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} 
% . . .
\usepackage{amssymb}

%  . . .
\theoremstyle{plain}
\newtheorem{proposition}{Mệnh đề}[section]

\begin{document}

\begin{proposition} \hfill
	\begin{enumerate}
	    \item Nếu \(a, b \in \mathbb{Z_+}\) là hai số nguyên dương nguyên tố cùng nhau thì ta có \(\phi(ab) = \phi(a)\phi(b)\)
	    \item Nếu \(n = p^m\) là lũy thừa bậc \(m\) của một số nguyên tố \(p\) thì ta có
	    \[
	        \phi(p^m) = (p-1)p^{m-1}
	    \]
	    \item Nếu \(n = p_1^{m_1} \dots p_r^{m_r}\) là lũy thừa bậc \(m\) của một số nguyên tố \(p\) thì ta có
	    \[
	        \phi(p^m) = \prod_{i = 1}^r (p_i - 1)p_i^{m_1 - 1}
	    \]
	\end{enumerate}
\end{proposition}

\end{document}
```


**Cách 2**: Thay lệnh `\hfill` ở **cách 1** bằng lệnh mới `\leavemode` . . . (? giải thích thêm lệnh này) 

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} 
% . . .
\usepackage{amssymb}

%  . . .
\theoremstyle{plain}
\newtheorem{proposition}{Mệnh đề}[section]

\begin{document}

\begin{proposition} \leavevmode % Đẩy item 1 xuống 
	\begin{enumerate}
	    \item Nếu \(a, b \in \mathbb{Z_+}\) là hai số nguyên dương nguyên tố cùng nhau thì ta có \(\phi(ab) = \phi(a)\phi(b)\)
	    \item Nếu \(n = p^m\) là lũy thừa bậc \(m\) của một số nguyên tố \(p\) thì ta có
	    \[
	        \phi(p^m) = (p-1)p^{m-1}
	    \]
	    \item Nếu \(n = p_1^{m_1} \dots p_r^{m_r}\) là lũy thừa bậc \(m\) của một số nguyên tố \(p\) thì ta có
	    \[
	        \phi(p^m) = \prod_{i = 1}^r (p_i - 1)p_i^{m_1 - 1}
	    \]
	\end{enumerate}
\end{proposition}

\end{document}
```

---

##  Bổ sung bài học dấu ngoặc 

. . . 

```latex
\big( \Big( \bigg( \Bigg( 
```

$\big( \Big( \bigg( \Bigg($ 

```latex
\big) \Big) \bigg) \Bigg) 
```

$\big) \Big) \bigg) \Bigg)$

. . .  (? đang viết dang dở ở phần lecture notes)

Khi viết tập hợp các số hữu tỉ $\mathbb{Q}$ được biểu diễn bằng cách chỉ rõ tính chất đặc trưng của mỗi phần tử:  

```latex
\documentclass{article}
\usepackage{amssymb}
\begin{document}
\[\mathbb{Q} = \left\{\frac{a}{b}|a, b \in \mathbb{Z}, b \ne 0 \right\}\]
\end{document}
```

$$\mathbb{Q} = \left\{\frac{a}{b}|a, b \in \mathbb{Z}, b \ne 0 \right\}$$

Người dùng có thể thấy rằng, tuy hai bên dấu ngoặc nhọn đã được . . . (? điều gì tự động căn chỉnh) tự động căn chỉnh bởi hai lệnh lần lượt là `\left` và `\right`, nhưng [kí hiệu]() `|` không được tự động co giãn sao cho phù hợp với kích thước chiều cao của phân số $\dfrac{a}{b}$.  

Để khắc phục được điều này, người dùng chỉ cần thêm lệnh 

```latex
\middle
```

vào trước dấu `|` đó. 

```latex
\documentclass{article}
\usepackage{amssymb}
\begin{document}
\[\mathbb{Q} = \left\{\frac{a}{b} \middle|a, b \in \mathbb{Z}, b \ne 0 \right\}\]
\end{document}
```

$$\mathbb{Q} = \left\{\frac{a}{b} \middle|a, b \in \mathbb{Z}, b \ne 0 \right\}$$

Lệnh `\middle` này chỉ được sử dụng trong việc giúp các kí hiệu nhằm mục đích phân cách . . . (?) có thể được tự động co giãn chiêu cao sao cho phù hợp, vừa vặn kích thước với cặp dấu ngoặc bao quanh các phân số (như ở ví dụ trên), tích phân, tổng chuỗi, ma trận, căn thức, ..vv.. 

>[!WARNING]
>Lệnh `\middle` không thể được hoạt động một cách độc lập.  Để sử dụng được lệnh này, chúng cần được đặt vào trong hai lệnh là `\left` và `\right`. Nếu không, thì hệ thống sẽ báo lỗi **Extra \middle.**  

Giả sử, nếu ta bỏ hai lệnh `\left` và `\right` ở hai bên dấu ngoặc nhọn: 
 
```latex
\documentclass{article}
\usepackage{amssymb}
\begin{document}
\[\mathbb{Q} = \{\frac{a}{b} \middle|a, b \in \mathbb{Z}, b \ne 0\]
\end{document}
```

(? Ảnh báo lỗi)

>[!WARNING]
> Ngay sau lệnh `\middle` là phải có các kí hiệu có khả năng co giãn với chiều cao tương ứng . . .(? với gì đó). Nếu không, hệ thống sẽ báo lỗi **Missing delimiter (. inserted).**

Nếu người dùng thay kí hiệu `|` bằng kí hiệu nằm ngang như $\rightarrow$ (? chắc phải làm một ví dụ mới)

```latex
\documentclass{article}
\usepackage{amssymb}
\begin{document}
\[\mathbb{Q} = \left\{\frac{a}{b} \middle \rightarrow a, b \in \mathbb{Z}, b \ne 0 \right\}\]
\end{document}
```

$$
\mathbb{Q} = \left\{\frac{a}{b} \middle \rightarrow a, b \in \mathbb{Z}, b \ne 0 \right\} 
$$

Việc người viết thay kí hiệu `|` bằng $\rightarrow$ ở ví dụ này không thật sự có ý nghĩa về mặt toán học, tuy vậy điều người viết muốn trình bày là ở chú ý . . . (? viết như c), người dùng có thể thấy các kí hiệu nằm ngang như $\rightarrow$ sẽ bị hệ thống lỗi. (? trình bày lại) 

---

## Bổ sung bài học viết phương trình toán học

Người dùng có thể thay đổi số thứ tự nằm cạnh phương trình toán học, bằng cách sử dụng lệnh: 

```latex
\tag
```

được đặt bên trong môi trường `equation`. 

. . . .(? giới thiệu thêm về lệnh `\tag`)

Lệnh này được định nghĩa bên trong package `amsmath`, nên người dùng nhớ hãy kiểm tra xem mình đã khai báo package này hay chưa, nếu không hệ thống sẽ báo lỗi **Undefined control sequence**. 

Ví dụ: . . . (? tìm ví dụ và giải thích ví dụ lại sau)

```latex
\documentclass{article}

\usepackage{amsmath}

\begin{document}

\begin{equation} \tag{*}
    1 + 1 = 2
    \label{eq:*}
\end{equation}

\end{document}
```

---

## Tập hợp các kí hiệu có thể được nhập trực tiếp trên bàn phím 

```latex
+ - = ! / ( ) [ ] < > | ' : * 
```

$+ \ - \ = \ ! \ / \ ( \ ) \ [ \ ] \ < \ > \ | \ ' \ : \ *$  

---

## Đơn vị Angstrom 

```latex
\(\mathring{A}\)
```

$\mathring{A}$ 

---

## Sai số (cũng ko hẳn)

```latex
\(a \pm b\)
```

$a \pm b$  

Hai nghiệm phân biệt của một phương trình bậc hai một ẩn, với $\Delta > 0$ 

$$
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
$$

? . . . (dấu dưới đây là dấu gì nhỉ)

```latex
\(a \mp b\)
```

$a \mp b$

--- 

## Các dấu chấm dài trong LaTex

Các dấu chấm này được sử dụng cả trong văn bản thông thường, lẫn trong văn bản toán học. 

| . . .            | Lệnh           |
| :--------------- | -------------- |
| a $\dots$ b      | `\dots`        |
| a $\cdots$ b     | `\cdots`       |
| a $\vdots$ b     | `\vdots`       |
| a $\ddots$ b     | `\ddots`       |

Ở bảng . . . (số bảng ...) trên, chỉ riêng dấu ba chấm "$\dots$" là không cần nhất thiết được đặt vào các lệnh và môi trường viết chế độ toán học. Còn lại là bắt buộc phải đặt chúng vào trong các lệnh, môi trường viết toán học, nếu không thì hệ thống sẽ báo lỗi **Missing $ inserted.** 

Ví dụ: 

. . . (ví dụ với hai dấu ba chấm đầu tiên) 

. . . (giới thiệu dấu $\vdots$) 

Ví dụ: Dấu $\vdots$ thường được thấy nhiều ở việc người dùng sử dụng chúng để viết một ma trận tổng quát có kích thước $m \times n$. 

. . . (ma trận tổng quát)

Ngoài ra dấu $\vdots$ còn được sử dụng để làm quan hệ chia hết giữa hai số. 

Ví dụ: Với bổ đề Euclid trong lý thuyết số  

Bổ đề Euclid: Cho  $a, b \in \mathbb{N}$ và $p \in \mathbb{P}$: 

Nếu $p \ \vdots \ (a \cdot b)$, thì $p \ \vdots \ a$ hoặc $p \ \vdots \ b$. 

Tuy vậy, đôi khi . . . thường sử dụng dấu $|$ để biểu diễn quan hệ chia hết giữa hai số. 

Đọc thêm ở . . . (? phần viết lý thuyết số cơ bản trên) 

. . . (giới thiệu dấu `\hdotsfor{n}`) 

Dấu này được sử dụng chính chỉ trong việc viết . . . (? dùng cho điều gì cơ)

. . . . (? giải thích lệnh này) 

---

## Viết văn bản trong chế độ toán học 

Đã viết một phần bên [[Lecture notes]].  

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

Chỉnh sửa lại ở phần [[Lecture notes]] phần ví dụ mở đầu. [^1]

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

. . . (Hướng dẫn sử dụng lệnh `\text`) 

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



--- 

## In đậm chữ cái Hy Lạp

Để in đậm chữ cái Hy Lạp, trước tiên người dùng cần phải khai báo gói `bm`

```latex
\usepackage{bm}
```

Sau đó, người dùng chỉ cần viết các chữ cái Hy Lạp vào trong dấu ngoặc nhọn của lệnh `\bm`. 

```latex
\bm
```

Lệnh này chỉ được sử dụng bên trong lệnh, môi trường viết toán học. 

Ví dụ: . . . 

```latex
\(\bm{\alpha}\)
```

Nếu như người dùng không thích khai báo package, mà muốn sử dụng một lệnh duy nhất để in đậm các chữ cái Hy Lạp, thì sử dụng qua lệnh: 

```latex
\boldsymbol{}
```

Ví dụ: . . . 

```latex
\(\boldsymbol{\alpha}\)
```

---

## Một số phông chữ trong toán học 

Phông chữ toán học thông thường: 

```latex
\[ABC \ abc \ 123\]
```

$$ABC \ abc \ 123$$

Để các chữ cái toán học không bị in nghiêng như trên sử dụng lệnh `\mathrm`: 

```latex
\[\mathrm{ABC} \ \mathrm{abc} \ 123\]
```

$$\mathrm{ABC} \ \mathrm{abc} \ 123$$

Để các số được in nghiêng ta sử dụng lệnh `\mathit`: 

```latex
\[\mathit{ABC} \ \mathit{abc} \ \mathit{123}\]
```

$$\mathit{ABC} \ \mathit{abc} \ \mathit{123}$$

Để in đậm các cái toán học ta sử dụng lệnh `\mathbf`: 

```latex
\[\mathbf{ABC} \ \mathbf{abc} \ \mathbf{123}\]
```

$$\mathbf{ABC} \ \mathbf{abc} \ \mathbf{123}$$

Để . . . 

```latex
\[\mathsf{ABC} \ \mathsf{abc} \ \mathsf{123}\]
```

$$\mathsf{ABC} \ \mathsf{abc} \ \mathsf{123}$$

Để . . 

```latex
\[\mathtt{ABC} \ \mathtt{abc} \ \mathtt{123}\]
```

$$\mathtt{ABC} \ \mathtt{abc} \ \mathtt{123}$$

Để . . .

```latex
\[\mathcal{ABCDEF}\]
```

$$
\mathcal{ABCDEF}
$$
Để viết các tập số như tập tự nhiên $\mathbb{N}$, ..vv.. rước tiên ta cần phải khai báo package là `amssymb` hoặc `amsfonts`. Sau đó sử dụng lệnh `\mathbb`:  

```latex
\[\mathbb{NPZQRC}\]
```

$$
\mathbb{NPZQRC}
$$

Để viết các tập số như tập tự nhiên $\mathbb{N}$, ..vv.. rước tiên ta cần phải khai báo package là `amssymb` hoặc `amsfonts`. Sau đó sử dụng lệnh `\mathfrak`: 

```latex
\[\mathfrak{ABC} \ \mathfrak{abc} \ \mathfrak{123}\]
```

$$\mathfrak{ABC} \ \mathfrak{abc} \ \mathfrak{123}$$

Để . . ., trước tiên ta cần phải khai báo package là `mathrsfs`. Sau đó sử dụng lệnh `\mathscr`: 

```latex
\[\mathscr{ABCDEF}\] 
```

$$
\mathscr{ABCDEF} 
$$
--- 

## Viết phương trình theo mục lục (đặt tiêu đề lại)

Câu hỏi 1: Đối với chỉ riêng **section**. 

Trước tiên, người dùng cần phải khai báo package `amsmath`, sau đó chỉ cần chèn lệnh

```latex
\numberwithin{}{}
```

ở trước môi trường `equation`, . . . (? còn môi trường nào nữa ko)

```latex

```

Câu hỏi 2: Đối với việc có cả subsection bên trong cả section.  



--- 

## Chưa phân loại (tổng hợp đại trước)

Nơi đây chứa tạp nhám các loại toán học, sau đó mới phân loại sau. 

Tổng hợp tại đây: https://www.overleaf.com/read/cvrzxtfnpxvk#5bc02f 

---

[^1]: Tài liệu tham khảo hàm Dirichlet: https://mathworld.wolfram.com/DirichletFunction.html

[^2]: Nguồn tham khảo liên phân số Roger-Ramanujan: https://arxiv.org/pdf/2512.19952 
