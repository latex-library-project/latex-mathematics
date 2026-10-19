## Bài học: 

### Môi trường `multline`: 

Sử dụng môi trường multline:  

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\begin{multline*}
p(x) = 3x^6 + 14x^5y + 590x^4y^2 + 19x^3y^3\\ 
- 12x^2y^4 - 12xy^5 + 2y^6 - a^3b^3
\end{multline*}
\end{document}
```

$$
\begin{multline*}
p(x) = 3x^6 + 14x^5y + 590x^4y^2 + 19x^3y^3\\ 
- 12x^2y^4 - 12xy^5 + 2y^6 - a^3b^3
\end{multline*}
$$ 

Một số cách khác để căn chỉnh khi viết phương trình dài: 

+ sử dụng môi trường split (như trong phần câu hỏi sau https://tex.stackexchange.com/questions/321796/how-to-handle-long-equation-in-latex).

### Môi trường `align` và `align*`

+ sử dụng môi trường align và align*. Bằng cách tận dụng thêm lệnh trong bài học [khoảng cách trong chế độ toán học](/Lecture%20notes%20math/Khoảng%20cách%20trong%20chế%20độ%20toán%20học.md)

```tex
\documentclass{article}
\usepackage{amsmath}
\begin{document}

\begin{align*}
p(x) = 3x^6 + 14x^5y + 590x^4y^2 + 19x^3y^3\\ 
     - 12x^2y^4 - 12xy^5 + 2y^6 - a^3b^3    
\end{align*}

\end{document}
```

### Môi trường `flalign`:  

Một cách để căn chỉnh phương trình dài bằng lệnh  `align` bằng cách kết hợp thêm lệnh `\qquad` trong đoạn mã trên, ta có thể sử dụng môi trường `flalign`. Để sử dụng được môi trường này, người dùng cần phải nhớ có khai báo package `amsmath`: 

```tex
\documentclass{article}
\usepackage{amsmath}
\begin{document}

\begin{flalign*}
p(x) = 3x^6 + 14x^5y + 590x^4y^2 + 19x^3y^3\\ 
- 12x^2y^4 - 12xy^5 + 2y^6 - a^3b^3
\end{flalign*}

\end{document}
```


## Câu hỏi: 

+ Sử dụng như thế nào ? 

+ Nên sử dụng khi nào ? 

+ Ưu va nhược của cách này là gì ? 