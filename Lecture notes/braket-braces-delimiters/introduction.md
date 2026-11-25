## Bài học: 

### Giới thiệu:

Dấu ngoặc rất phổ biến trong việc bao quát các biểu thức, toán tử trong toán học. Một số dấu ngoặc thông dụng được sử dụng, đi kèm với lệnh của chúng trong LaTeX được trình bày ở bảng dưới đây: 

|         Ký hiệu          | Tên tiếng Việt                      | Tên tiếng Anh                     | Lệnh LaTeX                                             |
| :----------------------: | :---------------------------------- | :-------------------------------- | :----------------------------------------------------- |
|         $(...)$          | Dấu ngoặc đơn                       | Parentheses (or Round brackets)   | `(...)` (nhập dấu ngoặc tròn trên bàn phím)            |
|         $[...]$          | Dấu ngoặc vuông                     | Brackets (or Square brackets)     | `[...]` (nhập dấu ngoặc vuông trên bàn phím)           |
|        $\{... \}$        | Dấu ngoặc nhọn                      | Braces (or Curly brackets)        | `\{...\}` (nhập dấu ngoặc nhọn trên bàn phím)          |
|   $\langle... \rangle$   | Dấu ngoặc nhọn góc / Ngoặc nhọn dẹt | Angle brackets                    | `\langle ... \rangle`                                  |
|     $\vert... \vert$     | Dấu trị tuyệt đối / Dấu gạch đứng   | Vertical bars (or Absolute value) | `\vert...\vert` hoặc `\|...\|` (nhập \| trên bàn phím) |
|     $\Vert... \Vert$     | Dấu chuẩn (Toán học) / Dấu gạch đôi | Double vertical bars (or Norm)    | `\Vert...\Vert` hoặc `\|\| ...\|\|`                    |
|   $\lfloor... \rfloor$   | Dấu hàm sàn / Ngoặc dưới            | Floor brackets                    | `\lfloor...\rfloor`                                    |
|    $\lceil... \rceil$    | Dấu hàm trần / Ngoặc trên           | Ceiling brackets                  | `\lceil...\rceil`                                      |
| $\ulcorner... \urcorner$ |                                     |                                   | `\ulcorner... \urcorner`                               |
|   $/...\textbackslash$   |                                     |                                   | `/...\textbackslash`                                   |

Để viết toán học ở chế độ `inline math` hoặc `display math` được bao quát bởi dấu ngoặc, người dùng chỉ cần đặt phần toán học đó vào bên trong cách viết các dấu ngoặc ở bảng trên một cách bình thường. 

Ví dụ về dấu ngoặc tròn với định lý Taylor[^1] . . . (? thay bằng một công thức toán học khác gọn hơn để minh họa ví dụ này)

```latex
\documentclass{article}
\begin{document}
\[
f(x) = f(a) + \frac{f'(a)}{1!}(x-a) + \frac{f^{''}(a)}{2!}(x-a)^2 + \frac{f^{'''}(a)}{3!}(x-a)^3 + \dots = \sum^\infty_{n = 0}\frac{f^{(n)}(a)}{n!}(x-a)^n
\]
\end{document}
```

Kết quả cho ra được sẽ là 

$$
f(x) = f(a) + \frac{f'(a)}{1!}(x-a) + \frac{f^{''}(a)}{2!}(x-a)^2 + \frac{f^{'''}(a)}{3!}(x-a)^3 + \dots = \sum^\infty_{n = 0}\frac{f^{(n)}(a)}{n!}(x-a)^n
$$


<div align="center">

<img src="./images/Brooks Taylor.jpg" alt="Taylor">

Nhà toán học người Anh Brooks Taylor

</div>

VÍ dụ về dấu giá trị tuyệt đối với . . . (? viết ví dụ mới sau)

. . .

Bên cạnh đó, người dùng cần lưu tâm đến một số lưu ý quan trọng sau đây khi sử dụng dấu ngoặc trong LaTeX.  

---

## Tài liệu tham khảo: 

\[1]:  Nguồn tham khảo viết ở Overleaf: https://www.overleaf.com/learn/latex/Brackets_and_Parentheses  

---

## Footnote: 

[^1]: Công thức tham khảo từ: https://mathworld.wolfram.com/TaylorSeries.html 