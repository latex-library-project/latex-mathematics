# 2026-10-18

## Vấn đề 1.18.10.26: 

Phân tách đoạn mã cho người đọc dễ hình dung, rồi mới tổng quát đầy đủ các đoạn mã.

Ví dự ở bài học [Tiên đề, định nghĩa,..vv..](/Lecture%20notes%20math/Tiên%20đề,%20định%20nghĩa,%20định%20lý,..vv...md), khi ta muốn viết tiêu đề định nghĩa, định lý bằng tiếng Việt, thì ta cần phải khai báo package ngôn ngữ Việt Nam, sau đó sửa lại từ từ định nghĩa, định lý ở phần `text`. 

Thay vì chỉ giải thích không như vậy, ta cần chèn thêm đoạn mã chỗ mình sửa 

```tex
% --- CẤU HÌNH GÓI & MÔI TRƯỜNG ---
% Sử dụng gói vietnam để hỗ trợ gõ tiếng Việt tốt hơn trong LaTeX
\usepackage[utf8]{vietnam}

% Khai báo môi trường Định lý và Định nghĩa bằng tiếng Việt
\newtheorem{theorem}{Định lý}
\newtheorem{definition}{Định nghĩa}
```

Sau đó mới đưa về chung cả đoạn mã lớn. 

```tex
	\documentclass{article}
	
	% --- CẤU HÌNH GÓI & MÔI TRƯỜNG ---
	% Sử dụng gói vietnam để hỗ trợ gõ tiếng Việt tốt hơn trong LaTeX
	\usepackage[utf8]{vietnam}
	
	% Khai báo môi trường Định lý và Định nghĩa bằng tiếng Việt
	\newtheorem{theorem}{Theorem}
	\newtheorem{definition}{Definition}
	
	\begin{document}
	
	% ==========================================
	% SECTION: ĐỊNH LÝ GAUSS - WANTZEL
	% ==========================================
	\begin{theorem}[Gauss--Wantzel]
	% Nội dung định lý về điều kiện dựng hình đa giác đều bằng thước và compa
	Việc chia đường tròn thành $n$ phần bằng nhau bằng thước kẻ và compa là khả thi khi và chỉ khi
	% Công thức toán dạng khối (display style)
	\[
	n = 2^k \cdot p_1 \cdot p_2 \dots p_t
	\]
	% Giải thích các tham số trong công thức (k có thể bằng 0 nên dùng số nguyên không âm)
	trong đó $k$ là một số nguyên dương và $p_1, p_2, \dots, p_t$ là các số nguyên tố Fermat phân biệt.
	\end{theorem}
	
	% ==========================================
	% SECTION: ĐỊNH NGHĨA SỐ NGUYÊN TỐ FERMAT
	% ==========================================
	\begin{definition}[Số nguyên tố Fermat]
	% Khai báo dạng tổng quát của số Fermat
	Một số nguyên có dạng 
	\[
	F_n = 2^{2^n}+1 
	\]
	% Điều kiện để một số Fermat trở thành số nguyên tố Fermat
	được gọi là số nguyên tố Fermat nếu kết quả $F_n$ tính được là một số nguyên tố.
	\end{definition}
	
	\end{document}
```

Thì đây chính là vấn đề mà mình nêu lên và cần chỉnh sửa lại ở các bài viết.  


# 2026-11-31: 

## Vấn đề 1.31.11.26: 

Plain TeX, ConTeXt, XeTeX, LuaTeX, fonts, graphics, ..vv.. 

Chúng là gì ? ... Một số câu hỏi khác để tìm hiểu các vấn đề trên.  

## Vấn đề 2.31.11.26: 

Ở các phần bài học toán luôn có những kết nối nhất định để mở ra bài học mới. Tất nhiên ta sẽ không thể học những phần kiến thức mới, nếu như ta không nền tảng vũng chắc trước đó để làm bệ phóng cho việc hiểu những cái mới, đó có thể là một bài học mới nhằm mở rộng các kiến thức đã biết trước đó, hoặc cũng có thể thay đổi lại một quan điểm cũ bằng một quan điểm mới, đầy chặt chẽ, tinh gọn, xúc tích hơn. 

Tất nhiên, ta sẽ không thể hiểu được quan điểm mới nếu như ta chưa từng đi qua những vấn đề sai lầm xưa cũ. Điều đó sẽ giúp ta phát triển hơn trên con đường tư duy về LaTeX. 

Dù vậy, mới hay cũ đều có những ưu và nhược của nó, nó bổ sung cho nhau, làm mở rộng trên chính nhu cầu của người dùng, hơn là sẽ sẵn sàng triệt tiêu, bệ hạ nhau. Điều này phụ thuộc vào cách bạn suy nghĩ theo tiêu chí của bản thân, và chọn sao cho phù hợp với bạn, cho nhiều vấn đề khác nhau. 

Ở mỗi phần bài học mới trong latex, tôi đều cố gắng đưa ra lại những phần kiến thức đã học để giúp mọi người không phải bị bỡ ngỡ hay cố gắng xoay sở nhảy qua lại kiến thức, nhằm tiết kiệm việc học latex nhất có thể đến người học. 

Chỉ là, tôi nên tổng hợp quá trình đó ở trước, giữa hay sau phần bài học mới latex đó ?   