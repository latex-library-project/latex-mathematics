(? vì sao đôi khi ta cần màu trong công thức toán học) 

Để viết các kí hiệu toán học có màu, người dùng có thể sử dụng lệnh `\textcolor` ở bài học [màu chữ]() hoặc cũng có thể thay thế lệnh đó bằng một lệnh mới sau

```latex
\mathcolor{color}{text}
```

nhằm phân biệt việc sắp màu chữ cho văn bản thông thường và văn bản toán học. 

Tương tự như lệnh `textcolor`, người dùng có thể sử dụng các màu mặc định hoặc mở rộng các màu khác ngoài 19 màu cơ bản như đã nêu ở bài học [màu chữ]() cho lệnh `\mathcolor`.   

Ví dụ về màu trong toán học  với phương trình Navier - Stokes . . . (? ptr này mô tả điều gì)

```latex
\documentclass{article}

% 
\usepackage[utf8]{vietnam}

% 
\usepackage{xcolor}

% 
\usepackage{amsmath}
\begin{document}
Phương trình Navier - Stokes:
\[
    \mathcolor{blue}{\rho} \left(\mathcolor{green}{\frac{\partial v}{\partial t} + (v \cdot \nabla) v} \right) = \mathcolor{red}{-\nabla p + \mu \nabla^2 v}
\]

trong đó: 
\begin{itemize}
    \item \(\mathcolor{blue}{\rho}\) là khối lượng chất lưu trên một đơn vị thể tích (hay mật độ của chất lưu)
    \item \(\mathcolor{green}{v}\) là vận tốc của dòng chảy
    \item \(\mathcolor{green}{\dfrac{\partial v}{\partial t} + (v \cdot \nabla) v}\) biểu thị gia tốc của dòng chảy 
    \item \(\mathcolor{red}{p}\): áp suất, \(\mathcolor{red}{-\nabla p}\) mô tả ứng suất cắt (shear stress) 
    \item \(\mathcolor{red}{\mu}\): là hệ số nhớt, đặc trưng cho độ nhớt (độ cản trở) (viscosity) của chất lỏng.
\end{itemize} 
\end{document}
```

$$
    \textcolor{blue}{\rho} \left(\textcolor{green}{\frac{\partial v}{\partial t} + (v \cdot \nabla) v} \right) = \textcolor{red}{-\nabla p + \mu \nabla^2 v}
$$

Mặc dù chức năng của hai lệnh này gần như là giống nhau, nhưng điểm khác biệt giữa lệnh `\textcolor` và `\mathcolor` là lệnh `\mathcolor` chỉ có thể được sử dụng khi được đặt vào bên trong lệnh, môi trường viết toán học. 

Chẳng hạn, nếu ở đoạn mã dòng thứ . . ., nếu như người dùng viết lệnh `\mathcolor` không được đặt vào bên trong lệnh `\(\)` để viết **inline math**, thì hệ thống sẽ báo lỗi . . . (? lỗi gì e nhỉ)

```latex
. . . (đoạn mã mà lệnh \mathcolor không được đặt bên trong \(\))
```

Trong khi lệnh `\textcolor` có thể được tùy ý sử dụng thoải mái dù là ở văn bản thông thường hay văn bản toán học. 

```latex
\documentclass{article}

% 
\usepackage[utf8]{vietnam}

% 
\usepackage{xcolor}

% 
\usepackage{amsmath}
\begin{document}
Phương trình Navier - Stokes:
\[
    \textcolor{blue}{\rho} \left(\textcolor{green}{\frac{\partial v}{\partial t} + (v \cdot \nabla) v} \right) = \textcolor{red}{-\nabla p + \mu \nabla^2 v}
\]

trong đó: 
\begin{itemize}
    \item \(\textcolor{blue}{\rho}\) là khối lượng chất lưu trên một đơn vị thể tích (hay mật độ của chất lưu)
    \item \(\textcolor{green}{v}\) là vận tốc của dòng chảy
    \item \(\textcolor{green}{\dfrac{\partial v}{\partial t} + (v \cdot \nabla) v}\) biểu thị gia tốc của dòng chảy 
    \item \(\textcolor{red}{p}\): áp suất, \(\textcolor{red}{-\nabla p}\) mô tả ứng suất cắt (shear stress) 
    \item \(\textcolor{red}{\mu}\): là hệ số nhớt, đặc trưng cho độ nhớt (độ cản trở) (viscosity) của chất lỏng.
\end{itemize} 

\end{document}
```

Nên người dùng có thể sử dụng luôn lệnh `\textcolor` trong việc viết các kí hiệu toán học mà không cần phải nhớ sử dụng lệnh `\mathcolor`.  

Tuy vậy, trong trường hợp các kí hiệu toán học cần để mặc định in nghiêng . . . (như ở ví dụ sau) thì việc sử dụng `\mathcolor` trong vấn đề nêu đây là hoàn toàn hợp lí. 

Kết luận lại, ta sẽ sử dụng lệnh `\mathcolor` . . . (khi nào) và lệnh `\textcolor` . . . (khi nào)

<div align="center">
<img src="LaTeX-Library-project-v1.0.0/b. Lectures notes/Mathematics/images math/Navier-Stokes.jpg" alt="Navier - Stokes">
</div> 
<center>Claude-Louis Navier (bên trái) và George Stokes (bên phải)</center>

--- 

## Tài liệu tham khảo: 

\[1]: https://dduclam.wordpress.com/wp-content/uploads/2017/02/ns_epsilon13.pdf 

--- 

## Footnote 


