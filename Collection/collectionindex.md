## Giới thiệu: 

**Ví dụ**: 

|Kí hiệu|Cách đọc|LaTeX|Gói|Ghi chú|
|:------|:-------|:----|:--|:------| 
|$\pm$|Dấu cộng trừ (Plus–minus sign)[^1]|`\pm`|Không cần|Chỉ được sử dụng trong lệnh và môi trường toán học| 

Có lẽ cách viết theo dạng bảng này không hợp với triết lý mà tôi muốn trình bày, vì chúng không có chỗ để tôi đưa ra ví dụ, trong ví dụ đó phải có đoạn mã chạy và kết quả hiển thị đoạn mã đó. 

**Ví dụ**: 

Kí hiệu: $\pm$. 

Cách đọc: Dấu cộng trừ (Plus–minus sign). 

Cách sử dụng: Không cần phải cài đặt thêm gói nào cả, chỉ được sử dụng bên trong lệnh hoặc môi trường viết chế độ toán học. 

Ví dụ về kí hiệu $\pm$ với hai nghiệm phân biệt từ phương trình bậc hai một ẩn: 

```tex
\documentclass{article}

\begin{document}

\[
    x_{1,2} = - \frac{b \pm \sqrt{\Delta}}{4a}
\]

\end{document}
```

Kết quả cho ra được sẽ là: 

$$
x_{1,2} = - \frac{b \pm \sqrt{\Delta}}{4a}
$$

Đây chính là điều mà tôi mong muốn, khi sưu tập và trình bày về các kí hiệu trong LaTeX. 

Tương tự ta cũng sẽ viết về kí hiệu $\mp$

|Kí hiệu|Cách đọc|LaTeX|Gói|Ghi chú|
|:------|:-------|:----|:--|:------| 
|$\mp$|Dấu ....|`\mp`|Không cần|Chỉ được sử dụng trong lệnh và môi trường toán học|

Ví dụ về kí hiệu $\mp$ với công thức cộng hàm $\cos$ trong lượng giác: 

```tex
\documentclass{article}

\begin{document}

\[
    \cos(\alpha \pm \beta) = \cos(\alpha) \cos(\beta) \mp \sin(\alpha) \sin(\beta)
\]

\end{document}
```

$$
    \cos(\alpha \pm \beta) = \cos(\alpha) \cos(\beta) \mp \sin(\alpha) \sin(\beta)
$$

>[!NOTE]
> Cách viết kí hiệu dấu $\mp$ chính là đảo lại thứ tự của cách viết kí hiệu viết dấu cộng trù $\pm$.

---

## Chú thích:

[^1]: https://en.wikipedia.org/wiki/Plus%E2%80%93minus_sign 