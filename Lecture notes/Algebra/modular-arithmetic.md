## Bài học: 

Định nghĩa về đồng dư thức: Cho $a, b \in \mathbb{Z}, m \in \mathbb{N}$. a đồng dư với b theo modulo (đọc là mô-đun) m, khi và chỉ khi hiệu của a và b chia hết cho m. 

Kí hiệu: $a \equiv b \pmod{m}$ 

Để viết được kí hiệu đồng dư trong latex, : 

+ a, b là các chữ cái thông thường, được nhập hoàn toàn trực tiếp trên bàn phím.  

+ Dấu bằng có ba gạch ngang (? tạm thời để vậy, nên kiểm tra lại tên gọi thuật ngữ chính xác) $\equiv$, được viết trong latex là `\equiv`. Có thể tra lại ở bài học [kí từ]() (? có bài học này trong đây luôn cơ à).  

Sử dụng lệnh: 

```tex
\pmod
```

```tex
\documentclass{article}

\begin{document}

\(x \equiv a \pmod {b}\)

\end{document}
```

Kết quả cho ra được: 

$x \equiv a \pmod { b }$  

Ví dụ về đồng dư thức được viết ở chế độ toán học display math với định lý Wilson. 

Định lý Wilson. Nếu $p$ là một số nguyên tố thì 

$$
(p-1)! + 1 \equiv 0 \pmod{p}
$$

Viết biểu thức trên vào trong soạn thảo latex: 

```tex
\documentclass{article}

\begin{document}

\[
    (p-1)! + 1 \equiv 0 \pmod{p}
\]

\end{document}
```

<div align="center">
    <img src="./Lecture notes/images/John Wilson.jpg">
</div>
<center>Nhà toán học người Anh Sir John Wilson </center>

