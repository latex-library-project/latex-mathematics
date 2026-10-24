## Bài học:

### Tổ hợp chập $k$ của của $n$ 

```latex
\[\binom{n}{k} = \frac{n!}{k!(n-k)!}\]
```

$$\binom{n}{k} = \frac{n!}{k!(n-k)!}$$
Trong đó: $n! = 1 \cdot 2 \cdot 3 \dots \cdot (n-2) \cdot (n-1) \cdot n$  là một hoán vị cấp n. 

. . . . khai báo package: 

```latex
\usepackage{amsmath}
```

. . . . lệnh `\tbinom` . . . : 

```latex
\[\tbinom{n}{k} = \frac{n!}{k!(n-k)!}\]
```

$$\tbinom{n}{k} = \frac{n!}{k!(n-k)!}$$
Ở **inline math** thì lệnh `\binom` và `tbinom` có kích thước không khác gì nhau.  Chỉ khi sử dụng lệnh 

```latex
\dbinom
```

ở **inline math** thì sẽ thấy rõ sự khác biệt kích thước. 

$\dbinom{n}{k} = \frac{n!}{k!(n-k)!}$  