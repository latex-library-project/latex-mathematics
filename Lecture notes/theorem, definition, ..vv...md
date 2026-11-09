## Dàn ý: 

. . .  (Dẫn dắt vào bài học và giới thiệu đôi nét ý nghĩa của tiên đề, định nghĩa, định lý, ..vv.. ở phần sau cuốn sách, vì tất nhiên những phần này nên được tìm hiểu riêng, còn bây giờ ta chỉ hiểu cơ bản chúng rằng . . . (? là gì) và cách để viết chúng vào trong soạn thảo LaTeX).   

## Bài học: 

(Sẽ thay bằng một ví dụ mới sau)

### Ý thứ nhất: Cách sử dụng cơ bản

Để viết được tiên đề, định nghĩa, định lý ..vv.. trong soạn thảo LaTeX, trước tiên người dùng sẽ cần phải khai báo chúng vào lệnh 

```latex
\newtheorem{name}{text}
```

trong đó: 

+ `name`: là . . . 
+ `text`: là . . .

(? lệnh này được đặt ở đâu trong cấu trúc soạn thảo latex, giới thiệu thêm đôi nét về lệnh mới này, cũng như lệnh đó có vai trò, ý nghĩa gì trong xuyên suốt trong phần bài học latex này)  

Khi biên dịch sang trang tài liệu, nếu như các từ tiên đề, định nghĩa, định lý ..vv.. được viết bằng ngôn ngữ tiếng Anh, thì các từ đó cũng sẽ xuất hiện trong trang tài liệu cũng sẽ là tiếng Anh. 

Ví dụ về lệnh `newtheorem` nhằm tạo môi trường **theorem** với định lý Gauss - Wantzel về số cạnh của đa giác đều có thể được dựng bởi thước và compa. Trong đó, từ định lý được viết bằng tiếng Anh:  

```tex
\documentclass{article}
	
% --- CẤU HÌNH GÓI & MÔI TRƯỜNG ---
% Sử dụng gói vietnam để hỗ trợ gõ tiếng Việt trong LaTeX
\usepackage[utf8]{vietnam}
	
% Khai báo môi trường Định lý và Định nghĩa bằng tiếng Anh
\newtheorem{theorem}{Theorem}
	
\begin{document}
	
% ==========================================
% SECTION: ĐỊNH LÝ GAUSS - WANTZEL
% ==========================================
\begin{theorem}
% Nội dung định lý về điều kiện dựng hình đa giác đều bằng thước và compa
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức toán dạng khối (display style)
\[
	n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Giải thích các tham số trong công thức (k có thể bằng 0 nên dùng số nguyên không âm)
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}
	
\end{document}
```

Điều này cũng được áp dụng tương tự với tất cả với [ngôn ngữ khác](). Chẳng hạn, để viết các từ "định lý", "định nghĩa" ..vv.. đang là tiếng Anh sang tiếng Việt. Trước tiên, người dùng cần phải khai báo package [ngôn ngữ tiếng Việt ]().

```tex
% Sử dụng gói vietnam để hỗ trợ gõ tiếng Việt tốt hơn trong LaTeX
\usepackage[utf8]{vietnam}
```

Sau đó người dùng chỉ cần gõ lại từ "theorem" (tiếng Anh) sang từ "định lý" (tiếng Việt) ở `text`.

```tex
% Khai báo môi trường Định lý và Định nghĩa bằng tiếng Việt
\newtheorem{theorem}{Định lý}
```

Quay trở lại ví dụ trên, lúc này từ "theorem" bên tiếng Anh sẽ được hiển thị trên trang tài liệu là từ "định lý" bên tiếng Việt:

```tex
\documentclass{article}
	
% --- CẤU HÌNH GÓI & MÔI TRƯỜNG ---
% Sử dụng gói vietnam để hỗ trợ gõ tiếng Việt trong LaTeX
\usepackage[utf8]{vietnam}
	
% Khai báo môi trường Định lý và Định nghĩa bằng tiếng Anh
\newtheorem{theorem}{Định lý}
	
\begin{document}
	
% Định lý Gauss - Wantzel
\begin{theorem}
% Nội dung định lý về điều kiện dựng hình đa giác đều bằng thước và compa
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức toán dạng khối (display style)
\[
	n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Giải thích các tham số trong công thức (k có thể bằng 0 nên dùng số nguyên không âm)
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}
	
\end{document}
```

>[!NOTE]
> Người dùng nên đồng bộ việc trình bày tài liệu bằng ngôn ngữ nào thì khởi tạo môi trường theo đúng ngôn ngữ trình bày đó. 

Thậm chí, người dùng cũng có thể viết lại từ "theorem" ở `name` thành từ "định lý" mà không cần phải khai báo package ngôn ngữ tiếng Việt. 

```tex
\documentclass{article}

% --- CẤU HÌNH GÓI & MÔI TRƯỜNG ---
% Sử dụng bảng mã utf8 để gõ tiếng Anh hoặc ký tự đặc biệt bình thường
\usepackage[utf8]{inputenc}

% Khai báo môi trường "Theorem" (Định lý) và "Definition" (Định nghĩa) trong tiếng Anh
\newtheorem{định lý}{Theorem}

\begin{document}

% ==========================================
% SECTION: ĐỊNH LÝ GAUSS - WANTZEL
% ==========================================
\begin{định lý}
% Nội dung định lý về điều kiện dựng hình đa giác đều bằng thước và compa
The division of a circle into $n$ equal parts using a straightedge and compass is possible if and only if
% Công thức hiển thị ở dạng khối (display math mode)
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Giải thích các biến trong công thức
where $k$ is a non-negative integer and $p_1, p_2, \dots, p_t$ are distinct Fermat primes.
\end{định lý}

\end{document} 
```

Đây chỉ là ví dụ vui và tất nhiên thì như đã nêu ở phân lưu ý trên, ta nên đồng bộ ngôn ngữ bên trong khởi tạo môi trường với ngôn ngữ trình bày. 

Anh - Anh: 

```tex
\documentclass{article}

% --- CẤU HÌNH GÓI & MÔI TRƯỜNG ---
% Sử dụng bảng mã utf8 để gõ tiếng Anh hoặc ký tự đặc biệt bình thường
\usepackage[utf8]{inputenc}

% Khai báo môi trường "Theorem" (Định lý) và "Definition" (Định nghĩa) trong tiếng Anh
\newtheorem{theorem}{Theorem}

\begin{document}

% ==========================================
% SECTION: ĐỊNH LÝ GAUSS - WANTZEL
% ==========================================
\begin{theorem}
% Nội dung định lý về điều kiện dựng hình đa giác đều bằng thước và compa
The division of a circle into $n$ equal parts using a straightedge and compass is possible if and only if
% Công thức hiển thị ở dạng khối (display math mode)
\[
    n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Giải thích các biến trong công thức
where $k$ is a non-negative integer and $p_1, p_2, \dots, p_t$ are distinct Fermat primes.
\end{theorem}

\end{document} 
```

Việt - Việt: 

```tex
\documentclass{article}
	
% --- CẤU HÌNH GÓI & MÔI TRƯỜNG ---
% Sử dụng gói vietnam để hỗ trợ gõ tiếng Việt trong LaTeX
\usepackage[utf8]{vietnam}
	
% Khai báo môi trường Định lý và Định nghĩa bằng tiếng Anh
\newtheorem{định lý}{Định lý}
	
\begin{document}
	
% Định lý Gauss - Wantzel
\begin{định lý}
% Nội dung định lý về điều kiện dựng hình đa giác đều bằng thước và compa
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức toán dạng khối (display style)
\[
	n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Giải thích các tham số trong công thức (k có thể bằng 0 nên dùng số nguyên không âm)
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{định lý}
	
\end{document}
```

. . . (? chưa biết dẫn dắt sao cho đúng, vì đang bí từ, nhưng cụ thể thì tiếng Anh vẫn là ngôn ngữ chung, nên ta vẫn khởi tạo môi trường với `text` là tiếng Anh cho quen thuộc với các bài học trước đó và về sau, còn nội dung thì vẫn là tiếng Việt.)

Anh - Việt: 

```tex
\documentclass{article}
	
% --- CẤU HÌNH GÓI & MÔI TRƯỜNG ---
% Sử dụng gói vietnam để hỗ trợ gõ tiếng Việt trong LaTeX
\usepackage[utf8]{vietnam}
	
% Khai báo môi trường Định lý và Định nghĩa bằng tiếng Anh
\newtheorem{theorem}{Định lý}
	
\begin{document}
	
% Định lý Gauss - Wantzel
\begin{theorem}
% Nội dung định lý về điều kiện dựng hình đa giác đều bằng thước và compa
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức toán dạng khối (display style)
\[
	n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Giải thích các tham số trong công thức (k có thể bằng 0 nên dùng số nguyên không âm)
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}
	
\end{document}
```

---

### Ý thứ hai: Viết kèm theo tên gọi định lý đó  

Bên cạnh môi trường viết tiên đề, định nghĩa, định lý , ..vv.. mà ta khai báo bằng lệnh `\newtheorem`, ta có thể thêm tên tác giả gốc, hoặc chú thích thêm của định lý đó. 

Ở **định lý 1** mà ta trình bày trên là định lý Gauss về đa giác đều , được do chính nhà toán học Gauss đưa ra, tuy ông ... (? kèm theo lịch sử của định lý đó) bằng cách thêm nội dung vào bên trong dấu ngoặc vuông `[]` vào bên trong môi trường định lý mà ta vừa khai báo. 

```tex
\begin{theorem}
[Gauss] % 
% Nội dung định lý về điều kiện dựng hình đa giác đều bằng thước và compa
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức toán dạng khối (display style)
\[
	n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Giải thích các tham số trong công thức (k có thể bằng 0 nên dùng số nguyên không âm)
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}
```

```tex
\documentclass{article}
	
% --- CẤU HÌNH GÓI & MÔI TRƯỜNG ---
% Sử dụng gói vietnam để hỗ trợ gõ tiếng Việt trong LaTeX
\usepackage[utf8]{vietnam}
	
% Khai báo môi trường Định lý và Định nghĩa bằng tiếng Anh
\newtheorem{theorem}{Định lý}
	
\begin{document}
	
% Định lý Gauss cho đa giác đều
\begin{theorem}
[Gauss]
% Nội dung định lý về điều kiện dựng hình đa giác đều bằng thước và compa
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức toán dạng khối (display style)
\[
	n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Giải thích các tham số trong công thức (k có thể bằng 0 nên dùng số nguyên không âm)
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}
	
\end{document}
```

Nếu người dùng viết . . . (? chưa biết mô tả sao)

```tex
\begin{theorem}
% Nội dung định lý về điều kiện dựng hình đa giác đều bằng thước và compa
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức toán dạng khối (display style)
\[
	n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Giải thích các tham số trong công thức (k có thể bằng 0 nên dùng số nguyên không âm)
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}
[Gauss] % 
```

hoặc

```tex
\begin{theorem}

[Gauss]  
% Nội dung định lý về điều kiện dựng hình đa giác đều bằng thước và compa
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức toán dạng khối (display style)
\[
	n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Giải thích các tham số trong công thức (k có thể bằng 0 nên dùng số nguyên không âm)
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}
```

thì hệ thống sẽ hiểu `[Gauss]` cũng là nội dung bên trong phần định nghĩa đó, nên sẽ không thêm chú thích bên cạnh tiêu đề định lý.

Ta chỉ cần để từ đó như cách đã hướng dẫn (? mô tả chán quá) và không nên khoảng cách . . . bằng cách xóa đi dòng trắng đó, hoặc thêm chú thích. 

Tuy vậy, khuyến khích nên để . . . bên cạnh lệnh `\begin{}` 

```tex
\begin{theorem}[Gauss]  
% Nội dung định lý về điều kiện dựng hình đa giác đều bằng thước và compa
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức toán dạng khối (display style)
\[
	n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Giải thích các tham số trong công thức (k có thể bằng 0 nên dùng số nguyên không âm)
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}
```

---

### Ý thứ ba: Tên gọi chính của định lý đó

Người dùng cũng có thể viết ở `text` là tên gọi chính của định lý, định nghĩa, ..vv.. đó thay vì chỉ hiện từ "định nghĩa", "định lý", ..vv.. thông thường, mới kèm theo tên gọi định lý, định nghĩa đó (? viết lại đoạn "thông thường, mới kèm . . .") như ví dụ trên.

Cụ thể, ta có thể viết lại "**Định lý 1 (Gauss)**" thành "**Định lý Gauss**".  

```tex
\newtheorem{theorem}{Định lý Gauss}
```

Áp dụng điều này vào lại ví dụ . . . , lúc này ta được: 

```tex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . . 
\usepackage{amsmath}

% Đặt tên tiêu đề hiển thị cho định lý và định nghĩa
\newtheorem{theorem}{Định lý Gauss - Wantzel}
\newtheorem{definition}{Số nguyên tố Fermat}

\begin{document}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

\end{document}
```

---

### Ý thứ tư: Tránh việc bị lặp lại với việc khai báo môi trường tên gọi chính của định lý đó

Trong trường hợp người dùng muốn viết định lý mới, nếu như người dùng sử dụng lại môi trường **theorem** đã được định nghĩa ban đầu, thì ở phần tiêu đề định lý mới đó vẫn sẽ xuất hiện "Định lý Gauss - Wantzel" như ở định lý . . . (? Hai định lý gì nhỉ)  

```tex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . . 
\usepackage{amsmath}

% Đặt tên tiêu đề hiển thị cho định lý và định nghĩa
\newtheorem{theorem}{Định lý Gauss - Wantzel}
\newtheorem{definition}{Số nguyên tố Fermat}

\begin{document}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

% Định lý F_5 là hợp số 

\begin{theorem}
   Số Fermat $F_5$ là hợp số
\end{theorem} 

% Định lý . . . 

\begin{theorem}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
    3^{\frac{F_n -1}{2}} \equiv -1 \pmod{F_n}.
    \end{equation*}
\end{theorem} 

\end{document}

```

Để khắc phục được điều trên, người dùng cần phải định nghĩa một môi trường mới cho định lý. 

Cần phải đảm bảo rằng, nếu như người dùng đã định nghĩa môi trường định lý với từ "theorem" ở  `name`, thì chúng không được lặp lại lần nữa khi người dùng muốn sử dụng chúng để viết một định lý khác. 

Điều này cũng áp dụng tương tự đối với định nghĩa (definition), ..vv.. 

Nếu như người dùng định nghĩa môi trường định lý với từ **theorem** đã được sử dụng ở môi trường định lý Gauss - Wantzel, thì hệ thống sẽ báo lỗi **Command \theorem already defined.**  như ở ví dụ . . . dưới đây: 

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . . 
\usepackage{amsmath}

% Đặt tên tiêu đề hiển thị cho định lý và định nghĩa
\newtheorem{theorem}{Định lý Gauss - Wantzel}
\newtheorem{theorem}{Định lý} % từ theorem ở lệnh đây bị trùng với theorem ở lệnh trên nó. (? Viết lại cmt này)
\newtheorem{definition}{Số nguyên tố Fermat}

\begin{document}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

% Định lý F_5 là hợp số 

\begin{theorem}
   Số Fermat $F_5$ là hợp số
\end{theorem} 

% - - - -

\begin{theorem}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
    3^{\frac{F_{n}-1}{2}} \equiv -1 \pmod{F_n}.
    \end{equation*}
\end{theorem}

\end{document}
```

Từ những điều đã nêu ở trên, lúc này để viết một hay nhiều định lý mới khác mà không bị trùng lặp với định lý đã được định nghĩa ban đầu, người dùng chỉ cần đặt tên . . . (? gì, ở đâu) khác đi. 

Cụ thể, thay vì sử dụng đầy đủ tên gọi **theorem**, lúc này ta có thể chỉ cần viết tắt lại thành **thm**: 

```latex
\newtheorem{thm}{Định lý}
```

và ở . . . (? ở đâu trong phần soạn thảo LaTeX) 

```latex
\begin{thm}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
	    3^{\frac{F_n -1}{2}} \equiv -1 \pmod{F_n}.
    \end{equation*}
\end{thm}
```

Từ đây ta viết lại ví dụ . . . :  

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . . 
\usepackage{amsmath}

% Đặt tên tiêu đề hiển thị cho định lý và định nghĩa
\newtheorem{theorem}{Định lý Gauss - Wantzel}
\newtheorem{thm}{Định lý} 
\newtheorem{definition}{Số nguyên tố Fermat}

\begin{document}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

% Định lý F_5 là hợp số 

\begin{theorem}
   Số Fermat $F_5$ là hợp số
\end{theorem} 

% . . . .

\begin{thm}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
    3^{\frac{F_n -1}{2}} \equiv -1 \pmod{F_n}.
    \end{equation*}
\end{thm}

\end{document}

```

Người dùng có thể áp dụng tương tự . . . (? Áp dụng tương tự điều gì) để khắc phục đoạn mã định lý $F_5$ là hợp số.  

```latex
% Định lý F_5 là hợp số 

\begin{thm}
   Số Fermat $F_5$ là hợp số
\end{thm} 
```

### Ý thứ năm: Xóa số bên cạnh định lý (khi viết đầy đủ tên gọi định lý chính đó)

Người dùng có thể thấy rằng, bên cạnh các tên chính của định lý, định nghĩa đó sẽ xuất hiện số thứ tự không cần thiết nằm ở bên cạnh chúng. 

. . . (Để không muốn có số thứ tự bên cạnh. . . ), trước tiên người dùng cần phải khai báo package sau: 

```latex
\usepackage{amsthm} % for theorem environments
```

. . . (? giới thiệu và giải thích đôi chút gói amsthm này)  

Sau đó người dùng chỉ cần thêm dấu `*` ở sau lệnh `\newtheorem` và trước hai dấu ngoặc nhọn (? mô tả hơi chán, nên viết lại sau):  

```latex
\newtheorem*{name}{text}
```

Quay lại với ví dụ . . . lúc này đoạn mã có được: 

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} % for theorem environments

% Đặt tên tiêu đề hiển thị cho định lý, định nghĩa và hệ quả
\newtheorem*{theorem}{Định lý Gauss - Wantzel}
\newtheorem{thm}{Định lý}
\newtheorem*{definition}{Số nguyên tố Fermat}

\begin{document}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

% Định lý F_5 là hợp số 

\begin{thm}
   Số Fermat $F_5$ là hợp số
\end{thm} 

% . . . .

\begin{thm}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
    3^{\frac{F_n -1}{2}} \equiv -1 \pmod{F_n}.
    \end{equation*}
\end{thm}

\end{document}
```

Người dùng có thể thấy rằng, bên cạnh tên "Định lý Gauss - Wantzel" và cũng như là "Số nguyên tố Fermat" không còn xuất hiện số thứ tự bên cạnh nữa. 

### Ý thứ sáu: Cập nhật số thứ tự khi viết môi trường mới

Nếu như người dùng viết một ví dụ ngay sau phần **định lý 2** ở đoạn mã trên: 

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} % for theorem environments

% Đặt tên tiêu đề hiển thị cho định lý, định nghĩa và hệ quả
\newtheorem*{theorem}{Định lý Gauss - Wantzel}
\newtheorem{thm}{Định lý}
\newtheorem*{definition}{Số nguyên tố Fermat}
\newtheorem{example}{Ví dụ}

\begin{document}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

% Định lý F_5 là hợp số 

\begin{thm}
   Số Fermat $F_5$ là hợp số
\end{thm} 

% . . . .

\begin{thm}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
    3^{\frac{F_n -1}{2}} \equiv -1 \pmod{F_n}.
    \end{equation*}
\end{thm}

% . . .

\begin{example}
    \(F_3\) là số nguyên tố. Thật vậy, ta có
    \[
        \begin{split}
            3^{\frac{F_3-1}{2}} & \equiv 3^{128} = 3^3 \cdot (3^5)^{25} \\
                                & \equiv 27 \cdot (-14)^{25} \\ 
                                & \equiv 27 \cdot 14^{24} \cdot (-14) \\ 
                                & \equiv 27 \cdot 19 \equiv 513 \equiv -1 \pmod{257} \\
        \end{split}
    \]
\end{example}

\end{document}
```

người dùng có thể thấy rằng số thứ tự ngay cạnh từ **ví dụ** không được tự cập nhật theo số thứ tự . . . (? viết tiếp)

. . . (? trình bày cách khắc phục)

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} % for theorem environments

% Đặt tên tiêu đề hiển thị cho định lý, định nghĩa và hệ quả
\newtheorem*{theorem}{Định lý Gauss - Wantzel}
\newtheorem{thm}{Định lý}
\newtheorem*{definition}{Số nguyên tố Fermat}
\newtheorem{example}[thm]{Ví dụ}

\begin{document}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

% Định lý F_5 là hợp số 

\begin{thm}
   Số Fermat $F_5$ là hợp số
\end{thm} 

% . . . .

\begin{thm}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
    3^{\frac{F_n -1}{2}} \equiv -1 \pmod{F_n}.
    \end{equation*}
\end{thm}

% . . .

\begin{example}
    \(F_3\) là số nguyên tố. Thật vậy, ta có
    \[
        \begin{split}
            3^{\frac{F_3-1}{2}} & \equiv 3^{128} = 3^3 \cdot (3^5)^{25} \\
                                & \equiv 27 \cdot (-14)^{25} \\ 
                                & \equiv 27 \cdot 14^{24} \cdot (-14) \\ 
                                & \equiv 27 \cdot 19 \equiv 513 \equiv -1 \pmod{257} \\
        \end{split}
    \]
\end{example}

\end{document}
```

### Ý thứ sáu chấm một: Cập nhật số thứ tự theo mục lục

Với bài viết chia [mục lục]() . . . ta chỉ cần thêm các lệnh . . .  tương ứng với phần tiêu đề . . .đó vào . . (? viết tào lao gì vậy)

 Giả sử . . . : Nếu như tiêu đề mục đang được sử dụng là lệnh `\section`, thì ta chỉ cần thêm . . . vào . . . cũng là `section`.  (? viết lại nhé) 

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} 

% Đặt tên tiêu đề hiển thị cho định lý, định nghĩa và hệ quả
\newtheorem*{theorem}{Định lý Gauss - Wantzel}
\newtheorem{thm}{Định lý}[section] 
\newtheorem*{definition}{Số nguyên tố Fermat}
\newtheorem{example}[thm]{Ví dụ}

\begin{document}

% . . . 
\section{Giới thiệu}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% . . . 
\section{Một số tính chất về tính nguyên tố của số Fermat}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

% Định lý F_5 là hợp số 

\begin{thm}
   Số Fermat $F_5$ là hợp số
\end{thm} 

% . . . .

\begin{thm}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
    3^{\frac{F_n -1}{2}} \equiv -1 \pmod{F_n}
    \end{equation*}
\end{thm}

% . . .

\begin{example}
    \(F_3\) là số nguyên tố. Thật vậy, ta có
    \[
        \begin{split}
            3^{\frac{F_3-1}{2}} & \equiv 3^{128} = 3^3 \cdot (3^5)^{25} \\
                                & \equiv 27 \cdot (-14)^{25} \\ 
                                & \equiv 27 \cdot 14^{24} \cdot (-14) \\ 
                                & \equiv 27 \cdot 19 \equiv 513 \equiv -1 \pmod{257} \\
        \end{split}
    \]
\end{example}

\end{document}
```

### Ý thứ bảy chọ: Phân biệt cách trình bày của tiên đề, định nghĩa, định lý, ..vv..

(? Nêu vấn đề vì sao ta lại phải phân biệt định nghĩa, định lý) 

Khai báo package: 

```latex
\usepackage{amsthm} 
```

Nhằm phân biệt được định nghĩa, định lý, ..vv.. trong trang tài liệu toán học người dùng sử dụng lệnh

```latex
\theoremstyle{stylename}
```

trong đó **stylename** gồm các kiểu cơ bản mặc định của hệ thống được tổng hợp ở bảng sau:[^2]

| stylename  | Đặc điểm và công dụng                                                                                                                                                                                 | Ví dụ                                 |
| :--------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- |
| definition | Tiêu đề in đậm, nội dung chữ thường. Được sử dụng trong định nghĩa, điều kiện, vấn đề và đưa ra ví dụ.                                                                                                | **Định nghĩa** 1: Nội dung định nghĩa |
| plain      | Tiêu đề in đậm, nội dung in nghiêng. Được sử dụng trong các định lý, bổ đề, hệ quả, mệnh đề và giả thuyết.                                                                                            | **Định lý 2**: *Nội dung định lý*     |
| remark     | Tiêu đề in nghiêng, nội dung in thường. Được sử dụng trong nhận xét, ghi chú, chú thích (notes), tuyên bố (annotations), trường hợp (claims), lời cảm ơn (acknowledgments) và kết luận (conclusions). | *Nhận xét 3*: Nội dung nhận xét       |

Ví dụ về stylename **definition** với định nghĩa số nguyên tố Fermat 

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} 

% . . . 
\theoremstyle{definition}
\newtheorem*{definition}{Số nguyên tố Fermat}


\begin{document}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

\end{document}
```

Ví dụ về stylename **plain** với các định lý . . . 

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} 

% Đặt tên tiêu đề hiển thị cho định lý, định nghĩa và hệ quả
\theoremstyle{plain}
\newtheorem*{theorem}{Định lý Gauss - Wantzel}
\newtheorem{thm}{Định lý}[section] 


\begin{document}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% Định lý F_5 là hợp số 

\begin{thm}
   Số Fermat $F_5$ là hợp số
\end{thm} 

% . . . .

\begin{thm}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
    3^{\frac{F_n -1}{2}} \equiv -1 \pmod{F_n}
    \end{equation*}
\end{thm}

\end{document}
```

Ví dụ về stylename **remark** với nhận xét về các số nguyên tố Fermat : 

```latex
\documentclass{article}
\usepackage[utf8]{vietnam} % for Vietnamese 
\usepackage{amsthm}
\theoremstyle{remark} 
\newtheorem*{remark}{Nhận xét} 
\begin{document}
\begin{remark}
Fermat nhận ra 5 số Fermat đầu tiên là \(F_0 = 3, F_1 = 5; F_2 = 17, F_3 = 257, F_4 = 65537\) đều là số nguyên tố và ông đã nhận định rằng $F_n$ là số nguyên tố với mọi giá trị của $n$. Tuy nhiên, đến năm 1732, nhà toán học người Thụy Sĩ Leohard Euler đã chứng minh rằng \(F_5\) là hợp số.
\end{remark}
\end{document} 
```

Từ các đoạn mã trên, ta tổng hợp lại được một đoạn mã sau . . .  (? viết lại nhé) 

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} 

% . . . 
\theoremstyle{definition}
\newtheorem*{theorem}{Định lý Gauss - Wantzel}

\theoremstyle{plain}
\newtheorem{thm}{Định lý}[section] 
\newtheorem*{definition}{Số nguyên tố Fermat}
\newtheorem{example}[thm]{Ví dụ}

\theoremstyle{remark} 
\newtheorem*{remark}{Nhận xét} 

\begin{document}

% . . . 
\section{Giới thiệu}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% . . . 
\section{Một số tính chất về tính nguyên tố của số Fermat}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

% . . . 

\begin{remark}
Fermat nhận ra 5 số Fermat đầu tiên là \(F_0 = 3, F_1 = 5; F_2 = 17, F_3 = 257, F_4 = 65537\) đều là số nguyên tố và ông đã nhận định rằng $F_n$ là số nguyên tố với mọi giá trị của $n$. Tuy nhiên, đến năm 1732, nhà toán học người Thụy Sĩ Leohard Euler đã chứng minh rằng \(F_5\) là hợp số.
\end{remark}

% Định lý F_5 là hợp số 

\begin{thm}
   Số Fermat $F_5$ là hợp số
\end{thm} 

% . . . .

\begin{thm}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
    3^{\frac{F_n -1}{2}} \equiv -1 \pmod{F_n}
    \end{equation*}
\end{thm}

% . . .

\begin{example}
    \(F_3\) là số nguyên tố. Thật vậy, ta có
    \[
        \begin{split}
            3^{\frac{F_3-1}{2}} & \equiv 3^{128} = 3^3 \cdot (3^5)^{25} \\
                                & \equiv 27 \cdot (-14)^{25} \\ 
                                & \equiv 27 \cdot 14^{24} \cdot (-14) \\ 
                                & \equiv 27 \cdot 19 \equiv 513 \equiv -1 \pmod{257} \\
        \end{split}
    \]
\end{example}

\end{document}
```

### Ý thứ tám: Bằng chứng (proof)

Bằng chứng (tiếng anh là proof) là . . . (? giải thích nghĩa từ bằng chứng, cũng như phân biệt chứng minh toán học so với các chứng minh ở bên vật lý, hóa học, ...vv...)

Để viết bằng chứng trong soạn thảo LaTeX, người dùng sử dụng môi trường `proof`

```latex
\begin{proof}
. . .
\begin{proof}
```

đã được có trong sẵn package `amsthm` mà ta đã khai báo ở . . . (phần bài học nhân xét mà không đánh số ở trên) 

Ví dụ về môi trường `proof` với việc chứng minh định lý số Fermat $F_5$ là hợp số 

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} 

%  . . .
\theoremstyle{plain}
\newtheorem{thm}{Định lý}

\begin{document}

% Định lý F_5 là hợp số 

\begin{thm}
   Số Fermat $F_5$ là hợp số
\end{thm} 

% Chứng minh định lý F_5 là hợp số

\begin{proof}
Ta thấy rằng 
\[
    \begin{split}
        F_5 &= 2^{32} + 1 \\
            &= 2^4 \cdot 2^{28} + 1 \\ 
            &= . . .
    \end{split}
\]
Kết quả này chứng tỏ \(F_5 \vdots 641\). Vậy \(F_5\) là hợp số. 
\end{proof}

\end{document}
```

### Ý thứ tám chấm một: Q.E.D

Khi hoàn thành xong phần chứng minh cho định lý, mệnh đề, bổ đề, ..vv.. nào đó trong toán học, chúng ta luôn luôn kết lại bằng câu "điều phải chứng minh".

<div align="center">
<img src="LaTeX-Library-project-v1.0.0/images/Q.E.D._(manga)_1.jpg">
</div>

À nhầm cái này mới đúng 

. . .  (? Ảnh) 

hoặc bởi một ô vuông trắng hoặc đen: 

. . . (? Ảnh) 

Điều này bắt nguồn từ . . . (? một chút lịch sử về việc tại sao phải có điều này) và được viết tắt ngắn gọn lại là QED[^1] . 

Để sử dụng từ QED khi kết thúc chứng minh trong soạn thảo LaTeX, người dùng sử dụng lệnh: 

```latex
\renewcommand\qedsymbol{QED}
```

được đặt ở (? ở đâu)

Từ QED trên thông thường được thay thế ngắn gọn lại bằng một [kí hiệu đặc biệt]() ô vuông trắng 

```latex
\renewcommand{\qedsymbol}{$\square$} 
```

hoặc đôi khi là một ô vuông đen 

```latex
\renewcommand\qedsymbol{$\blacksquare$}
```

Các lệnh trên đều phải được đặt trước môi trường `proof` . . . 

. . .  nếu như người dùng muốn thay ô vuông trắng (mặc định) ở . . . thành ô vuông đen: 

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} 
% . . .
\usepackage{amssymb}

%  . . .
\theoremstyle{plain}
\newtheorem{thm}{Định lý}

\begin{document}

% Định lý F_5 là hợp số 

\begin{thm}
   Số Fermat $F_5$ là hợp số
\end{thm} 

% Chứng minh định lý F_5 là hợp số

\renewcommand\qedsymbol{$\blacksquare$} % . . . 

\begin{proof}
Ta thấy rằng 
\[
    \begin{split}
        F_5 &= 2^{32} + 1 \\
            &= 2^4 \cdot 2^{28} + 1 \\ 
            &= . . .
    \end{split}
\]
Kết quả này chứng tỏ \(F_5 \ \vdots \ 641\). Vậy \(F_5\) là hợp số. 
\end{proof}

\end{document}
```

Viết lại đầy đủ từ . . . (? từ đâu (where))

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} 

%  . . .
\theoremstyle{plain}
\newtheorem*{theorem}{Định lý Gauss - Wantzel}
\newtheorem{thm}{Định lý}[section] 

\theoremstyle{definition}
\newtheorem*{definition}{Số nguyên tố Fermat}
\newtheorem{example}[thm]{Ví dụ}

\theoremstyle{remark}
\newtheorem*{remark}{Nhận xét} 

\begin{document}

% . . . 
\section{Giới thiệu}

% --- Phát biểu Định lý Gauss - Wantzel ---
\begin{theorem}
% Phát biểu điều kiện chia đều đường tròn (dựng đa giác đều)
Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
% Công thức phân tích n thành tích các số nguyên tố
\[
n = 2^k \cdot p_1 \cdot p_2 \dots p_t
\]
% Điều kiện của tham số k và các số nguyên tố Fermat p_i
trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
\end{theorem}

% Chứng minh định lý Gauss - Wantzel 

\begin{proof}
Ta thấy rằng . . .(tìm hiểu một chút lý thuyết số nữa nhé)
\end{proof}

% . . . 
\section{Một số tính chất về tính nguyên tố của số Fermat}

% --- Định nghĩa Số nguyên tố Fermat ---
\begin{definition}
% Công thức tổng quát của số Fermat
Một số nguyên có dạng 
\[
F_n = 2^{2^n}+1 
\]
% Điều kiện để F_n là số nguyên tố
được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
\end{definition}

% . . . 

\begin{remark}
Fermat nhận ra 5 số Fermat đầu tiên là \(F_0 = 3, F_1 = 5; F_2 = 17, F_3 = 257, F_4 = 65537\) đều là số nguyên tố và ông đã nhận định rằng $F_n$ là số nguyên tố với mọi giá trị của $n$. Tuy nhiên, đến năm 1732, nhà toán học người Thụy Sĩ Leohard Euler đã chứng minh rằng \(F_5\) là hợp số.
\end{remark}

% Định lý F_5 là hợp số 

\begin{thm}
   Số Fermat $F_5$ là hợp số
\end{thm} 

% Chứng minh định lý F_5 là hợp số

\begin{proof}
Ta thấy rằng . . .(tìm hiểu một chút lý thuyết số nữa nhé)
\end{proof}

% Định lý . . . .

\begin{thm}
    Với $n \geq 1$, số Fermat $F_n = 2^{2^{n}+ 1}$ là số nguyên tố nếu và chỉ nếu
    \begin{equation*}
    3^{\frac{F_n -1}{2}} \equiv -1 \pmod{F_n}
    \end{equation*}
\end{thm}

% Chứng minh . . . . 

\begin{proof}
Ta thấy rằng . . .(tìm hiểu một chút lý thuyết số nữa nhé)
\end{proof} 

% . . .

\begin{example}
    \(F_3\) là số nguyên tố. Thật vậy, ta có
    \[
        \begin{split}
            3^{\frac{F_3-1}{2}} & \equiv 3^{128} = 3^3 \cdot (3^5)^{25} \\
                                & \equiv 27 \cdot (-14)^{25} \\ 
                                & \equiv 27 \cdot 14^{24} \cdot (-14) \\ 
                                & \equiv 27 \cdot 19 \equiv 513 \equiv -1 \pmod{257} \\
        \end{split}
    \]
\end{example}

\end{document}
```

### Ý thứ chín: Tham chiếu chéo tiên đề, định nghĩa, định lý, ..vv..

Để tham chiếu chéo các định lý, định nghĩa, ..vv.. người dùng xem qua bài học [tham chiếu chéo](). 

<div align="center">
	
<img src="LaTeX-Library-project-v1.0.0/images/Fermat Gauss Wantzel.jpg" alt="Fermat Gausss Wantzel">

Hai nhà toán học người Pháp Fermat (trái), Wantzel (phải) và nhà toán học người Đức Gauss (giữa)

</div> 

--- 

### Ý thứ 10 (bổ sung và sẽ cập nhật vào trong bài học chính sau): Viết mệnh đề theo dạng liệt kê: 

Trong một số trường hợp, người dùng không đề cập dụng nội dung đầu của tiên đề, định nghĩa, định lý, ..vv.. đó. Để dễ hình dung, ta cùng xem qua ví dụ sau:  

(? . . .nêu rõ lại nguyên nhân, giải thích vì sao) 

(? . . . đi tìm một ví dụ mới sau)

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} 
% . . .
\usepackage{amssymb}

%  . . .
\theoremstyle{plain}
\newtheorem{proposition}{Mệnh đề}[section]

\begin{document}

\begin{proposition}
	\begin{enumerate}
	    \item Nếu \(a, b \in \mathbb{Z_+}\) là hai số nguyên dương nguyên tố cùng nhau thì ta có \(\phi(ab) = \phi(a)\phi(b)\)
	    \item Nếu \(n = p^m\) là lũy thừa bậc \(m\) của một số nguyên tố \(p\) thì ta có
	    \[
	        \phi(p^m) = (p-1)p^{m-1}
	    \]
	    \item Nếu \(n = p_1^{m_1} \dots p_r^{m_r}\) là lũy thừa bậc \(m\) của một số nguyên tố \(p\) thì ta có
	    \[
	        \phi(p^m) = \prod_{i = 1}^r (p_i - 1)p_i^{m_1 - 1}
	    \]
	\end{enumerate}
\end{proposition}

\end{document}
```


Để khắc phục được điều có hai cách cơ bản sau: 

**Cách 1**: Sử dụng lệnh `\hfill` được đặt bên trong môi trường `proposition` mà ta vừa định nghĩa và trước môi trường `enumerate` trên (? giải thích thêm lệnh `\hfill` này, tham khảo ở bài học đây https://www.overleaf.com/learn/latex/Line_breaks_and_blank_spaces):

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} 
% . . .
\usepackage{amssymb}

%  . . .
\theoremstyle{plain}
\newtheorem{proposition}{Mệnh đề}[section]

\begin{document}

\begin{proposition} \hfill
	\begin{enumerate}
	    \item Nếu \(a, b \in \mathbb{Z_+}\) là hai số nguyên dương nguyên tố cùng nhau thì ta có \(\phi(ab) = \phi(a)\phi(b)\)
	    \item Nếu \(n = p^m\) là lũy thừa bậc \(m\) của một số nguyên tố \(p\) thì ta có
	    \[
	        \phi(p^m) = (p-1)p^{m-1}
	    \]
	    \item Nếu \(n = p_1^{m_1} \dots p_r^{m_r}\) là lũy thừa bậc \(m\) của một số nguyên tố \(p\) thì ta có
	    \[
	        \phi(p^m) = \prod_{i = 1}^r (p_i - 1)p_i^{m_1 - 1}
	    \]
	\end{enumerate}
\end{proposition}

\end{document}
```


**Cách 2**: Thay lệnh `\hfill` ở **cách 1** bằng lệnh mới `\leavemode` . . . (? giải thích thêm lệnh này) 

```latex
\documentclass{article}

% Khai báo font tiếng Việt cho LaTeX
\usepackage[utf8]{vietnam}
% . . .
\usepackage{amsmath}
% . . . 
\usepackage{amsthm} 
% . . .
\usepackage{amssymb}

%  . . .
\theoremstyle{plain}
\newtheorem{proposition}{Mệnh đề}[section]

\begin{document}

\begin{proposition} \leavevmode % Đẩy item 1 xuống 
	\begin{enumerate}
	    \item Nếu \(a, b \in \mathbb{Z_+}\) là hai số nguyên dương nguyên tố cùng nhau thì ta có \(\phi(ab) = \phi(a)\phi(b)\)
	    \item Nếu \(n = p^m\) là lũy thừa bậc \(m\) của một số nguyên tố \(p\) thì ta có
	    \[
	        \phi(p^m) = (p-1)p^{m-1}
	    \]
	    \item Nếu \(n = p_1^{m_1} \dots p_r^{m_r}\) là lũy thừa bậc \(m\) của một số nguyên tố \(p\) thì ta có
	    \[
	        \phi(p^m) = \prod_{i = 1}^r (p_i - 1)p_i^{m_1 - 1}
	    \]
	\end{enumerate}
\end{proposition}

\end{document}
```

## Tài liệu tham khảo: 

\[1]:  Tham khảo viết từ: https://paulwintz.com/mathematical-writing/theorem-like-environments-in-latex/ và bài viết về "[Số nguyên tố Fermat](LaTeX-Library-project-v1.0.0/Toán học/Bib math/pdf/Số nguyên tố Fermat.pdf)" 

---

## Footnote: 

[^1]: Không nên nhầm lẫn với định nghĩa QED ở các lĩnh vực khác: https://en.wikipedia.org/wiki/QED

[^2]: Nguồn viết: [https://www.overleaf.com/learn/latex/Theorems_and_proofs#Reference_guide](https://www.overleaf.com/learn/latex/Theorems_and_proofs#Reference_guide) + [https://en.wikibooks.org/wiki/LaTeX/Theorems#Theorem_styles](https://en.wikibooks.org/wiki/LaTeX/Theorems#Theorem_styles)
