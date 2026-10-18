## Dàn ý:

Giới thiệu vấn đề . . . ? 

Cách sử dụng . . . ?

Nó được sử dụng khi nào . . . ? Tại sao ?

## Bài học:

Phải khai báo package `amsmath`  

```tex
\overset{trên}{dưới}
```

Ví dụ về lệnh trên với phép biến đổi Laplace [^1]: 

```tex
\documentclass{article}

\usepackage{amsmath}

\begin{document}

\[
    \mathcal{L}\{f(t)\} = F(s) \overset{\rm{def}}{=} \int^{\infty}_0 e^{-st} f(t) \ dt
\]

\end{document}
```

kết quả cho ra được lúc này sẽ là 

$$
    \mathcal{L}\{f(t)\} = F(s) \overset{\rm{def}}{=} \int^{\infty}_0 e^{-st} f(t) \ dt
$$

Hoặc người dùng cũng có thể sử dụng sử dụng lệnh `stackrel` thay cho lệnh `overset` ở ví dụ trên: 

```tex
\documentclass{article}

\begin{document}

\[
    \mathcal{L}\{f(t)\} = F(s) \stackrel{\rm{def}}{=} \int^{\infty}_0 e^{-st} f(t) \ dt
\]

\end{document}
```

mà kết quả cho ra được là . . . (? gì, như thế nào so với kết quả ban đầu)

$$
    \mathcal{L}\{f(t)\} = F(s) \stackrel{\rm{def}}{=} \int^{\infty}_0 e^{-st} f(t) \ dt
$$

---

## Câu hỏi cần giải quyết: 

**Câu hỏi 1**: Sự giống và khác nhau giữa hai lệnh `\overset` và `stackrel` là gì ? 

**Câu hỏi 2**: Trường hợp thì ta nên ưu tiên sử dụng lệnh `\overset` hơn lệnh `stackrel`, và ngược lại.  

---

[^1] https://math.libretexts.org/Bookshelves/Differential_Equations/Differential_Equations_for_Engineers_(Lebl)/6%3A_The_Laplace_Transform/6.1%3A_The_Laplace_Transform