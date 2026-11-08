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

---

### Mở rộng:

Sẽ có một vài trường hợp một vài kí hiệu sẽ không được hệ thống cài đặt sẵn mặc định hay thông qua các package khác. Chẳng hạn, ta cùng nhau xem qua ví dụ công thức Leibniz để tính định thức sau: 

```tex 
\documentclass{article}

\begin{document}

\[
\det(A) = \sum_{\sigma \in S_n} sgn(\sigma) \prod_{k = 1}^{n} \left (a_{k\sigma(k)}\right )
\]

\end{document}
```

$$
\det(A) = \sum_{\sigma \in S_n} sgn(\sigma) \prod_{k = 1}^{n} \left (a_{k\sigma(k)}\right )
$$

Ở đây, ta thấy dấu của phép thế (được kí hiệu sgn) đang được để mặc định thông thường, nên sẽ bị in nghiêng. 


Vì LaTeX không cài đặt kí hiệu dấu của phép thế sẵn, cũng như là các package khác, mà thay vào đó ta sẽ thông qua lệnh mới là

```tex
\operatorname{}
```

Lệnh này giúp ta tạo một toán tử hoặc một kí hiệu toán học mới, nếu như toán tử hoặc kí hiệu toán học ấy chưa được LaTeX định nghĩa sẵn, hoặc ở bất kì package nào khác. 

Để sử dụng được lệnh `\operatorname{}`, ta cần phải khai báo package là **amsmath** hoặc package là **mathtools**. 

**Câu hỏi (toán học)**: Dấu của phép thế (sgn) có phải là một toán tử ? 

```tex
\documentclass{article}

\usepackage{amsmath}

\begin{document}

\[
\det(A) = \sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) \prod_{k = 1}^{n} \left (a_{k\sigma(k)}\right )
\]

\end{document}
```

$$
\det(A) = \sum_{\sigma \in S_n} \operatorname{sgn} (\sigma) \prod_{k = 1}^{n} \left (a_{k\sigma(k)}\right )
$$

Lệnh `\operatorname` này cũng giúp chúng ta viết toán tử sau đây một cách vô cùng đơn giản. 

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

Điều này cũng tương tự đối với toán tử là $\operatorname{argmin}$. 

---

### Hệ quả từ bài học mở rộng: 

Một cách khác để nhóm điều kiện của $\lim \sup$ (? cách đọc sao nhỉ)

. . . (từ ví dụ trên, ta thấy lệnh `operatorname*{}` này còn giúp chúng ta nhóm điều kiện lại chung với toán tử nếu viết tách biệt . . .)[^second]

```tex
\documentclass{article}

\usepackage{mathtools}

\begin{document}

\[
    \operatorname*{limsup}_{n \to \infty} x_n \coloneqq  
    \lim_{n \to \infty} \left(\sup_{m \geq n} x_n \right)
\]

\end{document}
```

$$
    \operatorname*{limsup}_{n \to \infty} x_n \coloneqq  
    \lim_{n \to \infty} \left(\sup_{m \geq n} x_n \right)
$$

Tuy vậy, để cho toán tử giới hạn (lim) và toán tử supremum (sup) không bị dính liền, ta sẽ sử dụng [lệnh khoảng cách trong chế độ toán học]() nhỏ nhất với giá trị dương là `\,`: 

```tex
\operatorname*{lim \, sup} . . . 
```

Ta viết đầy đủ lại đoạn mã trên: 

```tex
\documentclass{article}

\usepackage{mathtools}

\begin{document}

\[
    \operatorname*{lim \, sup}_{n \to \infty} x_n \coloneqq  
    \lim_{n \to \infty} \left(\sup_{m \geq n} x_n \right)
\]

\end{document}
```

$$
    \operatorname*{lim \, sup}_{n \to \infty} x_n \coloneqq  
    \lim_{n \to \infty} \left(\sup_{m \geq n} x_n \right)
$$


Tuy vậy thì điều này không cần thiết, vì toán tử limit superior (tạm dịch là giới hạn trên) và limit inferior (tạm dịch là giới hạn dưới) đã được LaTeX định nghĩa sẵn: 

```tex
\documentclass{article}

\usepackage{mathtools}

\begin{document}

\[
    \limsup_{n \to \infty} x_n \coloneqq  
    \lim_{n \to \infty} \left(\sup_{m \geq n} x_n \right)
\]

\end{document}
```

$$
    \limsup_{n \to \infty} x_n \coloneqq  
    \lim_{n \to \infty} \left(\sup_{m \geq n} x_n \right)
$$

nên là ta không cần phải sử dụng lệnh `\operatorname` trong trường hợp này. 

Để giúp người dùng có thể xác định được đâu là toán tử đã được latex định nghĩa sẵn hay chưa, người dùng có thể tham khảo qua hai bảng phân loại hai điều kiện đây ở phần tổng hợp [kí hiệu]() (? bài học nào đây).   

---

[^first]: Tham khảo từ trang wiki https://en.wikipedia.org/wiki/Arg_max 

[^second]: Tham khảo từ trang wiki https://en.wikipedia.org/wiki/Limit_inferior_and_limit_superior#Definition_for_sequences