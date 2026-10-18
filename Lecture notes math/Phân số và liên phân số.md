## Phân số 

Để viết phân số ta sử dụng lệnh 

```latex
\frac{a}{b}
```

Ví dụ phân số ở **inline math** 

```latex
\(\frac{1}{2}\)
```

$\frac{a}{b}$

Ví dụ phân số ở **display math** 

```latex
\[\frac{1}{2}\]
```

$$
\frac{1}{2}
$$

Khai báo package: 

```latex
\usepackage{amsmath}
```

Lệnh `\tfrac` này được dùng để thu nhỏ lại phân số khi viết phân số ở **display math**

```latex
\[\tfrac{1}{2}\]
```

$$\tfrac{1}{2}$$

Lệnh `\dfrac` này được dùng để phóng to phân số khi viết phân số ở **inline math**

```latex
\(\dfrac{1}{2}\)
```

$\dfrac{1}{2}$


Để viết được hỗn số ta chỉ cần viết số nguyên đó đứng trước lệnh viết phân số: 

```latex
\[5 \frac{1}{2} = \frac{11}{2}\]
```


$$
5 \frac{1}{2} = \frac{11}{2}
$$

Một cách khác để viết phân số mà người dùng thường hay thấy ở các công thức nấu ăn (? đại loại những vấn đề như thế)

```latex
\(^1/_2\)
```

$^1/_2$ 

Người dùng có thể khai báo package 

```latex
\usepackage{xfrac}
```

rồi sau đó sử dụng lệnh 

```latex
\sfrac{}{}
```

để viết lại $^1/_2$. 

```latex
\documentclass{article}
\usepackage{xfrac} 
\begin{document}
 $\sfrac{1}{2}$ 
\end{document}
```

---

## Liên phân số (? Ktr lại thuật ngữ)

(? giới thiệu một chút liên phân số là gì ? được biểu diễn như thê nào ? Giới thiệu cách viết liên phân số trên giấy trắng trước, rồi từ đó áp dụng chúng vào việc viết liên phân số trên soạn thảo LaTeX . . .)

Để viết được liên phân số, trước tiên người dùng hãy nhớ phải khai báo package `amsmath`. 

. . . (? viết nối tiếp phần trên)

Liên phân số cơ bản: 

```latex
\documentclass{article}

\usepackage[utf8]{vietnam}

\usepackage{amsmath}

\begin{document}

\[
  x = a_0 + \cfrac{1}{a_1 
          + \cfrac{1}{a_2 
          + \cfrac{1}{a_3 + \cfrac{1}{a_4}}}}
\]

\end{document}
```

Kết quả: 

$$
  x = a_0 + \cfrac{1}{a_1 
          + \cfrac{1}{a_2 
          + \cfrac{1}{a_3 + \cfrac{1}{a_4} } } }
$$

Các lệnh này phải được đặt vào trong lệnh hoặc môi trường viết toán học ở chế độ **display math**. 

>[!NOTE]
>Không nên viết liên phân số ở chế độ ***inline math** . . . (? nguyên nhân vì sao )

Ví dụ về liên phân số Rogers – Ramanujan . . . (? thuộc lĩnh vực gì của toán học, nó đang nói về điều gì)[^2]

```latex
\documentclass{article}

\usepackage[utf8]{vietnam}

\usepackage{amsmath}

\begin{document}

\begin{equation}
       S(q) =  -R(-q) = \cfrac{q^{1/5}}{1 + 
           \cfrac{q}{1 + 
           \cfrac{q^2}{1 + 
           \cfrac{q^3}{1+ \cdots}}}}, \quad |q| < 1 
\end{equation}

hoặc cũng có thể viết lại thành: 

\begin{equation}
        R(q) = \cfrac{q^{1/5}}{1 + 
           \cfrac{q}{1 - 
           \cfrac{q^2}{1 - 
           \cfrac{q^3}{1 - \cdots}}}}, \quad |q| < 1 
\end{equation}

\end{document}
```

Kết quả: 

$$
       S(q) =  -R(-q) = \cfrac{q^{1/5}}{1 + 
           \cfrac{q}{1 + 
           \cfrac{q^2}{1 + 
           \cfrac{q^3}{1+ \cdots}}}}, \quad |q| < 1 
$$

hoặc

$$
\begin{equation}
        R(q) = \cfrac{q^{1/5}}{1 + 
           \cfrac{q}{1 - 
           \cfrac{q^2}{1 - 
           \cfrac{q^3}{1 - \cdots}}}}, \quad |q| < 1 
\end{equation}
$$

<div align="center">
<img src="LaTeX-Library-project-v1.0.0/Draft/draft img/Rogers–Ramanujan.jpg" alt="Rogers–Ramanujan">
</div>

<center>Nhà toán học người Anh   
Leonard James Rogers và nhà toán người Ấn Độ Srinivasa Ramanujan</center> 

