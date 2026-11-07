## Dàn ý: 

là gì ? được biểu diễn thành kí hiệu như thế nào ? đọc như nào ?  khi nào ? 

## Bài học: 

Các toán tử cơ bản: 

\+ Các dấu +, -, /, = có thể được nhập trực tiếp bàn phím. 
\+ Dấu $\times$ được viết ở LaTeX sẽ là 

```latex
\times
```

\+ Dấu $\cdot$ được viết ở LaTeX là 

```latex
\cdot
```

\+ Dấu $\div$ được viết ở LaTeX là 

```latex
\div
```

\+ Một số toán tử nhị phân (Binary Operators) 

```latex
\otimes, \oplus, \cup, \cap
```

$\otimes, \ \oplus, \ \cup, \ \cap$

\+ Một số toán tử quan hệ (Relation Operators)

Dấu <, > có thể được nhập trực tiếp trên bàn phím 

Dấu $\leq, \ \geq, \ \neq$

```latex
\leq, \geq, \neq
```

Dấu $\subset, \ \supset, \ \subseteq, \ \supseteq$

```latex
\subset, \supset, \subseteq, \supseteq
```

Dấu $\in, \ \notin$

```latex
\in, \notin
```

Dấu $\ \approx, \simeq, \ \cong, \ \equiv, \ \vee, \ \wedge, \ \perp$

```latex
\approx, \simeq, \cong, \equiv, \vee, \wedge, \perp
```

Dấu $\boxtimes, \Box$

```latex
\boxtimes, \Box
```

### Toán tử lượng giác 

```latex
\documentclass{article}
\begin{document}
\(\cos(x), \sin(x), \tan(x), \cot(x), ..vv..\)
\end{document}
```

$\cos(x), \ \sin(x), \ \tan(x), \ \cot(x), ..vv..$  

<div align="center">
<img src="LaTeX-Library-project-v1.0.0/Draft/draft img/trigonometry iceberg.jpg" alt = "trinogometry" width="80%" height="70%"> 
</div>

<center>Tảng băng chìm toán tử lượng giác</center>

---

### Toán tử hàm mũ 

. . . (định nghĩa hàm số mũ) 
```latex
\documentclass{article}
\begin{document}
\(\log(x)\)
\end{document}
```

$\log(x)$ 

Đối với một hàm cơ số $e$ mũ x ta có 

```latex
\documentclass{article}
\begin{document}
\(y = e^x\)
\end{document}
```

$y = e^x$ 

Ta thấy hằng số Euler $\mathrm{e}$ hơi nghiêng, để khắc phục điều này người dùng chỉ cần đặt hằng số đó vào lệnh `\mathrm`

```latex
\documentclass{article}
\begin{document}
\(y = \mathrm{e}^x\)
\end{document}
```

$y = \mathrm{e}^x$

Hàm  $y = \mathrm{e}^x$ của x này còn được viết tắt lại thành $y = \exp(x)$. Để viết kí hiệu $\exp$ trong LaTeX, người dùng chỉ cần thêm vào trước nó dấu `\`. 

```latex
\documentclass{article}
\begin{document}
\(y = \exp(x)\)
\end{document}
```

$y = \exp(x)$ 

### Mở rộng:

arguments of the maxima (viết tắt lại là argmax) . . . (? nó là gì nhỉ, trong lĩnh vực nào của toán học nhỉ)

Nếu viết thông thường trong LaTeX[^first]

```tex
\documentclass{article}

\usepackage{mathtools}

\begin{document}

\[
    \arg \max {}_S f \coloneqq \{x \in S : f(x) = \sup {}_S f\}
\]

\end{document}
```

Kết quả hiển thị: 

$$
    \arg \max {}_S f \coloneqq \{x \in S : f(x) = \sup {}_S f\}
$$

Ta thấy kí hiệu $\operatorname{argmax}$ không được viết dính liền. 

Để làm được điều này, ta sẽ sử dụng lệnh mới: 

```tex
\operatorname{}
```

Lệnh này giúp ta tạo một toán tử mới, nếu như toán tử ấy chưa được LaTeX định nghĩa sẵn, hoặc ở bất kì package nào khác. 

Ta sẽ sửa lại đoạn mã trên như sau: 

```tex
\documentclass{article}

\usepackage{mathtools} % để định nghĩa lệnh \coloneqq

\begin{document}

\[
    \operatorname{argmax} {}_S f \coloneqq \{x \in S : f(x) = \sup {}_S f\}
\]

\end{document}
```

Kết quả cho ra được lúc này sẽ là: 

$$
    \operatorname{argmax} {}_S f \coloneqq \{x \in S : f(x) = \sup {}_S f\}
$$

Nếu như ta không thêm cặp dấu ngoặc nhọn vào trước lệnh viết [chỉ số dưới](): 

```tex
\documentclass{article}

\usepackage{mathtools} % để định nghĩa lệnh \coloneqq

\begin{document}

\[
    \operatorname{argmax}_S f \coloneqq \{x \in S : f(x) = \sup _S f\}
\]

\end{document}
```

Ta sẽ thấy 

$$
    \operatorname{argmax}_S f \coloneqq \{x \in S : f(x) = \sup _S f\}
$$

. . . (nếu ta viết thông thường)

```tex
\documentclass{article}

\usepackage{mathtools} % để định nghĩa lệnh \coloneqq

\begin{document}

\[
    \operatorname{argmax}_S f \coloneqq 
    \operatorname{argmax}_{x \in S} f(x) \coloneqq 
    \{x \in S : f(s) \leq f(x) \text{ for all } s \in S\}
\]

\end{document}
```
$$
    \operatorname{argmax}_S f \coloneqq 
    \operatorname{argmax}_{x \in S} f(x) \coloneqq 
    \{x \in S : f(s) \leq f(x) \text{ for all } s \in S\}
$$

. . . (bằng cách sử dụng lệnh `\operatorname` ở trên và có thêm dấu *, cụ thể: 
```tex
\operatorname*{}
```
)

```tex
\documentclass{article}

\usepackage{mathtools} % để định nghĩa lệnh \coloneqq

\begin{document}

\[
    \operatorname{argmax}_S f \coloneqq 
    \operatorname*{argmax}_{x \in S} f(x) \coloneqq 
    \{x \in S : f(s) \leq f(x) \text{ for all } s \in S\}
\]

\end{document}
```

$$
    \operatorname{argmax}_S f \coloneqq 
    \operatorname*{argmax}_{x \in S} f(x) \coloneqq 
    \{x \in S : f(s) \leq f(x) \text{ for all } s \in S\}
$$

---

[^first]: Tham khảo từ trang wiki https://en.wikipedia.org/wiki/Arg_max 