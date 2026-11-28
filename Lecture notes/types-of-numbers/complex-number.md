## Bài học:

\+ Viết tính chất cộng hai số phức liên hợp 

$\overline{z_1} + \overline{z_2} = \overline{z_1 + z_2}$

Để viết dấu . . . ta sử dụng lệnh 

```latex 
\overline{}
```

Áp dụng điều này  . . . ta được

```latex 
\overline{z_1} + \overline{z_2} = \overline{z_1 + z_2} 
```

\+ Mũ hai số phức dạng lượng giác 
$z\cdot z = z^2 = [r \cdot (\cos(\phi) + i\sin(\phi))]^2 = r^2 \cdot (\cos(\phi)^2 + 2 \cdot \cos(\phi) \cdot i\sin(\phi) + (i\sin(\phi)^2) = r^2 \cdot (\cos(2\phi) + i \sin(2\phi))$ 
\+ Mũ $n$ số phức dạng lượng giác 

$\underbrace{z \cdot z \cdot \ldots \cdot z}_{n} = z^n = [r \cdot (\cos(\phi) + i\sin(\phi))]^n = r^n \cdot [\cos(n \phi) + i \sin (n \phi)]$

Công thức này còn được gọi là công thức De Moivre dùng để nâng một số phức dưới dạng lượng giác lên lũy thừa bậc $n$ một cách nhanh chóng.

Để viết được $\underbrace{z \cdot z \dots z}_{n}$ ta sử dụng lệnh: 
```latex
\underbrace{. . .}_{. . .}
```

trong đó: 
+  `{...}` . . .
+ `{...}` . . .

\+ Căn bậc 2 của 2 được kí hiệu là $\sqrt{2}$  

Để viết được căn bậc 2 của một số bất kì ta sử dụng lệnh 

```latex
\sqrt{}
```

Bên trong dấu ngoặc nhọn của lệnh `\sqrt` là số . . .(? viết lại)

Viết lại . . . 

```latex
\sqrt{2}
```

\+ Căn bậc 3 của 2 được kí hiệu là $\sqrt[3]{2}$

```latex
\sqrt[3]{2}
```

\+ Căn bậc $n$ của số phức 

$$
\sqrt[n]{z} = \sqrt[n]{r} \left[\cos\left(\frac{a}{n} + \frac{k2\pi}{n}\right) + i\sin\left(\frac{a}{n} + \frac{k2\pi}{n}\right) \right], \ k = \{1, 2, \dots, n\}
$$

```latex
\sqrt[n]{z} = \sqrt[n]{r} . . .
```