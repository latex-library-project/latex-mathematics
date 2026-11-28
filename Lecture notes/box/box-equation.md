## Bài học: 

Bi ba bi bô

---

### Ý thứ nhất: Đóng khung công thức cơ bản 

Đóng khung công thức qua tài liệu tham khảo sau: 

https://ocw.mit.edu/courses/8-902-astrophysics-ii-fall-2023/mit8_902_f23_lec10.pdf 

Để đóng khung công thức, ta sẽ viết công thức vào trong lệnh: 

```tex
\boxed{}
```

Vì lệnh này không được LaTeX định nghĩa sẵn, mà ta phải thông báo thêm package **amsmath**. 

Xem qua ví dụ sau: 

```tex
\documentclass{article}

\usepackage{amsmath}

\begin{document}


\begin{equation}
    \boxed{\mathrm{H}^2 = \left( \frac{\dot{a}}{a} \right)^2 = \frac{8\pi G}{3}\rho - \frac{kc^2}{a^2} + \frac{\Lambda c^2}{3}}
\end{equation}

\end{document}
```

Kết quả hiển thị trong trang tài liệu:

$$
\begin{equation}
    \boxed{\mathrm{H}^2 = \left( \frac{\dot{a}}{a} \right)^2 = \frac{8\pi G}{3}\rho - \frac{kc^2}{a^2} + \frac{\Lambda c^2}{3}}
\end{equation}
$$

