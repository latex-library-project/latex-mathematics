## Bài học

### Ma trận

Khai báo package 

```latex
\usepackage{amsmath}
```

Các môi trường sau đây phải được đặt viết trong các lệnh và môi trường **inline math**, **display math**. 

Sử dụng môi trường `bmatrix` để viết ma trận được bao quanh bởi dấu ngoặc vuong

```latex
\begin{bmatrix}
. . .
\end{bmatrix} 
```

Ví dụ với một ma trận $2 \times 2$ cơ bản sau: 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{bmatrix}
  1 & 2 \\
  3 & 4
\end{bmatrix}
\]
\end{document}
```


$$
\begin{bmatrix}
1 & 2 \\
3 & 4 
\end{bmatrix}
$$

Kí hiệu `&` dùng để phân cách (? sử dụng từ khác) các phân tử bên trong ma trận. Nếu ta không sử dụng dấu `&` ở hàng đầu tiên của ma trận

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{bmatrix}
  1  2 \\
  3 & 4
\end{bmatrix}
\]
\end{document}
```

$$
\begin{bmatrix}
  1  2 \\
  3 & 4
 \end{bmatrix}
$$

thì người dùng có thể thấy, phần tử đầu tiên của hàng đầu tiên của ma trận lúc này là 12 thay vì 1, còn hàng thứ hai lúc này bị bỏ trống thay vì là 2.  

Kí hiệu `\\` được dùng để xuống hàng mới. 

. . . 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{bmatrix}
  1 & 2 
  3 & 4
\end{bmatrix}
\]
\end{document}
```

Đoạn mã trên cũng tương đồng với đoạn mã sau 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{bmatrix}
  1 & 23 & 4
\end{bmatrix}
\]
\end{document}
```

Kết quả hiện thị ma trận trong trang tài liệu ở hai đoạn mã trên đều là như nhau: 

$$
\begin{bmatrix}
  1 & 2 
  3 & 4
 \end{bmatrix}
$$

Lúc này ta sẽ hiểu đây là một ma trận $1 \times 3$ (hay còn được gọi là một ma trận dòng). Có phần tử thứ nhất là 1, phần tử thứ 2 là 23 và cuối cùng phần tử thứ 3 là 4.  

Trong một số tài liệu toán học, khi viết các ma trận thay vì được bao quát bởi dấu ngoặc vuông, chúng lại được bao quát bởi dấu ngoặc tròn như hình dưới đây: 

(? Tìm ảnh minh họa cho ma trận được bao quát bởi dấu ngoặc tròn)

Để viết được ma trận được bao quanh bởi dấu ngoặc tròn ta sử dụng lệnh: 

```latex
\begin{pmatrix}
. . .
\end{pmatrix} 
```

(? trình bày cách ghi nhớ lệnh trên bằng cách phân biệt chữ cái đầu matrix là **b** và **p**) 

. . . 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{pmatrix}
  1 & 2 \\
  3 & 4
\end{pmatrix}
\]
\end{document}
```

$$
\begin{pmatrix}
  1 & 2 \\
  3 & 4
 \end{pmatrix}
$$

. . . (ma trận chuẩn (matrix norm))

```latex
\begin{Vmatrix}
. . .
\end{Vmatrix}
```

. . . 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{Vmatrix}
  1 & 2 \\
  3 & 4
\end{Vmatrix}
 \]
\end{document}
```

. . . 

$$
\begin{Vmatrix}
  1 & 2 \\
  3 & 4
\end{Vmatrix}
$$

Khi viết các phần tử bên trong ma trận là các số hữu tỉ, chẳng hạn như ở ví dụ sau: 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{bmatrix}
       \frac{5}{6} & \frac{1}{6} & 0           \\
       \frac{5}{6} & 0           & \frac{1}{6} \\
       0           & \frac{5}{6} & \frac{1}{6}
\end{bmatrix}
 \]
\end{document}
```

$$
\begin{bmatrix}
       \frac{5}{6} & \frac{1}{6} & 0           \\
       \frac{5}{6} & 0           & \frac{1}{6} \\
       0           & \frac{5}{6} & \frac{1}{6}
\end{bmatrix}
$$
Người dùng có thể thấy, tử số của phân số phần tử $a_{21} = \dfrac{5}{6}$ là 5, bị dính với mẫu số của phân số phần tử $a_{12} = \dfrac{5}{6}$. Và điều này cũng xảy ra tương tự ở phần tử $a_{33} = \dfrac{2}{3}$ với phần tử $a_{23} = \dfrac{2}{3}$. 

Để khắc phục được điều trên, người dùng chỉ cần viết dính liền, ngay sau dấu ngăn cách các hàng trong ma trận `\\` với dấu ngoặc vuông `[]`. 

Và bên trong dấu ngoặc vuông đó chứa thông số . . . .(? thông số gì) để co giãn hai phân tử cùng cột mà khác hàng . . .(? viết lại)

Chẳng hạn, người viết muốn . . . 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{bmatrix}
       \frac{5}{6} & \frac{1}{6} & 0           \\[0.5em]
       \frac{5}{6} & 0           & \frac{1}{6} \\[0.5em]
       0           & \frac{5}{6} & \frac{1}{6}
\end{bmatrix}
 \]
\end{document}
```


$$
\begin{bmatrix}
       \frac{5}{6} & \frac{1}{6} & 0           \\[0.5em]
       \frac{5}{6} & 0           & \frac{1}{6} \\[0.5em]
       0           & \frac{5}{6} & \frac{1}{6}
\end{bmatrix}
$$

Nếu như người dùng viết cách dấu `\\` và `[]`: (? viết chưa rõ ý)

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\begin{bmatrix}
       \frac{5}{6} & \frac{1}{6} & 0           \\ [0.5em]
       \frac{5}{6} & 0           & \frac{1}{6} \\[0.5em]
       0           & \frac{5}{6} & \frac{1}{6}
\end{bmatrix}
 \]
\end{document}
```

thì hệ thống sẽ hiểu `[]` . . . (? hiểu gì)

$$
\begin{bmatrix}
       \frac{5}{6} & \frac{1}{6} & 0           \\ [0.5em]
       \frac{5}{6} & 0           & \frac{1}{6} \\[0.5em]
       0           & \frac{5}{6} & \frac{1}{6}
\end{bmatrix}
$$

. . . .

Đối với gói `amsmath` để viết ma trận ở **inline math** ta sẽ sử dụng môi trường `smallmatrix`

```latex
\begin{smallmatrix}
. . . 
\end{smallmatrix}
```

Ta cần phải thêm . . . (? thêm gì)

Ví dụ: . . . 

```latex
To produce a small matrix suitable for use in text, there is a `smallmatrix` environment \(\left(\begin{smallmatrix}1 & 2 \\ 3 & 4\end{smallmatrix}\right)\) that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . . 
```


To produce a small matrix suitable for use in text, there is a `smallmatrix` environment $\left(\begin{smallmatrix}1 & 2 \\ 3 & 4\end{smallmatrix}\right)$ that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . . 

Cách này chỉ phù hợp với việc người dùng viết ma trận được bao quanh bởi dấu ngoặc tròn cơ bản. Trong trường hợp ma trận đó được kí hiệu là định thức, ma trận chuẩn thì . . . (? thì sao em nhỉ)

Để làm được điều này, trước tiên người dùng cần phải sử dụng gói `mathtools`.

Môi trường `bsmailmatrix` . . .

```latex
\begin{bsmailmatrix}
. . . 
\begin{bsmailmatrix}
```

Ví dụ: . . . 

```latex
To produce a small matrix suitable for use in text, there is a `smallmatrix` environment \(\begin{bsmallmatrix}1 & 2 \\ 3 & 4\end{bsmallmatrix}\) that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . .
```

To produce a small matrix suitable for use in text, there is a `smallmatrix` environment $\begin{bsmallmatrix}1 & 2 \\ 3 & 4\end{bsmallmatrix}$ that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . .

Môi trường `Bsmailmatrix` . . . 

```latex
\begin{Bsmailmatrix}
. . . 
\begin{Bsmailmatrix}
```

Ví dụ: . . .

```latex
To produce a small matrix suitable for use in text, there is a `smallmatrix` environment \(\begin{Bsmallmatrix}1 & 2 \\ 3 & 4\end{Bsmallmatrix}\) that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . .
```

To produce a small matrix suitable for use in text, there is a `smallmatrix` environment $\begin{Bsmallmatrix}1 & 2 \\ 3 & 4\end{Bsmallmatrix}$ that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . .

Môi trường `vsmailmatrix` . . . 

Ví dụ:  . . . 

```latex
To produce a small matrix suitable for use in text, there is a `smallmatrix` environment \(\begin{vsmallmatrix}1 & 2 \\ 3 & 4\end{vsmallmatrix}\) that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . .
```

To produce a small matrix suitable for use in text, there is a `smallmatrix` environment $\begin{vsmallmatrix}1 & 2 \\ 3 & 4\end{vsmallmatrix}$ that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . .

Môi trường `Vsmallmatrix` . . . 

Ví dụ: . . . 

```latex
To produce a small matrix suitable for use in text, there is a `smallmatrix` environment $\begin{Vsmallmatrix}1 & 2 \\ 3 & 4\end{Vsmallmatrix}$ that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . .
```

To produce a small matrix suitable for use in text, there is a `smallmatrix` environment $\begin{Vsmallmatrix}1 & 2 \\ 3 & 4\end{Vsmallmatrix}$ that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . .

Ta còn có thể thay cách thủ công . . . (? ở phần giới thiệu gói `amsmath`) . . . bằng môi trường `psmailmatrix` . . .

Ví dụ: . . . 

```latex
To produce a small matrix suitable for use in text, there is a `smallmatrix` environment $\begin{psmallmatrix}1 & 2 \\ 3 & 4\end{psmallmatrix}$ that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . .
```

To produce a small matrix suitable for use in text, there is a `smallmatrix` environment $\begin{psmallmatrix}1 & 2 \\ 3 & 4\end{psmallmatrix}$ that comes closer to fitting within a single text line than a normal matrix. This example was produced by . . . 

### Ma trận bổ sung 

Cho một hệ phương trình tuyến tính tổng quát . . . 

$$
. . . 
$$

Đưa về dạng ma trận ta được: 

$$
. . .
$$

. . . (trình bày ma trận hệ số (coefficient matrix), ma trận cột ẩn số, ma trận cột hệ số tự do)

. . . (chúng ta còn có thể biểu diễn dạng ma trận trên thành ma trận bổ sung (augmented matrix)) 

Để viết ma trận bổ sung, người dùng sẽ sử dụng gián tiếp thông qua môi trường `array`. 

Ví dụ . . . : Cho một hệ phương trình tuyến tính sau 

```latex
\begin{cases}
	x_1 + 2x_2 + 3x_3 = 4 \\[0.5em] 
	2x_1 + 3x_2 + 4x_3 = 5 \\[0.5em]
	3x_1 + 4x_2 + 5x_3 = 6
\end{cases}
```

$$
\begin{cases}
	x_1 + 2x_2 + 3x_3 = 4 \\[0.5em] 
	2x_1 + 3x_2 + 4x_3 = 5 \\[0.5em]
	3x_1 + 4x_2 + 5x_3 = 6
\end{cases}
$$

Ta viết gọn lại bằng ma trận bổ sung như sau: 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
\left[
\begin{array}{@{}ccc|c@{}}
2 & 3 & 4 & 5 \\ 
3 & 4 & 5 & 6 \\
4 & 5 & 6 & 7 
\end{array} 
\right]
\]
\end{document}
```

$$
\left[
\begin{array}{@{}ccc|c@{}}
1 & 2 & 3 & 4 \\ 
3 & 4 & 5 & 6 \\
4 & 5 & 6 & 7 
\end{array} 
\right] 
$$

Lệnh `@{}` được đặt hai bên . . . (? gì đó) trong dấu ngoặc nhọn, dùng để căn chỉnh hai dấu ngoặc vuông của ma trận bổ sung khi viết ở phần thảo LaTeX sao cho  .  .  . (? giúp chúng như thế nào)  

Nếu như người dùng không sử dụng lệnh `@{}`, thì ở trong trang tài liệu lúc này sẽ hiện thị một kết quả hoàn toàn khác:   

$$
\left[
\begin{array}{ccc|c}
1 & 2 & 3 & 4 \\ 
3 & 4 & 5 & 6 \\
4 & 5 & 6 & 7 
\end{array} 
\right] 
$$

### Pp khử Gauss - Jordan 

(? . . . . Giới thiệu phương pháp khử Gauss - Jordan) 

Ví dụ . . . : Cho một hệ ba phương trình ba ẩn sau: 

```latex
\[
\begin{cases}
    x + 2y -z = 3 \\[0.5em]
    2x + 5y + z = 10 \\[0.5em] 
    3x + 6y + 2z = 15 
\end{cases}
\]
```

$$
\begin{cases}
    x + 2y -z = 3 \\[0.5em]
    2x + 5y + z = 10 \\[0.5em] 
    3x + 6y + 2z = 15 
\end{cases}
$$

Viết lại dưới dạng ma trận bổ sung ta được: 

```latex
\[
\left[
\begin{array}{ccc|c}
    1 & 2 & -1 & 3 \\
    2 & 5 & 1 & 10 \\
    3 & 6 & 2 & 15 
\end{array}
\right]
\]
```

$$
\left[
\begin{array}{ccc|c}
    1 & 2 & -1 & 3 \\
    2 & 5 & 1 & 10 \\
    3 & 6 & 2 & 15 
\end{array}
\right]
$$

Sử dụng phương pháp khử Gauss - Jordan để tìm nghiệm hệ trên: 

```latex
\[
\left[
\begin{array}{ccc|c}
    1 & 2 & -1 & 3 \\
    2 & 5 & 1 & 10 \\
    3 & 6 & 2 & 15 
\end{array}
\right] 
\xrightarrow{\substack{R_2 \to R_2 - 2R_1 \\[0.3em] R_3 \to R_3 - 3R_1}}
\left[
\begin{array}{ccc|c}
    1 & 2 & -1 & 3 \\
    0 & 1 & 3 & 4 \\
    0 & 0 & 5 & 6 
\end{array}
\right] 
\xrightarrow{R_3 \to \dfrac{1}{5}R_3} 
\left[
\begin{array}{ccc|c}
    1 & 2 & -1 & 3 \\
    0 & 1 & 3 & 4 \\
    0 & 0 & 1 & \dfrac{6}{5} 
\end{array}
\right] 
\]

\[
\xrightarrow{\substack{R_2 \to R_2 - 3R_3 \\[0.3em] R_1 \to R_1 + R_3}} 
\left[
\begin{array}{ccc|c}
    1 & 2 & 0 & \dfrac{21}{5} \\[0.3em]
    0 & 1 & 0 & \dfrac{2}{5} \\[0.3em]
    0 & 0 & 1 & \dfrac{6}{5} 
\end{array}
\right] 
\xrightarrow{R_1 \to R_1 - 2R_2} 
\left[
\begin{array}{ccc|c}
    1 & 0 & 0 & \dfrac{17}{5} \\[0.3em]
    0 & 1 & 0 & \dfrac{2}{5} \\[0.3em]
    0 & 0 & 1 & \dfrac{6}{5} 
\end{array}
\right] 
\]
```

$$
\left[
\begin{array}{ccc|c}
    1 & 2 & -1 & 3 \\
    2 & 5 & 1 & 10 \\
    3 & 6 & 2 & 15 
\end{array}
\right] 
\xrightarrow{\substack{R_2 \to R_2 - 2R_1 \\[0.3em] R_3 \to R_3 - 3R_1}}
\left[
\begin{array}{ccc|c}
    1 & 2 & -1 & 3 \\
    0 & 1 & 3 & 4 \\
    0 & 0 & 5 & 6 
\end{array}
\right] 
\xrightarrow{R_3 \to \dfrac{1}{5}R_3} 
\left[
\begin{array}{ccc|c}
    1 & 2 & -1 & 3 \\
    0 & 1 & 3 & 4 \\
    0 & 0 & 1 & \dfrac{6}{5} 
\end{array}
\right] 
$$

$$
\xrightarrow{\substack{R_2 \to R_2 - 3R_3 \\[0.3em] R_1 \to R_1 + R_3}} 
\left[
\begin{array}{ccc|c}
    1 & 2 & 0 & \dfrac{21}{5} \\[0.3em]
    0 & 1 & 0 & \dfrac{2}{5} \\[0.3em]
    0 & 0 & 1 & \dfrac{6}{5} 
\end{array}
\right] 
\xrightarrow{R_1 \to R_1 - 2R_2} 
\left[
\begin{array}{ccc|c}
    1 & 0 & 0 & \dfrac{17}{5} \\[0.3em]
    0 & 1 & 0 & \dfrac{2}{5} \\[0.3em]
    0 & 0 & 1 & \dfrac{6}{5} 
\end{array}
\right] 
$$

Cách viết thứ hai . . . bằng cách sử dụng môi trường `align`

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\begin{align*}
\left[\begin{array}{ccc|c}
1 & 2 & -1 & 3 \\
2 & 5 & 1 & 10 \\
3 & 6 & 2 & 15 
\end{array}\right]
&\xrightarrow{\substack{R_2 \to R_2 - 2R_1 \\[0.2em] R_3 \to R_3 - 3R_1}}
\left[\begin{array}{ccc|c}
1 & 2 & -1 & 3 \\
0 & 1 & 3 & 4 \\
0 & 0 & 5 & 6 
\end{array}\right] \\[1em] % xuống hàng mới 
& \xrightarrow{R_3 \to \dfrac{1}{5}R_3} % Vô hàng
\left[\begin{array}{ccc|c}
1 & 2 & -1 & 3 \\
0 & 1 & 3 & 4 \\
0 & 0 & 1 & \frac{6}{5} 
\end{array}\right] \\[1em]
& \xrightarrow{\substack{R_2 \to R_2 - 3R_3 \\[0.3em] R_1 \to R_1 + R_3}} 
\left[
\begin{array}{ccc|c}
    1 & 2 & 0 & \frac{21}{5} \\[0.3em]
    0 & 1 & 0 & \frac{2}{5} \\[0.3em]
    0 & 0 & 1 & \frac{6}{5} 
\end{array}
\right] \\[1em]
& \xrightarrow{R_1 \to R_1 - 2R_2} 
\left[
\begin{array}{ccc|c}
    1 & 0 & 0 & \frac{17}{5} \\[0.3em]
    0 & 1 & 0 & \frac{2}{5} \\[0.3em]
    0 & 0 & 1 & \frac{6}{5} 
\end{array}
\right] 
\end{align*}
\end{document}
```

$$
\begin{align*}
\left[\begin{array}{ccc|c}
1 & 2 & -1 & 3 \\
2 & 5 & 1 & 10 \\
3 & 6 & 2 & 15 
\end{array}\right]
&\xrightarrow{\substack{R_2 \to R_2 - 2R_1 \\[0.2em] R_3 \to R_3 - 3R_1}}
\left[\begin{array}{ccc|c}
1 & 2 & -1 & 3 \\
0 & 1 & 3 & 4 \\
0 & 0 & 5 & 6 
\end{array}\right] \\[1em] % xuống hàng mới 
& \xrightarrow{R_3 \to \dfrac{1}{5}R_3} % Vô hàng
\left[\begin{array}{ccc|c}
1 & 2 & -1 & 3 \\
0 & 1 & 3 & 4 \\
0 & 0 & 1 & \frac{6}{5} 
\end{array}\right] \\[1em]
& \xrightarrow{\substack{R_2 \to R_2 - 3R_3 \\[0.3em] R_1 \to R_1 + R_3}} 
\left[
\begin{array}{ccc|c}
    1 & 2 & 0 & \frac{21}{5} \\[0.3em]
    0 & 1 & 0 & \frac{2}{5} \\[0.3em]
    0 & 0 & 1 & \frac{6}{5} 
\end{array}
\right] \\[1em]
& \xrightarrow{R_1 \to R_1 - 2R_2} 
\left[
\begin{array}{ccc|c}
    1 & 0 & 0 & \frac{17}{5} \\[0.3em]
    0 & 1 & 0 & \frac{2}{5} \\[0.3em]
    0 & 0 & 1 & \frac{6}{5} 
\end{array}
\right] 
\end{align*}
$$

Vậy 

$$
(x, y, z) = \left(\frac{17}{5}, \frac{2}{5}, \frac{6}{5}\right)
$$


<div align="center">
	
<img src="./draft img/Gauss-Jordan.jpg" alt="Gauss-Jordan">

Hai nhà toán học người Đức là Carl Gauss (trái) và Wilhelm Jordan (phải) (không nền nhầm lẫn với hai nhà toán học cùng tên khác là Camille Jordan và Pascual Jordan) 

</div>