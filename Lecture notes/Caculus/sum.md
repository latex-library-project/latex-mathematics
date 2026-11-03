##  Bài học 

### Tổng 

Vào năm lớp 6 THCS (theo chương trình học Việt Nam ...), chúng ta đã quen thuộc với bài toán đếm tổng dãy từ 1 đến 100 huyền thoại mà ở đó nhà toán học người Đức Carl Gauss đã giải bằng một phương pháp thú vị . . . mà tổng tính được từ dãy đó là 5050

Nếu ta viết lại đáp án bài toán lại như sau

$$1+2+3+4+5+.... + 100 = 5050$$ 
thì sẽ rất dài. 

Kí hiệu tổng: 

```latex
\(\sum\)
```

$\sum$

được phát minh lần đầu bởi nhà toán học Euler vào năm 1755. 

. . . (? viết tiếp)

<div align="center">
<img src="LaTeX-Library-project-v1.0.0/Draft/draft img/1.1.jpg" alt="1.1">
Nguồn: https://thomaskojar.wordpress.com/2021/05/13/history-of-math-symbols/
</div>

$$
\sum^{100}_{n = 1} n = 5050 
$$

#### inline math

Để viết kí hiệu tổng (sigma) ta sẽ sử dụng lệnh: 

```tex
\sum  
```

Lệnh này đã được hệ thống cài đặt sẵn, nên ta không cần phải khai báo thêm package nào thêm cả.

Ví dụ về kí hiệu sigma không có điều kiện (? chuẩn thuật ngữ chưa nhỉ) 

```tex
\documentclass{article}

\begin{document}

\[
     \sigma C_n = . . .  
\]

\end{document}
```

>[!WARNING]
> Nếu như chúng ta viết sát biểu thức (? đúng chưa nhỉ, còn gì nữa nhỉ) với lệnh `\sigma`, hệ thống sẽ báo lỗi **Undefined control sequence**. 

```tex
\documentclass{article}

\begin{document}

\[
     \sigmaC_n = . . .  
\]

\end{document}
```

Ví dụ về kí hiệu sigma có điều kiện (? chuẩn thuật ngữ chưa nhỉ) 

```tex
\(\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s}\)
```

$\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s}$

So với việc viết kí hiệu tổng không điều kiện (?) ở trên, ta có thể viết liền chúng mà không bị hệ thống báo lỗi.

```tex
\(\zeta(s) = \sum_{n=1}^{\infty}\frac{1}{n^s}\)
```

Tuy vậy, chúng ta nên cách ra để khi đọc đoạn mã sẽ dễ dàng hơn. (? . . . vì sao thế nhỉ) 

Để có thể căn chỉnh kí hiệu tổng sao cho đẹp, ta có thể sử dụng lệnh: 

```tex
\displaystyle
```

vào trước lệnh `\sum`

```tex
\documentclass{article}

\begin{document}

\(\zeta(s) = \displaystyle\sum_{n=1}^{\infty} \frac{1}{n^s}\)

\end{document}
```

$\zeta(s) = \displaystyle\sum_{n=1}^{\infty} \frac{1}{n^s}$  

Ngoài lệnh `\displaystyle` để căn chỉnh trên ta còn có các lệnh sau: 

|Lệnh|Mô tả|Ghi chú thêm|
|:---|:----|:-----------| 
|`\textstyle`|Kích thước dành cho các phương trình được viết ở chế độ toán học **inline math**|Vì kích thước của chúng đã hệ thống mặc định như ban đầu, nên ta không cần phải sử dụng trong việc viết chúng trong toán học ở chế độ| 

Để dễ hình dung, ta quay lại với ví dụ ban đầu, nếu ta thêm lệnh `textstyle`: 

```tex
\documentclass{article}

\begin{document}

\(\zeta(s) = \textstyle\sum_{n=1}^{\infty} \frac{1}{n^s}\)

\end{document}
```

Kết quả cho ra được cũng ra giống hệt với lúc ban đầu:  

$\zeta(s) = \textstyle\sum_{n=1}^{\infty} \frac{1}{n^s}$  

Vậy nên ta chỉ cần viết như cách ban đầu là được, mà không cần phải sử dụng lệnh `\textstyle`. 

**Câu hỏi**: Vậy lệnh `\textstyle` nên được sử dụng vào lúc nào ? 

Nếu chúng ta viết một đoạn văn dài, có chứa bên trong đoạn văn công thức tổng sử dụng lệnh `\displaystyle`, chẳng hạn như ví dụ sau: 

```tex
\documentclass{article}

\begin{document}

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Ut purus elit, vestibulum ut, placerat ac, adipiscing vitae, felis. Curabitur dictum gravida mauris. Donec vehicula augue eu neque. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas
\(
     \displaystyle\sum^{100}_{n = 1} k = 5050 
\)
Nam arcu libero, nonummy eget, consectetuer id, vulputate a, magna.Donec vehicula augue eu neque. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas

\end{document}
```

Có thể thấy, một khoảng cách rộng giữa dòng trong đoạn văn bản chứa kí hiệu tổng sử dụng lệnh `\displaystyle` và dòng không chứa kí hiệu tổng đó. 

**Câu hỏi**: Điều này làm ảnh hưởng gì đến với người đọc ?

**Câu hỏi**: Làm thế nào để giải quyết vấn đề trên ?

. . .

Vấn đề này bạn cũng sẽ gặp rất nhiều đối với các bài học . . . (? gồm những phần bài học nào có gặp vấn đề trên)

---

#### display math

```latex
\[\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s}\]
```

$$
\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s}
$$

Giả sử, cho $s = 2$, thay vào . . . ta được: 

$$
\zeta(2) = \sum_{n=1}^{\infty} \frac{1}{n^s} = \frac{1}{1^2} + \frac{1}{2^2} + \frac{1}{3^2} + \dots
$$
. . . (đọc đầy đủ định lý ở đây https://pkg.yihui.org/bookdown/markdown-extensions-by-bookdown#theorems) 

Từ những kiến thức đã trình bày ở trên về cách viết kí hiệu tổng trên, ta viết gọn lại bài toán tổng ở đầu bài như sau: 

```latex
\[\sum_{n = 1}^{100} = 5050\]
```

$$
\sum^{100}_{n = 1} n = 5050 
$$

#### Mở rộng: 

Primed sum operator (tạm dịch là Toán tử tổng có phẩy) được kí hiệu là $\sum\nolimits '$. 

Về kí hiệu `'`, xem qua lại phần bài học kí hiệu (? bài học nào cơ).

Đối với **inline math**: $\sum\nolimits '$. 

Đối với **display math**: 

$$
\sum\nolimits '
$$

Đối với tổng không có điều kiện, ta sẽ kết hợp với lệnh 

```tex
\nolimits
```

được sử dụng bên cạnh lệnh `\sum`. 

Đoạn mã: 

```tex
\[
     \sum\nolimits '
\]
```


**Câu hỏi**: Lệnh `\nolimits` này có phải đối nghịch của lệnh `\limits` mà ta đã sử dụng ở bài học toán [giới hạn](/Lecture%20notes/Caculus/lim.md) hay không ?

Với tổng có điều kiện, ta không nên sử dụng lệnh `\nolimts` khi viết ở chế độ toán học **display math**, để dễ hình dung, ta xem qua ví dụ sau (thay bằng một ví dụ toán học tốt sau):

```tex
\sum\nolimits'_{n<k,\;\text{$n$ odd}} nE_n
```

Kết quả hiện thị sẽ là: 

$$
    \sum\nolimits'_{n<k,\;\text{$n$ odd}} nE_n
$$

Có thể thấy, lúc này điều kiện của hàm tổng đang ở dạng (? thay câu từ chuẩn lại) sẽ là `\textstyle`. 

Để khắc phục được điều này, ta sẽ sử dụng một lệnh mới là 

```tex
\sideset{}{}
```

(? phân tích lệnh này cho người dùng hình dung) 

Lệnh này không được hệ thống cài đặt sẵn, mà phải khai báo package **amsmath**, thì mới có thể sử dụng được lệnh này. 

Lệnh này phải được đặt trước lệnh `\sum`. 

Sửa lại đoạn mã trên 

```tex
\sideset{}{'}\sum_{n<k,\;\text{$n$ odd}} nE_n
```

lúc này ta được: 

$$
     \sideset{}{'}\sum_{n<k,\;\text{$n$ odd}} nE_n
$$

Nếu ta không viết lệnh `\sideset` trước lệnh `\sum` thì hệ thống sẽ báo lỗi . . . (? gồm những lỗi gì) 


Trong một số tài liệu toán, chẳng hạn như bài báo . . . (? bài báo nào chỉ điểm đến nguồn giúp) 

(? ảnh từ bài bào đó)

khi soạn thảo latex, nếu không cần quá chu tâm nhiều đến việc căn chỉnh phải nhớ những lệnh trên, mà chọn một giải pháp đơn giản hơn như sau: (viết ví dụ tạm thời đây, sau đó viết cái mới sau)

```tex
\[
     \sum_{n<k,\;\text{$n$ odd}}' nE_n
\]
```

kết quả hiển thị sẽ là


$$
    \sum_{n<k,\;\text{$n$ odd}}' nE_n
$$

Lúc này mặc định dấu `'` sẽ nằm ở chỉ số trên kí hiệu tổng. 

Vậy nên, nếu ta viết kí hiệu chỉ số trên thêm, 

```tex
\[
     \sum_{n<k,\;\text{$n$ odd}}^{1} ' nE_n
\]
```

thì hệ thống sẽ báo lỗi **Double superscript**. 

Điều này, khi xét về mặt toán học cũng hoàn toàn đúng về ý nghĩa kí hiệu của chúng. (? xác nhận lại quan điểm này và giải thích thêm về chúng thay vì chỉ đưa ra nhanh chóng kết luận, mà không đưa ra thêm giải thích). 


Nếu người dùng sử dụng lệnh `\subset{}{}` để sửa: 

```tex
\[
    \subset{}{'} \sum_{k=1}^1 C_n
\]
```

thì người dùng có thể thấy, về mặt câu lệnh latex, thì hệ thống sẽ xác nhận là hoàn toàn chính xác. Với lệnh `\subset` lúc này đang được hệ thống hiểu là kí hiệu tập con (xem qua lại ở bài học [kí hiệu]() (? bài học nào đây cháu bé)), dấu `'` được hiển thị bên bên trong phương trình, dù được bao bởi dấu ngoặc nhọn, nhưng vì không phải lệnh để hiển thị dấu ngoặc trong tài liệu, nên nó không hiển thị trên trang tài liệu. Còn lệnh `\sum` được viết với điều kiện trên và dưới hoàn toàn hợp lệ với những gì mà ta đã học ở phần trên. (? mô tả hơi loạn, cần đọc và sửa lại)  

Nhưng chúng vẫn sẽ là không chính xác về mặt toán học về kí hiệu toán tử tổng có dấu phẩy mà ta đang được học. (? mô tả hơi loạn, cần đọc và sửa lại)

---

## Câu hỏi: 

**Câu hỏi 1**: Tại lại là lệnh `\sum` mà không phải là lệnh `\Sigma`, để viết kí hiệu tổng (sigma). 

--- 

## Bổ sung: 

Sử dụng lệnh 

```tex
\atop
```

để viết điều kiện dài thay vì trên cùng một dòng, thì có thể phân cách qua dấu `,`.  

ví dụ: 

```tex
{\displaystyle s(n)=\sum _{{d|n,} \atop {d\neq n}}d\,.} 
```

kết quả: 

$$
{\displaystyle s(n)=\sum _{{d|n,} \atop {d\neq n}}d\,.}
$$

tham khảo từ trang wiki: 

https://en.wikipedia.org/wiki/Aliquot_sum và https://wikimedia.org/api/rest_v1/media/math/render/svg/efef3d606e4f16796b5fed1270794af51abf52f3 

Để viết nhiều điều kiện (? thuật ngữ chuẩn chưa nhỉ) cùng một lúc, ta sẽ sử dụng lệnh: 

```tex
\substack{}
```.

Ví dụ: (thay bằng một ví dụ mới sau) 

```tex
\[
     \prod_{\substack{
               1\le i \le n\\
               1\le j \le m}
          }
          M_{i,j}
\]
```

Kết quả hiển thị: 

$$
\prod_{\substack{
            1\le i \le n\\
            1\le j \le m}
     }
     M_{i,j}
$$ 