 ## Bài học: 

(Sẽ thay bằng một ví dụ mới sau)

---

### Ý thứ nhất: Cách sử dụng cơ bản

Để viết được tiên đề, định nghĩa, định lý ..vv.. trong soạn thảo LaTeX, trước tiên người dùng sẽ cần phải khai báo chúng vào lệnh 

```tex
\newtheorem{name}{text}
```

trong đó: 

+ `name`: là . . . 
+ `text`: là . . .

(? lệnh này được đặt ở đâu trong cấu trúc soạn thảo latex, giới thiệu thêm đôi nét về lệnh mới này, cũng như lệnh này có vai trò, ý nghĩa gì trong xuyên suốt trong phần bài học latex này)  

Khi biên dịch sang trang tài liệu, nếu như các từ "tiên đề", "định nghĩa", "định lý", ..vv.. được viết bằng ngôn ngữ tiếng Anh, thì các từ đó cũng sẽ xuất hiện trong trang tài liệu cũng sẽ là tiếng Anh. 

Ví dụ về lệnh `newtheorem` nhằm tạo môi trường `lemma` với bổ đề Kuratowski-Zorn . . . (? bổ đề này đóng vai trò gì trong toán học). Trong đó, từ **lemma** được viết bằng tiếng Anh: 

```tex
\documentclass{article}

\newtheorem{lemma}{Lemma}

\begin{document}

\begin{lemma}
    Let P be a partially ordered set and suppose that every chain in P has an upper bound in P. Then P has a maximal member.
\end{lemma}

\end{document}
```

Điều này cũng được áp dụng tương tự với tất cả với [ngôn ngữ khác](). Chẳng hạn, để viết các từ "tiên đề", "định lý", "định nghĩa", ..vv.. đang là tiếng Anh sang tiếng Việt. Trước tiên, người dùng cần phải khai báo package [ngôn ngữ tiếng Việt ]() ở (? ở đâu trong cấu trúc soạn thảo latex): 

```tex
\usepackage{utf8}{vietnam}
```

sau đó chỉ cần viết lại từ "Lemma" ở phần `text` thành "Bổ đề" là xong. Dù phần `name` vẫn để là từ tiếng Anh, nhưng đó chỉ đóng vai trò như là tạo môi trường như bao môi trường khác mà ta đã học ở các bài học khác.

```tex
\documentclass{article}

\usepackage[utf8]{vietnam}

\newtheorem{lemma}{Bổ đề}

\begin{document}

\begin{lemma}
    Cho P là một tập hợp sắp thứ tự riêng phần và giả sử mọi xích trong P đều có một chặn trên trong P. Khi đó P có một phần tử cực đại.
\end{lemma}

\end{document}
```

>[!NOTE]
> Người dùng nên đồng bộ việc trình bày tài liệu bằng ngôn ngữ nào thì khởi tạo phần `text` ở lệnh `newtheorem` theo đúng ngôn ngữ trình bày đó. 

Khi viết "bổ đề" ở hai ví dụ trên, người viết đã đồng bộ đúng ngôn ngữ trình bày, giúp người dùng có thể hình dung được ghi chú ở trên.

---

### Ý thứ hai: Áp dụmg bài học viết toán ở chế độ `in/dis` và tạo danh sách có/ko thứ tự

Viết ví dụ với việc viết toán học ở chế độ **display math** vào trong định lý Euler-Fermat trong ...: 

```tex
\documentclass{article}

\usepackage[utf8]{vietnam}

\newtheorem{theorem}{Định lý}

\begin{document}

\begin{theorem}[Fermat--Euler]
    Cho \(a\) và \(n\) là hai số nguyên tố cùng nhau. Khi đó ta có
    \[
        a^{\phi (n)} \equiv 1 \pmod{n}
    \]
\end{theorem}

\end{document}
```

--- 

### Ý thứ ba: Viết kèm theo tên gọi định lý đó  

Bên cạnh môi trường viết tiên đề, định nghĩa, định lý , ..vv.. mà ta khai báo bằng lệnh `\newtheorem`, ta có thể thêm tên tác giả gốc, hoặc ghi chú thêm gì đó về tiên đề, định nghĩa, định lý , ..vv.. đó. 

Ở **bổ đề 1** mà ta trình bày trên là bổ đề Zorn , được do chính nhà toán học ... đưa ra, tuy ông ... (? kèm theo lịch sử của định lý đó) bằng cách thêm nội dung vào bên trong dấu ngoặc vuông `[]` vào bên trong môi trường định lý mà ta vừa khai báo 

```tex
\begin{lemma}
[Bổ đề Kuratowski-Zorn]
    Cho P là một tập hợp sắp thứ tự riêng phần và giả sử mọi xích trong P đều có một chặn trên trong P. Khi đó P có một phần tử cực đại.
\end{lemma}
```

Tổng hợp đầy đủ lại ta có đoạn mã sau:

```tex
\documentclass{article}

\usepackage[utf8]{vietnam}

\newtheorem{lemma}{Bổ đề}

\begin{document}

\begin{lemma}
[Bổ đề Kuratowski-Zorn]
    Cho P là một tập hợp sắp thứ tự riêng phần và giả sử mọi xích trong P đều có một chặn trên trong P. Khi đó P có một phần tử cực đại.
\end{lemma}

\end{document}
```

>[!NOTE]
> Khi viết nhiều tên tác giả của tiên đề, định nghĩa, định lý , ..vv.. đó, thay vì sử dụng một kí tự `-` (? đọc là sao), chúng ta sẽ gõ hai lần kí tự đó để tạo một kí tự gạch nối . . . (? vì sao thế nhỉ)

Cụ thể thay vì viết 

```tex
[Bổ đề Kuratowski-Zorn]
```

ta sẽ sửa lại bằng hai lần kí tự đó `--`: 

```tex
[Bổ đề Kuratowski--Zorn]
```

Tổng hợp lại ta được: 

```tex
\documentclass{article}

\usepackage[utf8]{vietnam}

\newtheorem{lemma}{Bổ đề}

\begin{document}

\begin{lemma}
[Bổ đề Kuratowski--Zorn]
    Cho P là một tập hợp sắp thứ tự riêng phần và giả sử mọi xích trong P đều có một chặn trên trong P. Khi đó P có một phần tử cực đại.
\end{lemma}

\end{document}
```

Nếu người dùng viết . . . (? chưa biết mô tả sao) 


```tex
\begin{lemma}
    Cho P là một tập hợp sắp thứ tự riêng phần và giả sử mọi xích trong P đều có một chặn trên trong P. Khi đó P có một phần tử cực đại.
    [Bổ đề Kuratowski--Zorn]
\end{lemma}
```

hoặc 

```tex
\begin{lemma}

    [Bổ đề Kuratowski--Zorn]
    Cho P là một tập hợp sắp thứ tự riêng phần và giả sử mọi xích trong P đều có một chặn trên trong P. Khi đó P có một phần tử cực đại.
\end{lemma}
```

thì hệ thống sẽ hiểu `[Gauss]` cũng là nội dung bên trong phần định nghĩa đó, nên sẽ không thêm chú thích bên cạnh tiêu đề định lý.

Ta chỉ cần để từ đó như cách đã hướng dẫn (? mô tả chán quá) và không nên khoảng cách . . . bằng cách xóa đi dòng trắng đó, hoặc thêm chú thích. 

Khuyến khích nên để phần mô tả đó (? mô tả đó là sao) bên cạnh lệnh `\begin{}` 

```tex
\begin{lemma}[Bổ đề Kuratowski--Zorn]
    Cho P là một tập hợp sắp thứ tự riêng phần và giả sử mọi xích trong P đều có một chặn trên trong P. Khi đó P có một phần tử cực đại.
\end{lemma}
```

Tổng hợp lại ta được: 

```tex
\documentclass{article}

\usepackage[utf8]{vietnam}

\newtheorem{lemma}{Bổ đề}

\begin{document}

\begin{lemma}[Bổ đề Kuratowski--Zorn]
    Cho P là một tập hợp sắp thứ tự riêng phần và giả sử mọi xích trong P đều có một chặn trên trong P. Khi đó P có một phần tử cực đại.
\end{lemma}

\end{document}
```