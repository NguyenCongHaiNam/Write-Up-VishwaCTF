*Tớ đã không thể solved trong thời gian cuộc thi và đây là wu sau 3 tiếng ngồi ở quán Cát Xét Cafe của người anh chai ruộc (ở đây có món Trà trôi tàu siu đỉnh, ai rảnh thì ghé số 10 ngõ 445 Nguyễn Khang, HN thưởng thức nhé .-.)*



# OSINT
## Description
######  In response to alarming reports, our cybersecurity team is actively pursuing a hacker known by the alias "h3ck3r_h3_bh41", who poses a serious threat by extorting innocent individuals for monetary gain. Your mission is to track down this hacker and provide us with the crucial information needed to apprehend them. Retrieve the Hacker's complete full name (first name, middle name, last name), formatted in lowercase and replacing spaces with underscores, along with the associated website domain. Flag Format: VishwaCTF{full_name_domain.in}

## Recon
Đầu tiên tớ thấy đề cho một cái biệt danh, search một chút thì tớ tìm được tài khoản X này 

![](/osint1.png "") 

Tìm mãi trong đây thì tớ vẫn không thấy có gì khả nghi trừ cái post đầu tiên `Who is Cookie the baby chick ? Very Cute indeed :)`, nhưng trong thời gian cuộc thi không cách nào tìm được thông tin gì từ đây, khi kết thúc giải tớ dm author thì được biết nó phải là `cookiethebabychick`, sử dụng [tool này](https://www.idcrawl.com/) thì tớ tìm được account IG của hắn

![](/osint2.png "") 

Một số thông tin thu thập được:
1. Người ta đang theo dõi là `h3ck3r_h3_bh41` aka `cookiethebabychick's dad` aka `simon_j_peter`.

![](/osint3.png "") 
![](/osint4.png "") 
   
2. Hắn có một kênh Youtube với username là `husky woof woof`.

![](/osint5.png "") 

Tớ đã thử dùng tool trên để tìm những social khác của `husky woof woof` nhưng không được, những tài khoản tìm được đều là rabbit hole. Betak quá nên tìm lại description đọc thì 

`our cybersecurity team is actively pursuing a hacker known by the alias "h3ck3r_h3_bh41"`

Ở đây có đề cập tới một `cybersecurity team`, nhận ra là organization of this ctf cũng là một cyber team. Tìm thử trên gg thì đúng là như vậy, tớ có được Linkedin của tổ chức.

![](/osint6.png "") 

Recon các thành viên của tổ chức thì tớ tìm được một tài khoản khá là khả nghi

![](/osint7.png "") 

Tiếp tục tìm kiếm thì tada, Linkedin của `h3ck3r_h3_bh41` hay bây giờ là `simon_john_peter` 

![](/osint8.png "") 

Thừa thắng xông lên, ở post thứ 2 có một link ảnh

![](/osint9.png "") 
![](/osint10.png "") 

Tải về và phân tích thì tớ có được tọa độ của bức anh, dùng [tool này](https://www.aperisolve.com/)

![](/osint11.png "")

Tìm kiếm theo tọa độ thì tớ có được địa điểm chụp bức ảnh là ở ` Maharashtra, India`, nhưng cụ thể có vẻ không đúng lắm

![](/osint12.png "")

Lúc này nhớ lại con hổ trong bức anh, có lẽ nào đây là một sở thú hay vườn hoang dã gì gì ở gần đây, tiếp tục search gg thì tada again

![](/osintend.png "")
![](/osintend2.png "")

Flag: VishwaCTF{simon_john_peter_tadobanationalpark.in}
## In Conclusion

Tóm lại thì bài này sú vlon :)) btw some new knowledge from this challenge ~~
