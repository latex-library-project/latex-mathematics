## Bài học:

### Giới thiệu:

Một trong những động lực lớn nhất thúc đẩy [Donald Knuth]() khi bắt đầu phát triển hệ thống TeX ban đầu là tạo ra một công cụ cho phép xây dựng các công thức toán học một cách đơn giản, đồng thời trông chuyên nghiệp khi in ấn. Việc ông thành công có lẽ là lý do tại sao TeX (và sau này là LaTeX) trở nên phổ biến trong cộng đồng khoa học. Việc trình bày toán học là một trong những thế mạnh lớn nhất của LaTeX. Đây cũng là một chủ đề rộng lớn do sự tồn tại của rất nhiều ký hiệu toán học.[^1]

. . . . (? viết tiếp) Để bắt đầu với chủ đề thú vị, đầy hấp dẫn nhưng cũng rất rộng lớn, khó nhằn đây, ta sẽ bắt đầu với một phép toán quen thuộc sau đây: 

$$
1+1=2
$$

Đối với phép tính thông thường trên, người dùng có thể dễ dàng nhập trực tiếp hai [số tự nhiên]() (1, 2), toán tử số học (arithmetic operators) (+, -) và toán tử quan hệ (relational operators) (=) vào trong phần soạn thảo văn LaTeX. 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\begin{document}

Phép tính 1 + 1 = 2 là một trong những phép tính sơ khai trong lịch sử phát triển học và nghiên cứu toán học của loài người. Điều này nghe có vẻ hiển nhiên như khi ta còn nói rằng việc một cây bút chì như là tiên đề vậy. 

Tuy vây, thật bất ngờ khi mãi đến thế kỉ thứ . . . các nhà toán học mới tổng quát cấu trúc đại số . . . bắt đầu từ tiên đề Peano về . . . cho đến khi hai nhà toán học Russell và Whitehead trong tác phẩm . . . xuất bản . . .ở trang . . . mới chứng minh định lý 1 + 1 = 2. 

\end{document}
```

(? Ảnh các nhà toán học Peano, Russell, Whitehead)

Điều này cũng tương tự, đối với việc người dùng viết kí hiệu của các đơn vị đo lượng cơ bản như khối lượng 

```latex
70kg
```

vận tốc 

```latex
5 cm/s
```

khoảng cách

```latex
10 m 
```

tần số

```latex
50hz
```

các biến x, y, z, ..vv.., ẩn số a, b, ...vv... được gọi chung là các [chữ cái thông thường]() 

```latex
y = ax + b 
```

..vv..

Tập hợp các kí hiệu thông thường trên có thể được gõ trực tiếp trên bàn phím, người dùng có thể xem lại bài . . . (? bài học nào trong chủ đề latex này) 

Tuy vậy, để người dùng có thể viết phần toán học có các [kí hiệu, chữ cái toán học đặc biệt]() ở mức độ phức tạp hơn. Ví dụ nếu người dùng muốn viết [chữ cái Hy Lạp]() $\sigma$ (đọc là sigma), [hằng số Dirac]() $\hbar$ (đọc là h-bar), toán tử số học ($\cdot$), [toán tử quan hệ]() $\ge$ (đọc là lớn hơn hoặc bằng), viết [phân số]() $\dfrac{\hbar}{2}$, [chỉ số dưới]() $x, p$ trong phương trình toán học từ nguyên lý bất định Heisenberg (? tên tiếng Anh là gì). . . (? nguyên lý này nói về vấn đề gì trong vật lý) sau đây: 

$$
\sigma_{x} \cdot \sigma_{p} \ge \frac{\hbar}{2} 
$$

Vì những kí hiệu, chữ cái đó không được hiện hữu sẵn trên bàn phím (thậm chí nếu có, thì hệ thống đôi khi sẽ hiểu các kí hiệu đó được sử dụng cho mục đích khác trong LaTeX (? vì sao hệ thống bị nhầm lẫn với các kí hiệu đó), xem lại bài học [kí hiệu đặc biệt]() để hiểu rõ lại chi tiết), nên chúng ta không thể gõ được trực tiếp chúng vào trong phần soạn thảo LaTeX. 

Thay vào đó, người dùng cần phải viết các kí hiệu đó dưới dạng một số lệnh nhất định được hệ thống cài đặt sẵn mặc định trực tiếp hoặc phải khai báo các package nhất định mà nhất định người dùng sẽ bắt gặp rất nhiều ở các bài học về toán học ở phía trước đang chờ đón mọi người . . . (? viết lại), 

```tex
\documentclass{article}

\usepackage[utf8]{vietnam}

\begin{document}

Để viết được chữ cái Hy Lạp \(\sigma\) ta sẽ sử dụng lệnh \verb|\sigma|. 

\vspace{0.5em}

Để viết được hằng số Dirac \(\hbar\) ta sẽ sử dụng lệnh \verb|\hbar|. 

\vspace{0.5em}

Toán tử số học . . .(viết tiếp sau)

\end{document}
```

thì mới có thể hiển thị được ở trong trang tài liệu. 

$\sigma$, . . .(? . . .điền vào sau)

Hơn nữa, so với việc viết 1 + 1 = 2, 70kg, 5 cm/s, 10 m, ..vv.. nếu người dùng viết trực tiếp các lệnh trên vào trong phần soạn thảo LaTeX như đoạn mã sau: 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam}
\begin{document}

Phương trình toán học từ nguyên lý bất định Heisenberg trong cơ học lượng tử . . . (? trình bày tiếp)

\sigma_{x} \cdot \sigma_{p} \ge \frac{\hbar}{2} 

trong đó \sigma_{x} là độ lệch chuẩn của x, \sigma{p} là độ lệch chuẩn của p . . .

\end{document}
```

thì khi biên dịch (compile) sang trang tài liệu, hệ thống sẽ lập tức báo lỗi `! Missing $ inserted` ở dòng thứ 7 và 9 ở đoạn mã trên. 

(? . . . Ảnh báo lỗi) 

Ngoài ra, phương trình được hiện thị ở trong trang tài liệu từ đoạn mã trên cũng không được căn chỉnh tự động ở một dòng riêng biệt như trong một trang sách được cắt từ cuốn học vật lý về cơ học lượng tử ["Introduction to quantum mechanics"](https://5.imimg.com/data5/SELLER/Doc/2025/3/498430108/LF/IH/PO/241144082/introduction-to-quantum-mechanics-3rd-edition-book.pdf) tái bản lần thứ ba, trang 19 được viết bởi nhà vật lý David J.Griffiths sau đây: 

<div align="center">
<img src="https://hackmd.io/_uploads/HyvZn4v5Gx.jpg" alt="David J.Griffiths"> 
</div>

(? . . . thay ảnh mới sau)

Thâm chí, nếu người dùng viết trực tiếp các kí hiệu, chữ cái trên vào cùng chung dòng với văn bản  (? . . . sẽ dẫn đến vấn đề gì, vì sao)  (**Nháp** . . . Người dùng có thể thấy, . . .  vì hệ thống lúc này đang hiểu . . . (?hiểu gì). Để có thể khắc phục việc viết văn bản trong toán học, người dùng có thể xem lướt qua nhanh tạm thời bài học [văn bản trong toán học]() đây, nhưng điều quan trọng mà người dùng cần phải tập trung ở đây, lúc này là việc làm sao để chúng ta có thể viết các kí hiệu, chữ cái phức tạp đó sao cho hệ thống có thể hiểu được là ta đang muốn đâu là văn bản thông thường và đâu là văn bản toán học.)

Từ hai vấn đề cơ bản mà người viết đã nêu trên, người dùng có thể thấy rằng, để viết được một hoặc [nhiều phương trình toán học]() có các kí hiệu, chữ cái phức tạp (? lặp từ quá nhỉ), chúng cần phải được đặt vào trong lệnh, môi trường riêng biệt khác, để hệ thống có thể dễ dàng phân biệt, xác nhận . . . (? đúng ko nhỉ) nhằm phân tách việc đâu là văn bản chữ thông thường, đâu là văn bản toán học, giúp hiển thị chính xác các kí hiệu, chữ cái toán học mà người dùng mong muốn xuất hiện trên trang tài liệu, khi biên dịch (compile) từ phần soạn thảo LaTeX.

. . . (giới thiệu về inline math, display đây)

. . . và LaTeX cung cấp đầy đủ hai chế độ trình bày toán học chính đó, gồm:

+ `inline math`(**toán học nội tuyến**): được sử dụng để viết các biểu thức, kí hiệu toán học nằm trong cùng với đoạn văn bản.
+ `display math`(**toán học hiển thị**): được sử dụng để viết các biểu thức, kí hiệu toán học không thuộc ở đoạn văn và được trình bày trên các dòng riêng biệt. 

<div align="center">
<img src="#" alt="Heisenberg">
</div>
<center>Nhà vật lý người Đức Werner Heisenberg</center>

---

###  inline math: 

Để viết toán học ở chế độ **inline math**, người dùng cần phải viết chúng vào bên trong một trong ba cách sau: 

1. Một cặp dấu đô la đơn:`$...$`
2. Một cặp dấu ngoặc tròn  `\(...\)`
3. Môi trường toán học (`math`)

```latex
\begin{math} 
. . . 
\end{math}
```

Điều này có nghĩa là người dùng có thể viết phương trình toán học nổi tiếng từ định lý Pythagoras về mối quan hệ giữa hai cạnh góc vuông và một cạnh huyền trong một tam giác vuông ở chế độ **inline math** bằng một cặp dấu đô la đơn 

```latex
\documentclass{article}

% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}

\begin{document}

Phương trình định lý Pythagoras: $x^2 + y^2 =z^2$

\end{document}
```

hoặc cũng có thể là bằng một cặp dấu ngoặc tròn

```latex

\documentclass{article}

% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}

\begin{document}

Phương trình định lý Pythagoras: \(x^2 + y^2 =z^2\)

\end{document}
```

hay là bằng môi trường `math` 

```latex
\documentclass{article}

% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}

\begin{document}

Phương trình định lý Pythagoras: 
\begin{math} 
x^2 + y^2 = z^2
\end{math}

\end{document}
```

mà kết quả cho ra được đều sẽ là giống nhau: 

Phương trình định lý Pythagoras:  $x^2 + y^2 =z^2$ 

Đối với việc viết **inline math** bằng môi trường `math`, nếu nhấn phím Enter xuống dòng, tạo khoảng trống giữa văn băn thông thường "Phương trình định lý Pythagoras" và văn bản toán học phương trình Pythagoras, thì phần toán học nằm trong môi trường `math` đó sẽ nằm bên trong một đoạn văn bản mới. 

```latex
\documentclass{article}

% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}

\begin{document}

Phương trình định lý Pythagoras: 

\begin{math} 
x^2 + y^2 = z^2
\end{math}

\end{document}
```

Điều này đã được trình bày ở phần bài học [xuống dòng văn bản]() 

Việc lựa chọn một trong ba cách trên để viết **inline math** tùy thuộc vào sở thích, thói quen cá nhân của mỗi người dùng. Tuy vậy, quen thuộc, cơ bản và tiện nghi nhất vẫn là hai cách đầu tiên trong ba cách viết trên. 

> [!WARNING]  
> Nếu như người dùng không viết các [kí hiệu, chữ cái toán học đặc biệt]() vào một trong ba cách viết toán học ở chế độ **inline math** trên, thì hệ thống sẽ báo lỗi `! Missing $ inserted.`

Đây là thông báo lỗi mà người viết đã trình bày ở phần [mở đầu]() của bài học. Thông báo lỗi này được hệ thống đưa ra, nhằm nhắc nhở người dùng cần phải viết một số lệnh cho các kí hiệu, chữ cái đặc biệt của toán học, vào bên trong lệnh, môi trường viết toán học, thì khi biên dịch sang trang tài liệu nhằm để tránh . . . (? tránh điều gì) 

Để dễ hình dung, người dùng có thể thấy ở đoạn mã dưới đây (? nhớ đánh số đoạn mã), nếu kí hiệu `^` để viết [chỉ số trên]() được dùng làm kí hiệu mũ 2 của phương trình Pythagoras, nếu không được viết vào trong lệnh, môi trường chế độ **inline math** ở trong phần soạn thảo LaTeX 

```latex
\documentclass{article}

% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}

\begin{document}

Phương trình định lý Pytago: x^2 + y^2 = z^2 

\end{document}
```

thì khi người dùng biên dịch sang trang tài liệu, hệ thống sẽ thông báo lỗi như đã nêu ở chú ý trên (? nhớ đánh số chú ý). 

(? Ảnh báo lỗi đoạn mã trên)

Chú ý trên (? nhớ đánh số chú ý) cũng được áp dụng tương tự đối với việc người dùng viết toán học ở chế độ [display math]().

(**Nháp** . . . Ở ví dụ về phương trình định lý Pythagoras, người dùng chỉ nên hiểu đây chỉ là ví dụ về cách viết **inline math** trong soạn thảo LaTeX. 

Thông thường, **inline math** chỉ nên phù hợp với ... (? với điều gì)

Còn đối với việc viết một phương trình dù ngắn hoặc dài, đều được khuyến nghị (? bên nào khuyến nghịch) là nên căn chỉnh chúng ở một dòng riêng biệt. . . .(? vì sao thế nhỉ) (**Nháp và chỉnh sửa lại quan điểm sau**. . . đối với phương trình dài cũng sẽ gây phức tạp đến văn bản, điều này sẽ được trình bày cụ thể ở trong bài học [tham chiếu chéo phương trình toán học]())

Để làm được điều này, như đã định nghĩa ở phần [mở đầu]() của chủ đề toán học này, chúng ta sẽ viết những phương trình đó vào trong chế độ toán học có tên là **display math**. 

<center>
    <img src="https://hackmd.io/_uploads/S1ciSSwqMe.jpg" alt="Pythagoras" height="700">
    <p>
        Triết gia và nhà toán học người Hy Lạp cổ đại xứ Samos Pythagoras
    </p>
</center>


---

###  display math:

Để viết toán học ở chế độ **display math**, người dùng cần viết chúng vào bên trong một trong ba cách sau:

1. Một cặp dấu đô la kép: `$$...$$`
2. Một cặp dấu ngoặc vuông: `\[...\]`
3. Môi trường `displaymath`: 

```latex
\begin{displaymath} 
. . . 
\end{displaymath}
```

Tương tự như **inline math**, tùy thuộc vào sở thích, thói quen cá nhân của mỗi người dùng, mà để có thể lựa chọn một trong ba cách trên để viết toán học ở chế độ **display math**, mà vẫn đảm bảo kết quả cho ra được vẫn sẽ là giống nhau. (? Quan điểm này cũng sẽ được thay đổi chút ít khi học lập trình [marco](), nhưng trước mắt ta hãy cứ tiếp tục với vấn đề này đi đã)

Ví dụ về việc viết toán học ở chế độ `display math` với phương trình logarithm của một tích là tổng của logarit của các thừa số. Trong đó:

+ Phương trình được viết bên trong `$$...$$`

```latex
\documentclass{article}
% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}
\begin{document} % Sử dụng cặp dấu $$ để viết phương trình logarithm
Phương trình logarithm của một tích là tổng của logarit của các thừa số: 
$$\log_b{xy} = \log_b{x} + \log_b{y}$$
\end{document}
```

+  Phương trình được viết bên trong `\[...\]`

```latex
\documentclass{article} % Sử dụng cặp dấu \[\] để viết phương trình logarithm
% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}
\begin{document}
Phương trình logarithm của một tích là tổng của logarit của các thừa số: 
\[\log_b{xy} = \log_b{x} + \log_b{y}\] 
\end{document}
```

+  Phương trình được viết bên trong môi trường `displaymath`: 

```latex
\documentclass{article}
% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}
\begin{document}
Phương trình logarithm của một tích là tổng của logarit của các thừa số: 
\begin{displaymath} % Sử dụng môi trường displaymath để viết phương trình logarithm
\log_b{xy} = \log_b{x} + \log_b{y}\
\end{displaymath}
\end{document}
```

Kết quả cho ra được từ ba viết cách trên, vẫn sẽ xuất hiện ở trong trang tài liệu là 

$$
\log_b{xy} = \log_b{x} + \log_b{y}
$$

Để viết các phương trình có số được đánh ở bên cạnh theo thứ tự tăng dần, nhằm về sau giúp người dùng [tham chiếu chéo phương trình]() , người dùng lúc này sẽ sử một môi trường mới là có tên là `equation`:

```latex
\begin{equation} 
. . . 
\end{equation}
```

Nếu như chúng ta thay lệnh, môi trường `displaymath` ở ví dụ (? . . . đánh số thứ tự), bằng môi trường mới là `equation`, thì người dùng có thể thấy rằng phương trình logarithm trên lúc này 

```latex
\documentclass{article}
% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}
\begin{document}
Phương trình logarithm của một tích là tổng của logarit của các thừa số:
\begin{equation} % Sử dụng môi trường equation để đánh số thứ tự ở phương trình logarit
\log_b{xy} = \log_b{x} + \log_b{y}
\end{equation}
\end{document}
```

sẽ được hệ thống tự động đánh thêm một số thứ tự mặc định bắt đầu từ (1) đến số thứ tự tăng dần theo số lượng phương trình toán học có được viết vào trong môi trường `equation` ở bên trong phần soạn thảo LaTeX. Và số thứ tự đó cũng mặc định được nằm ở bên phải của phần toán học đó có trong trang tài liệu. 


Trong một số tài liệu toán học, đôi khi người dùng cũng thế thấy rằng số thứ tự được đánh bên cạnh phần toán học đó nằm ở bên trái thay vì bên phải mặc định như ở hình dưới đây 

<div align="center"> 
    <img src="https://hackmd.io/_uploads/rJy0qHD5Gx.jpg" alt="Kakeya">
</div>

<center>Ảnh được cắt từ trang 1 bài báo toán học <a src="https://drive.google.com/file/d/1dlpgd5Q5AAOsaCFQK5MGRisJNUPmgxFu/view?usp=sharing" target="_blank">"A STREAMLINED PROOF OF THE KAKEYA SET CONJECTURE IN \(\mathbb{R^3}\)</a> của ba nhà toán học <a src="https://math.mit.edu/~lguth/" target="_blank">Larry Guth</a>, <a src="https://sites.google.com/view/hongwang/home" target="_blank">Vương Hồng</a>, <a src="https://jzahl.github.io/" target="_blank">Joshua Zahl</a></center>

<div align="center">
	<img src="LaTeX-Library-project-v1.0.0/b. Lectures notes/Mathematics/images math/Guth Hong Zahl.jpg" alt="Guth Hong Zahl">
</div>
<center>Nhà toán học Lary Guth, nhà toán học Vương Hồng và nhà toán học Joshua Zahl</center>

Để chuyển vị trí số thứ tự đó nằm từ bên phải sang bên trái như hình . . . (Số hình), người dùng chỉ cần thêm `options` là 

```latex
leqno
```

ở phần khai báo lớp tài liệu (`documentclass`). Và sau đó vẫn viết phương trình toán học vào bên trong môi trường `equation`. 

```latex
\documentclass[leqno]{article} % 

% --- Cấu hình ngôn ngữ tiếng Việt ---
\usepackage[utf8]{vietnam}

\begin{document}

Phương trình logarithm của một tích là tổng của logarit của các thừa số:

\begin{equation} % 
    \log_b{xy} = \log_b{x} + \log_b{y}
\end{equation}

\end{document}
```

Nếu như người dùng không muốn xuất hiện số thứ tự bên cạnh phương trình toán học, thì người dùng có thể quay lại ba cách đầu tiên mà người viết đã hướng dẫn ban đầu khi viết toán học ở chế độ [`display math`](), hoặc người dùng cũng có thể sử dụng một cách mới sau. 

Trước tiên người dùng nhớ cần phải khai báo package

```latex
\usepackage{amsmath}
```

ở phần . . . (? vị trí đặt lệnh `amsmath` trong cấu trúc soạn thảo LaTeX) (? package amsmath này là gì ? mục đích của package này là gì ?)

(**Nháp** . . . Package `amsmath` còn cung cấp cho người dùng một số tùy chọn để sắp xếp và hiển thị bố cục phương trình toán học sao cho phù hợp với tài liệu người dùng, ngay cả khi các phương trình rất dài hoặc nếu người dùng phải đưa nhiều phương trình vào cùng một dòng, để tránh việc viết phương trình có thể thiếu tính linh hoạt, dẫn đến việc chồng chéo hoặc thậm chí cắt bớt một phần phương trình khi nó quá dài [?].)

. . . (*viết sau*) https://www.overleaf.com/learn/latex/Aligning_equations_with_amsmath

Tiếp đến, người dùng chỉ cần thêm dấu `*` vào bên trong dấu ngoặc nhọn `{}` của môi trường `equation` là phương trình logarithm ở ví dụ . . .lúc này  sẽ không còn xuất hiện số thứ tự bên cạnh ở trong trang tài liệu nữa:  

```latex
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\begin{equation*} % Sử dụng môi trường equation* để viết phương trình logarit
\log_b{xy} = \log_b{x} + \log_b{y}
\end{equation*}
\end{document}
```

Kết quả lúc này ta nhận được giống với ba cách đầu tiên trên: 

$$
\begin{equation*}
\log_b{xy} = \log_b{x} + \log_b{y}
\end{equation*}
$$

Việc thêm dấu `*` vào bên trong dấu ngoặc nhọn của môi trường, cũng được áp dụng tương tự đối với các môi trường khác như môi trường `aligned` (xem ở bài học (? . . . tên bài học đó là gì)), . . . vv . . . (viết tiếp)

**(?)** Câu hỏi lúc này chúng ta cần đặt ra ở đây là điểm khác biệt của môi trường `equation*` và `displaymath` là gì ? Nên sử dụng chúng trong trường hợp nào ? (xem qua issues đây https://github.com/Namlete102/LaTeX-Library-project/issues/1) 

> [!WARNING]
> Khi người dùng viết toán học dù ở chế độ `inline math` hay `display math`, người dùng không được phép để các biểu thức, toán tử, kí hiệu, chữ cái đặc biệt toán học có các khoảng trống ở mỗi dòng. Nếu không, thì hệ thống cũng sẽ báo lỗi `Missing $ inserted`

Nếu chúng ta để khoảng trống giữa các dòng biểu thức $\log_b{xy}$  và $= \log_b{x} + \log_b{y}$ như đoạn mã (? . . . số thứ tự đoạn mã) sau đây 

```latex
\documentclass{article}

\begin{document}

\[
\log_b{xy} 

= 
\log_b{x} + \log_b{y}
\]

\end{document}
```

thì hệ thống sẽ lập tức báo lỗi `Missing $ inserted` ở dòng 5 và 7. 

. . . (? ảnh báo lỗi) 

Vì lúc này, hệ thống đang hiểu người dùng để khoảng trống như vậy là nhằm [xuống dòng đoạn văn bản](). Vậy nên ở dòng thứ 5 của đoạn mã đang thiếu `\]` để tạo thành một cặp dấu `\[\]` nhằm viết `display math`. Điều này cũng tương tự đối với dòng thứ 7 của đoãn mã, đang thiếu `\[`, cũng để tạo thành một cặp dấu `\[\]` nhằm viết **display math**.

. . . (? trình bày gì nhỉ để kết nối đoạn trên và dưới đoạn mã dưới đây)

```latex
\documentclass{article}
\begin{document}

\[
\log_b{xy} 
\] % . . . .
\[ % . . . . 
= \log_b{x} + \log_b{y}
\]

\end{document}
```

$$
\log_b{xy} 
$$
$$
= \log_b{x} + \log_b{y}
$$

Cách sửa ở đoạn mã . . . (? đánh số đoạn mã) chỉ giúp người dùng có thể hình dung, để hiểu được điều mà người viết trình bày ở trên. Vậy nên, điều này sẽ không phải là cách mà chúng ta cố gắng đưa về đầy đủ, chính xác với phương trình logarithm đây.

Để khắc phục được lỗi ở đoạn mã (? . . . đánh số đoạn mã), người dùng có thể viết gọn lại phương trình như lúc ban đầu . . . (? trình bày chưa rõ cần viết lại)

```latex
\documentclass{article}
\begin{document}
\[\log_b{xy} =  \log_b{x} + \log_b{y}\]
\end{document}
```
 
hoặc thêm [chú thích]() vào khoảng trống giữa hai biểu thức đó 

```latex
\documentclass{article}
\begin{document}
\[
\log_b{xy} 
% Chú thích này sẽ lấp lại dòng trống
= \log_b{x} + \log_b{y}
\]
\end{document}
```

hoặc đơn giản hơn là người dùng chỉ cần xóa đi khoảng trắng dòng thứ 5 đoạn mã là xong

```latex
\documentclass{article}
\begin{document}
\[
\log_b{xy} 
= 
\log_b{x} + \log_b{y}
\]
\end{document}
```

mà kết quả cho ra được đều vẫn sẽ là như sau:

$$
\log_b{xy} 
% Chú thích này sẽ lấp lại dòng trống
= \log_b{x} + \log_b{y}
$$

Đối với các bài viết . . . (? . . . phần toán học được đánh số 1.1, ..vv..) (đang viết ví dụ tại đây https://www.texpage.com/project/user/6b3729dd-7669-4c54-9f27-b53a521a0cd5/be79ef56-b97e-44ac-a215-add1800d4c80 và viết phần bài học ở [[Toán]].)

Để tham chiếu phương trình toán học, người dùng hãy xem qua phần bài học ở . . . (? gồm những phần bài học nào) trước khi đến với vấn đề chính được tổng hợp và trình bày trong bài học [tham chiếu chéo]() đây. 


<center>
    <img src="https://hackmd.io/_uploads/Bk23WIP9fl.jpg" alt="John Napier">
    <p>
        Nhà toán học người Scotland John Napier
    </p>
</center> 

---

###  Tài liệu tham khảo: 

\[1]: Nguồn tham khảo viết toán học ở Overleaf: https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes#Adding_math_to_LaTeX. 

\[2]:  Nguồn tham khảo lời viết này sử dụng ở Wikibook: https://en.wikibooks.org/wiki/LaTeX/Mathematics 


---

## Câu hỏi: 

---

<!-- footnote -->

[^1]: [https://en.wikibooks.org/wiki/LaTeX/Mathematics](https://en.wikibooks.org/wiki/LaTeX/Mathematics)

[^2]: Còn được gọi là hằng số Planck rút gọn . . . (? bổ sung sau) là biến thể từ chữ h là chữ cái Latinh thông thường, có thể được gõ trực tiếp trên bàn phím. 

