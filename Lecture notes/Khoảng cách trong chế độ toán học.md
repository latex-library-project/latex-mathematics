(? . . . nên viết bài học khoảng cách giữa các từ trong văn bản thông thường (tiêu đề tạm thời để vậy) trước khi viết bài học này) 

Nếu ta nhấn phím **spcae** tạo khoảng cách các chữ cái thông thường trong từ if:

```latex
\documentclass[article]

\begin{document}

I   f

\end{document}
```

Kết quả cho ra được sẽ là: 

I  f

So với việc viết văn bản thông thường, khi ta nhấn phím **space** giữa biến x và y trong biểu thức $xy$ như đoạn mã sau 

```latex
\documentclass[article]

\begin{document}

\(x    y\)

\[
x    y
\]

\end{document}
```

$x    y$

$$
x   y 
$$


Kết quả cho ra được là biến x và y đều luôn tạo thành biểu thức $xy$. 


Khi người dùng viết toán học,  . . . (nêu vấn đề)

Để điều chỉnh khoảng cách giữa các biểu thức, toán tử . . . người dùng chỉ cần thêm lệnh ở bảng sau đây 

| Lệnh LaTeX | Mô tả                                                   | Ví dụ         |
| :--------- | :------------------------------------------------------ | ------------- |
| `\quad`    | = 18 mu                                                 | $a \quad b$   |
| `\qquad`   | $= 2 \cdot$`\quad` (= 36 mu)                            | $a \qquad b$  |
| `\enskip`  | $= \frac{1}{2} \cdot$`\quad` (= 9 mu)                   | $a \enskip b$ |
| `\,`       | $= \frac{3}{18} \cdot$`\quad` (= 3 mu)                  | $a \, b$      |
| `\:`       | $= \frac{4}{18} \cdot$`\quad` (= 4 mu)                  | $a \: b$      |
| `\;`       | $= \frac{5}{18} \cdot$`\quad` (= 5 mu)                  | $a \; b$      |
| `\!`       | $= \frac{-3}{18} \cdot$`\quad` (= -3 mu)                | $a \! b$      |
| `\`        | tương đương với khoảng trắng trong văn bản thông thường | $a \ b$       |

(Bảng tham khảo từ [Overleaf](https://www.overleaf.com/learn/latex/Spacing_in_math_mode#Spaces)) 

vào ngay bên cạnh . . . (? bên cạnh gì)

Với các [toán tử quan hệ]()  

Ví dụ về khoảng cách trong chế độ toán học với . . . 

. . . 

--- 

## Tài liệu tham khảo: 

\[1]: Tham khảo từ bài học Overleaf: https://www.overleaf.com/learn/latex/Spacing_in_math_mode 
