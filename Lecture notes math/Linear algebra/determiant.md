## Định thức của ma trận 

### Công thức Leibniz

. . . (định thức của một ma trận) 

```latex
\begin{vmatrix}
. . .
\end{vmatrix}
```

. . . 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{vmatrix}
  1 & 2 \\
  3 & 4
\end{vmatrix}
 \]
\end{document}
```

. . . 

$$
\begin{vmatrix}
  1 & 2 \\
  3 & 4
 \end{vmatrix}
$$

Ngoài ra, định thức của một ma trận vuông $A$ cấp $n$ còn được kí hiệu là $\det(A)$. 

Ví dụ . . .  về công thức tính định thức tổng quát của một ma trân vuông $A$ cấp $n$ được chứng minh bởi nhà toán học Leibniz  

```latex
\documentclass{article}
\begin{document}
\[det(A) = \sum_{\sigma \in S_n} sgn(\sigma) \prod_{k = 1}^{n} \left (a_{k\sigma(k)}\right )\]
\end{document}
```

. . . 

$$det(A) = \sum_{\sigma \in S_n} sgn(\sigma) \prod_{k = 1}^{n} \left (a_{k\sigma(k)}\right )$$

Ta thấy hai kí hiệu từ công thức trên là "det" và "sgn" bị nghiêng. LaTeX đã định nghĩa lệnh

```latex
\det
```

dùng để viết kí hiệu định thức. 

Còn kí hiệu "sgn", người dùng cần phải viết chúng vào trong dấu ngoặc nhọn của lệnh `\operatorname`

```latex
\operatorname{sgn}
```

Từ những điều ở trên, đoạn mã lúc này được sửa có được như sau

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[\det(A) = \sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) \prod_{k = 1}^{n} \left (a_{k\sigma(k)}\right)\]
\end{document}
```

$$
\det(A) = \sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) \prod_{k = 1}^{n} \left (a_{k\sigma(k)}\right)
$$

### Công thức khai triển Laplace 

Một cách khác để tính định thức đó là khai triển Laplace . . . (? không cần nói quá rõ chi tiết lý thuyết, những vẫn cần giới thiệu sơ qua)

. . . (? công thức khai triển Laplace tổng quát theo hàng)

```latex
\[
\det(A) = \sum_{1 \leq i_1 < \dots < i_k \leq k} ((-1)^{i_1 + \dots i_k + j_1 + \dots + j_k} \cdot \overline{D}_{i_1 \dots i_k}^{j_1 \dots j_k} \cdot D_{i_1 \cdots i_k}^{j_1 \cdots j_k})
\]
```

$$
\det(A) = \sum_{1 \leq i_1 < \dots < i_k \leq k} ((-1)^{i_1 + \dots i_k + j_1 + \dots + j_k} \cdot \overline{D}_{i_1 \dots i_k}^{j_1 \dots j_k} \cdot D_{i_1 \cdots i_k}^{j_1 \cdots j_k})
$$
Người dùng có thể thấy, có một khoảng trống giữa lệnh `\sum` hai bên. Vì điều kiện của phương trình quá lớn dẫn đến việc hệ thống tự động co giãn các biểu thức hai bên đầu điều kiện. (? . . . kiểm tra lại phần mô tả này)

Để khắc phục được vấn đề này, trước tiên người dùng cần phải khai báo package `mathtools`. Sau đó, người dùng chỉ cần nhóm điều kiện ở chỉ số dưới lệnh `\sum` này lại vào trong dấu ngoặc nhọn của lệnh `\mathclap`. Cụ thể: 

```latex
\mathclap{1 \leq i_1 < \dots < i_k \leq k}
```

Từ đây, ta viết lại công thức khai triển Laplace tổng quát theo theo hàng như sau: 

```latex
\[
\det(A) = \sum_{\mathclap{1 \leq i_1 < \dots < i_k \leq k}} ((-1)^{i_1 + \dots i_k + j_1 + \dots + j_k} \cdot \overline{D}_{i_1 \dots i_k}^{j_1 \dots j_k} \cdot D_{i_1 \cdots i_k}^{j_1 \cdots j_k})
\]
```

Kết quả hiện thị lúc này,  . . . (? lúc này sẽ ra làm sao)

$$
    \det(A) = \sum_{\mathclap{1 \leq i_1 < \dots < i_k \leq k}} ((-1)^{i_1 + \dots i_k + j_1 + \dots + j_k} \cdot \overline{D}_{i_1 \dots i_k}^{j_1 \dots j_k} \cdot D_{i_1 \cdots i_k}^{j_1 \cdots j_k})
$$