## Bài học:   

Để viết toán tử giới hạn, ta sẽ sử dụng lệnh: 

```tex
\lim
```

Lệnh này chỉ có thể được sử dụng bên trong lệnh và môi trường viết toán học. 

Đối với việc viết kí hiệu giới hạn ở chế độ **inline math**: 

```latex
\documentclass{article}
\begin{document}
\(\lim_{x \to \infty}\)
\end{document}
```

$\lim_{x \to \infty}$

Một cách viết khác đẹp hơn là sử dụng thêm lệnh `displaystyle`:

```tex
\documentclass{article}
\begin{document}
\(\displaystyle\lim_{x \to \infty}\)
\end{document}
```

hoặc sử dụng lệnh mới là `limits`:

```latex
\documentclass{article}
\begin{document}
\(\lim\limits_{x \to \infty}\)
\end{document}
```

mà kết quả cho ra được đều là giống hệt nhau: 

$\lim\limits_{x \to \infty}$

Ví dụ về việc viết toán tử lim trong chế độ **display math** với bài toán giới hạn Basel: 

```tex
\documentclass{article}

\begin{document}

\[
    \lim_{n \to \infty} \sum^{n}_{k = 1} \frac{1}{k^{2}} = \frac{\pi^{2}}{6} 
\]

\end{document}
```

Kết quả cho được sẽ là

$$
\lim_{n \to \infty} \sum^n_{k=1} \frac{1}{k^2} = \frac{\pi^2}{6} 
$$

## Câu hỏi: 

**Vấn đề 1**: Sự giống và khác nhau giữa lệnh `displaystyle` và `limits` khi sử dụng để viết toán tử giới hạn là gì ? Nên sử dụng chúng khi nào ? Tại sao ? 