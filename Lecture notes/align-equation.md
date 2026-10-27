## Dàn ý: 

+ Nêu vấn đề  
+ Sử dụng chúng khi nào ? Sử dụng như thế nào ? 
+ Viêt ví dụ để minh họa lệnh hoặc môi trường trên.  

## Lưu ý: 

Sẽ có một vài ví dụ tạm thời được trình bày, để hiểu và hình dung được cách đoạn mã hoạt động, một cách nhanh chóng. 

Để có thể viết một ví dụ đủ tốt, hay, hấp dẫn, ta sẽ tìm và chuyển hóa thành bài học để thay cho ví dụ tạm thời. 

## Bài học: 

### Môi trường `eqnarray`:

Môi trường `eqnarray*` này không cần đặt vào lệnh, môi trường viết phương trình toán học nào cả. Chúng được sử dụng như là một môi trường riêng biệt. 

Hơn nữa, môi trường này đã được hệ thống cài đặt sẵn, nên ta chỉ cần sử dụng môi trường mà không cần phải khai báo thêm package nào cả.

Gợi ý viết ví dụ: 

+ Sử dụng môi trường `eqnarray` để viết các phương trình Maxwell mô tả . . . (trong vật lý).


```tex
\documentclass{article}

\usepackage{amsmath}

\begin{document}

\begin{eqnarray}
    \nabla \cdot \mathbf{E} &=& \frac{\rho}{\epsilon_0} \\
    \nabla \cdot \mathbf{B} &=& 0 \\
    \nabla \cdot \mathbf{E} &=& - \frac{\partial \mathbf{B}}{\partial t}\\
    \nabla \cdot \mathbf{B} &=& \mu_0 \left(\mathbf{J} + \epsilon_0 \frac{\partial \mathbf{E}}{\partial t} \right) 
\end{eqnarray}

\end{document}
```

Kết quả cho ra được sẽ là 

$$
\begin{eqnarray}
    \nabla \cdot \mathbf{E} &=& \frac{\rho}{\epsilon_0} \\
    \nabla \cdot \mathbf{B} &=& 0 \\
    \nabla \cdot \mathbf{E} &=& - \frac{\partial \mathbf{B}}{\partial t}\\
    \nabla \cdot \mathbf{B} &=& \mu_0 \left(\mathbf{J} + \epsilon_0 \frac{\partial \mathbf{E}}{\partial t} \right) 
\end{eqnarray}
$$

Khi người dùng sử dụng môi trường `eqnarray`, vì nó đánh số hết tất cả các phương trình, nên trong trường hợp người dùng không muốn để dòng phương trình đó đước đánh số bên cạnh, ta sẽ sử dụng lệnh 

```tex
\nonumber
```

được đặt ở bên cạnh dòng viết phương trình đó. 



Nếu như người dùng không muốn tất cả các dòng phương trình đều không được đánh số bên cạnh, ta có thể sử dụng lệnh `\nonumber` trên như sau: 

```tex
\documentclass{article}

\begin{document}

\begin{eqnarray}
    662 &=& 414 \cdot 1 + 248 \nonumber \\
    414 &=& 248 \cdot 1 + 166 \nonumber \\
    248 &=& 166 \cdot 1 + 82 \nonumber \\
    166 &=& 82 \cdot 2 + 2 \nonumber \\ 
    82 &=& 2 \cdot 41 \nonumber
\end{eqnarray} 

\end{document}
```

Một cách khác để tối ưu đoạn mã trên, thay vì phải lặp lại nhiều lần lệnh `\nonumber`, thì ta sẽ sử dụng môi trường `eqnarray*`.

### Môi trường `eqnarray*`:

Gợi ý viết ví dụ: 

+ Sử dụng môi trường `eqnarray*` để viết thuật toán Euclid để tìm UCLN của hai số bất kì.

```tex
\documentclass{article}

\begin{document}

\begin{eqnarray*}
    662 &=& 414 \cdot 1 + 248  \\
    414 &=& 248 \cdot 1 + 166 \\
    248 &=& 166 \cdot 1 + 82  \\
    166 &=& 82 \cdot 2 + 2 \\ 
    82 &=& 2 \cdot 41
\end{eqnarray*} 

\end{document}
```

Từ những điều ở trên, ta có thể thấy rằng, chúng ta nên sử dụng lệnh `\nonumber` khi riêng lẻ, thay vì cộng dồn. (? mô tả lại nhé).  

Một cách khác để căn chỉnh các dòng phương trình toán học thay cho môi trường `eqnarray` là sử dụng một môi trường mới có tên là `align`.  

### Môi trường `align`:  

Trước đó, người dùng nhớ cần phải khai báo package `amsmath`. 

```tex
\documentclass{article}

\usepackage{amsmath}

\begin{document}

\begin{align}
    \nabla \cdot \mathbf{E} &= \frac{\rho}{\epsilon_0} \\
    \nabla \cdot \mathbf{B} &= 0 \\
    \nabla \cdot \mathbf{E} &= - \frac{\partial \mathbf{B}}{\partial t}\\
    \nabla \cdot \mathbf{B} &= \mu_0 \left(\mathbf{J} + \epsilon_0 \frac{\partial \mathbf{E}}{\partial t} \right) 
\end{align} 

\end{document}
```

Kết quả cho ra được sẽ là

$$
\begin{align}
    \nabla \cdot \mathbf{E} &= \frac{\rho}{\epsilon_0} \\
    \nabla \cdot \mathbf{B} &= 0 \\
    \nabla \cdot \mathbf{E} &= - \frac{\partial \mathbf{B}}{\partial t}\\
    \nabla \cdot \mathbf{B} &= \mu_0 \left(\mathbf{J} + \epsilon_0 \frac{\partial \mathbf{E}}{\partial t} \right) 
\end{align} 
$$

>[!WARNING]
> Nếu như người dùng quên khai báo package `amsmath` để sử dụng môi trường `align`, hệ thống LaTeX sẽ báo lỗi **Environment align undefined.**

Nếu như người dùng bỏ package `amsmath` ở ví dụ viết phương trình Maxwell trên:

```tex
\documentclass{article}

\begin{document}

\begin{align}
    \nabla \cdot \mathbf{E} &= \frac{\rho}{\epsilon_0} \\
    \nabla \cdot \mathbf{B} &= 0 \\
    \nabla \cdot \mathbf{E} &= - \frac{\partial \mathbf{B}}{\partial t}\\
    \nabla \cdot \mathbf{B} &= \mu_0 \left(\mathbf{J} + \epsilon_0 \frac{\partial \mathbf{E}}{\partial t} \right) 
\end{align} 

\end{document}
```

Người dùng có thể thấy, ở dòng thứ thứ 5 của đoạn mã sẽ xuất hiện thông báo lỗi như đã lưu ý trên. 

. . . (? chưa viết để kết nối với đoạn này) Điều này sẽ rất có ích đối với việc người dùng sử dụng môi trường `align` để viết một phương trình hoặc khai triển biểu thức dài. Xem bài học [viết phương trình dài](/Lecture%20notes/display-long-equation.md) để biết thêm chi tiết. 

### Môi trường `align*`:
  
Trước đó, người dùng nhớ cần phải khai báo package `amsmath`. 

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\begin{align*}
    662 &= 414 \cdot 1 + 248 \\
    414 &= 248 \cdot 1 + 166 \\
    248 &= 166 \cdot 1 + 82 \\
    166 &= 82 \cdot 2 + 2 \\ 
    82 &= 2 \cdot 41
\end{align*}
\end{document}
```

$$
\begin{align*}
    662 &= 414 \cdot 1 + 248 \\
    414 &= 248 \cdot 1 + 166 \\
    248 &= 166 \cdot 1 + 82 \\
    166 &= 82 \cdot 2 + 2 \\ 
    82 &= 2 \cdot 41
\end{align*}
$$

>[!WARNING]
>Người dùng không được phép để môi trường `align`, `align*` vào trong lệnh hoặc môi trường viết toán học. Nếu không, hệ thống sẽ thông báo lỗi **Package amsmath Error: Erroneous nesting of equation structures;** (? kiểm tra lại tên gọi lỗi này). 

### Môi trường `gather`: 

+  Môi trường gather giúp khai triển các phương trình liên tiếp, căn giữa mà không cần quan tâm đến bất kỳ sự căn chỉnh nào (? chưa biết lệnh này dùng để làm gì) 

```latex
\documentclass{article}

\usepackage{amsmath}

\begin{document}

\begin{gather*} 
2x - 5y =  8 \\ 
3x^2 + 9y =  3a + c
\end{gather*}

\end{document}
```

$$
\begin{gather*} 
2x - 5y =  8 \\ 
3x^2 + 9y =  3a + c
\end{gather*}
$$

### Môi trường `split`: 

+ Môi trường `split` giúp khai triển đẳng thức đáng nhớ căn bản sau:  

(nháp. . .chẳng hạn như ví dụ ở sau đây (? thay bằng một ví dụ khác về khai triển $a^n + b^n$  và ví sao không có công thức $a^2 + b^2$))   

```latex
\documentclass{article}

\usepackage{amsmath}

\begin{document}

\[
\begin{split}
    (a+b)^2 &= (a+b) \cdot (a+b) \\
            &= a \cdot (a+b) + b \cdot (a+b) \\
            &= a^2 + ab + ba + b^2 \\
            &= a^2 +2ab + b^2
\end{split}
\]

\end{document}
```

Kết quả cho ra được sẽ là: 

$$
\begin{split}
    (a+b)^2 &= (a+b) \cdot (a+b) \\
            &= a \cdot (a+b) + b \cdot (a+b) \\
            &= a^2 + ab + ba + b^2 \\
            &= a^2 +2ab + b^2
\end{split}
$$

Ta cũng có thể sử dụng môi trường `align*` để khai triển hằng đẳng thức đánh nhớ trên: 

```tex
\documentclass{article}

\usepackage{amsmath}

\begin{document}

\begin{align*}
    (a+b)^2 &= (a+b) \cdot (a+b) \\
            &= a \cdot (a+b) + b \cdot (a+b) \\
            &= a^2 + ab + ba + b^2 \\
            &= a^2 +2ab + b^2
\end{align*}

\end{document}
```

Kết quả cho ra được cũng sẽ tương tự như việc người dùng sử dụng môi trường `split`: 

$$
\begin{align*}
    (a+b)^2 &= (a+b) \cdot (a+b) \\
            &= a \cdot (a+b) + b \cdot (a+b) \\
            &= a^2 + ab + ba + b^2 \\
            &= a^2 +2ab + b^2
\end{align*}
$$

Vậy đâu là sự khác nhau giữa môi trường `align*` và môi trường `split` ?

---



## Câu hỏi: 

+ Sự giống và khác giữa hai lệnh `eqnarray` và `align`.  
+ Ưu và nhược của cả hai lệnh trên. 
+ Nên ưu tiên sử dụng lệnh nào ? trong trường hợp nào ? 

(Tham khảo câu trả lời tại 

https://www.tug.org/pracjourn/2006-4/madsen/)

+ Sự khác nhau giữa môi trường `align*` và môi trường `split`. 