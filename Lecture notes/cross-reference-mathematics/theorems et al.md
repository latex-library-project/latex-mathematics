Để tham chiếu đến định lý, định nghĩa, trước tiên ta cần đặt lệnh 

```latex
\label{}
```

vào môi trường định nghĩa "định lý", "định nghĩa" ...vv... đó.

Để tham chiếu đến môi trường đó ta cần đặt lệnh 

```latex
\ref{}
```

vào . . . 

Ví dụ: . . .

```latex
\documentclass{article}

\usepackage[utf8]{vietnam}

% Useful packages

%  Khai báo màu đường link
\usepackage[colorlinks=true, allcolors=blue]{hyperref}

\usepackage{amsmath}
\usepackage{amsthm}

\theoremstyle{plain}
\newtheorem{theorem}{Định lý}[section]

\begin{document}

\begin{theorem}[Định lý Rolle]
    Cho hàm số $f$ liên tục trên đoạn $[a;b]$ có đạo hàm trên khoảng $(a;b)$ và $f(a) < f(b)$ khi đó tồn tại $c \in (a;b)$ sao cho $f^{'}(c) = 0$
    \label{thm:0.1}
\end{theorem}

\begin{proof}
    Xem ở đây: \url{https://artofproblemsolving.com/wiki/index.php?title=Rolle%27s_Theorem}
\end{proof}

\begin{theorem}[Định lý giá trị trung bình Lagrange]
    Cho hàm số $f$ liên tục trên đoạn $[a;b]$  có đạo hàm trên khoảng $(a;b)$ khi đó tồn tại $c \in (a;b)$ sao cho 
    \[
    f^{'}(c) = \frac{f(b) - f(a)}{b - a} 
    \]
    \label{thm:0.2}
\end{theorem}

\begin{proof}
    . . . 
\end{proof}

Như vậy, định lý \ref{thm:0.2} chính là trường hợp tổng quát của định lý \ref{thm:0.1}.

\end{document}
```

(?) Có hai vấn đề mà mình chưa giải quyết trong phần này

(1) Khi định lý bị thay đổi số thì hệ thống sẽ không được tự cập nhật dẫn đến đôi khi tham chiếu không được hợp lí. Ví dụ khi "định lý 1.1" bị thay đổi thành "định lý 1.2" thì nếu ta để `\label{1.1}` thì `\ref{1.1}` vẫn sẽ để 1.1. 

(2) Với định lý có tên dài, chẳng hạn "định lý Gauss - Wantzel" thì làm sao để `\ref` có đầy đủ tên định lý đó để tham chiếu đến tiêu đề định lý Gauss - Wantzel. 

(Ảnh Lagrange và Rolle) 

<div align="center">

<img src="LaTeX-Library-project-v1.0.0/images/Theorem environments.jpg"> 

</div> 