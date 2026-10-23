Trong một số trường hợp, khi người dùng viết tài liệu toán học cần [tham chiếu]() từ đoạn văn bản này đến phương trình toán học ở chế độ `display math`, mà không cần phải viết lặp lại, cũng như sẽ bị tràn ra khỏi văn bản đối với các [phương trình dài]() (? của phương trình đó ở chế độ `inline math` . . . (? viết tiếp đê)) 

Để làm được điều này, trước tiên người dùng cần phải khai báo package ở bài học [liên kết thông thường]() 

```latex 
\usepackage{hyperref}
```

Tiếp theo, để tham chiếu chéo đến phương trình toán học đó, người dùng sử dụng lệnh 

```latex
\label
```

cần phải được đặt vào trong môi trường `equation`. 

Cuối cùng là lệnh

```latex
\ref{}
```

hoặc lệnh 

```latex
\eqref{}
```

được đặt ở trong đoạn văn mà người dùng mong muốn để được tham chiếu đến phương trình có lệnh `\label` tương ứng.  

> [!NOTE]  
>  Người dùng nên để lệnh `\label` ở bên cạnh `\begin{equation}`, vì . . . (? vì sao thế nhỉ ?)

. . . .(? viết ví dụ mới yéeeeeeee)

```latex
\documentclass{article} % 
\usepackage{hyperref} % . . .
\begin{document} \label{eq:1} %
\begin{equation} % Sử dụng môi trường equation để đánh số thứ tự ở phương trình logarit
\log_b{xy} = \log_b{x} + \log_b{y} 
\end{equation}
. . . \ref{}
\end{document}
```

Điểm khác biệt giữa lệnh `\ref` và lệnh `\eqref`, đó là lệnh `\eqref` sẽ được hệ thống tự động thêm dấu ngoặc tròn `()` cho số thứ tự tương ứng với phương trình được tham chiếu ở đoạn văn, còn lệnh `\ref` thì không.  

```latex
\documentclass{article}
\begin{document}
\begin{equation} \label{eq:1} % . . .
\log_b{xy} = \log_b{x} + \log_b{y}
\end{equation}

. . . (\ref{eq:1}) % lệnh \ref không được hệ thống tự động đóng ngoặc tròn, mà người dùng phải tự chủ động thêm vào nếu cần.    
. . . \eqref{eq:1} % lệnh \eqref được hệ thống tự động đóng ngoặc tròn, mà người dùng không cần phải tự chủ động thêm vào. 

\end{document}
```

> [!WARNING]  
> Nếu như người dùng viết nội dung bên trong dấu ngoặc nhọn `{}` của lệnh `\ref`, cũng như là lệnh `\eqref` mà không trùng với nội dung bên trong dấu ngoặc nhọn của lệnh `\label` nào bên trong phần soạn thảo LaTeX, thì hệ thống sẽ báo lỗi `Undefined reference`. Lúc này, ở trong trang tài liệu, đoạn văn có lệnh`\ref` (hoặc lệnh `\eqref`) thay vì được hiện thị số thứ tự tương ứng với lệnh `\label` của phần toán học cần được trỏ đến, thì sẽ xuất hiện hai lần dấu chấm hỏi `??`, 

```latex
\documentclass{article}

\usepackage{hyperref}

\begin{document} 

\begin{equation} \label{eq:1}
\log_b{xy} = \log_b{x} + \log_b{y}
\end{equation}

. . . \eqref{eq:2} . . .\ref{eq:1}

\end{document}
```

Vậy nên, nội dung bên trong dấu ngoặc nhọn của lệnh `\label` và lệnh `\ref` (hoặc `\eqref`) đều phải được giống nhau. 

```latex
\documentclass{article}

\usepackage{hyperref}

\begin{document} 

\begin{equation} \label{eq:1}
\log_b{xy} = \log_b{x} + \log_b{y}
\end{equation}

. . . \eqref{eq:1} . . .\ref{eq:1}

\end{document}
```

> [!WARNING]  
> Nếu như người dùng để nội dung bên trong dấu ngoặc nhọn `{}` của nhiều lệnh `\label` là giống hệt nhau, thì hệ thống sẽ báo lỗi `multiply-defined labels`. 

```latex
\documentclass{article}

\begin{document}

\begin{equation} % 
\log_b{xy} = \log_b{x} + \log_b{y}
\label{eq:1} % 
\end{equation}

\begin{equation} % 
\log_b{\frac{x}{y}} = \log_b{x} - \log_b{y} 
\label{eq:1} % 
\end{equation}

\end{document}
```

>[!WARNING]
>Hơn nữa, nếu lệnh `\label` bị trùng nội dung với nhau bên trong dấu ngoặc nhọn, thì lệnh `\ref` cũng như là lệnh `\eqref` sẽ được hệ thống mặc định trỏ đến vị trí có lệnh `\label` xuất hiện gần nhất.

```latex
\documentclass{article}

\begin{document}

\begin{equation} % 
\log_b{xy} = \log_b{x} + \log_b{y}
\label{eq:1} % 
\end{equation}

\begin{equation} % 
\log_b{\frac{x}{y}} = \log_b{x} - \log_b{y} 
\label{eq:1} % 
\end{equation}

. . . \ref{eq:1} . . . 

\end{document}
```

 Vậy nên, nội dung bên trong dấu ngoặc nhọn của mỗi lệnh `\label` là phải khác nhau nhằm phân biệt số thứ tự của các phương trình toán học.  

```latex
\documentclass{article}

\begin{document}

\begin{equation} % 
\log_b{xy} = \log_b{x} + \log_b{y}
\label{eq:1} % 
\end{equation}

\begin{equation} % 
\log_b{\frac{x}{y}} = \log_b{x} - \log_b{y} 
\label{eq:2} % 
\end{equation}

. . . \ref{eq:1} . . . 

\end{document}
```

Các chú ý trên cũng được áp dụng tương tự với các bài học tham chiếu chéo [hình ảnh](), [bảng](), ..vv..   