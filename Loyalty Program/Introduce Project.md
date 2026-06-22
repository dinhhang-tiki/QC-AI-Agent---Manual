**1\. Introduce.** 

Loyalty Program là một product được xây dựng để phục vụ chương trình khách hàng tri ân của TIKI. Sản phẩm được xây dựng để cung cấp trải nghiệm đầy đủ cho khách hàng khi mua hàng tại TIKI, cũng như giúp biz teams có thể vận hành chương trình được hiệu quả.

2.Requirements.

**2.1. Tổng quan.**

Chương trình loyalty program cho phép phân loại khách hàng dựa trên lượng đơn hàng vái giá trị mua hàng tích luỹ trong vòng 6 tháng gần nhất. Chương trình có nhiều thứ hạng, mỗi thứ hạng có yêu cầu về lượng đơn và giá trị mua hàng nhất định. Mỗi thứ hạng sẽ đi kèm nhiều quyền lợi khác nhau để kích thích khách hàng mua hàng hoá trên TIKI, như freeship coupon, special discount... Thứ hạng thành viên sẽ được xét duyệt lại sau mỗi chu kỳ 6 tháng. Chương trình cũng cho phép chia sẻ khách hàng chia sẻ quyền lợi với các thành viên gia đình.

## **2.2. Hạng thành viên**

Chương trình Loyalty có nhiều hạng thành viên khác nhau. Hiện tại chương trình đang quy hoạch cho 4 tháng thành viên:

* Hạng mặc định: tất cả các khách hàng Tiki đều thuộc hàng mặc định.  
* Hạng Gold  
* Hạng Diamond  
* Hạng VIP **\=\> tạm thời không cần quan tâm**

|  |  |  |
| :---- | :---- | :---- |
| Gold | Trong vòng 6 tháng: 3 orders 1 triệu VNĐ |  |
| Diamond | Trong vòng 6 tháng: 10 orders 4 triệu VNĐ |  |
| VIP | Trong vòng 6 tháng: 30 orders 12 triệu VNĐ | Sẽ không launching ngay lần đầu tiên |

**Lưu ý:**

* **Về tiêu chí số lượng đơn hàng:** Chỉ tính các đơn hàng giao thành công trong chu kỳ (xác định theo thời điểm giao hàng thành công), và loại trừ đơn hàng sau:  
  * Đơn hàng Dịch vụ, Voucher & Dịch vụ (*danh sách ngành hàng bị loại trừ chi tiết ở [**link**](https://docs.google.com/spreadsheets/d/1Ffy9IFM80U5RqQryHbTp2z3WunNqq6CpvpeWLf50dfs/edit?gid=480632505#gid=480632505)*).  
  * Đơn hàng nạp ngân sách TIKI Ads.  
  * Đơn hàng vi phạm chính sách của TIKI.  
  * Đơn hàng giao không thành công hoặc đơn hàng trả hàng, hoàn tiền. (Lưu ý: Trong trường hợp đơn hàng bị hủy hoặc khách hàng yêu cầu trả hàng/hoàn tiền, giá trị đơn hàng, chi tiêu từ đơn hàng này sẽ bị trừ khỏi số tích lũy trước đó. Đồng thời số tiền hoàn lại sẽ bằng giá trị đơn hàng trừ đi cashback trước đó, Số tiền hoàn lại \= Tiền gốc \- Cashback).  
* **Về tiêu chí số tiền chi tiêu:** Chỉ xét dựa theo đơn hàng hợp lệ. Số tiền chi tiêu được xác định bằng NMV. Theo đó, Spending \= NMV \= Product Value \+ Handling Fee \+ Shipping Fee \- (Discount \+ Shipping Discount \- TikiXu).

Các thứ hạng này có thể thay đổi theo thời gian như thêm hoặt bớt thứ hạng. Các tiêu chí cũng có thể thay đổi theo thời gian có thể yêu cầu tăng hoặc giảm lượng đơn và giá trị mua hàng hoặc thêm bớt các điều kiện khác. Vì vậy việc thiết kế hệ thống phải linh hoạt để đáp ứng các yêu cầu mở rộng sau này về nghiệp vụ.

### **Chu kỳ xét hạng thành viên.**

Mỗi năm, TIKI Loyalty Rewards sẽ có 2 chu kỳ xét duyệt thứ hạng: Chu kỳ 1 từ 01/01 đến 30/06 và Chu kỳ 2 từ 01/07 đến 31/12. Việc khởi động lại chu kỳ sẽ diễn ra vào 2 mốc thời gian quan trọng: 01/01 và 01/07 hàng năm.

Vào đầu mỗi chu kỳ, thứ hạng của người dùng sẽ được thiết lập lại và tính là "thứ hạng khởi điểm", đồng thời số lượng đơn hàng và mức chi tiêu tích lũy sẽ được làm mới về 0\. Thứ hạng khởi điểm sẽ được xác định dựa trên số đơn hàng và chi tiêu tích lũy trong chu kỳ trước đó.

Ví dụ: *Nếu trong Chu kỳ 1 từ ngày 01/01/2025 đến 30/06/2025, bạn đã hoàn thành 10 đơn hàng và chi tiêu tổng cộng 4.000.000 VND trên TIKI, thì thứ hạng khởi điểm của bạn trong Chu kỳ 2 năm 2025 (từ 01/07/2025 đến 31/12/2025) sẽ là Kim Cương.*  

Phase 2: 
3. Điểm thưởng thành viên.
 3.1. Điểm thưởng.
Điểm thưởng thành viên là một dạng khuyến mại có giá trị tương đương tiền. Khách hạng sẽ nhận được tuỳ theo từng hạng thành viên (coi thêm ở mục quyền lợi). Các đặc điểm của điểm thưởng thành viên:

Có giá trị tương đương tiền, khách hàng có thể sử dụng khi mua hàng (như TIKI Xu).
Điểm thưởng thành viên được quản lý trong ví điểm thưởng của từng khách hàng. Nó không bị ảnh hưởng bởi việc thay đổi thứ hạng người dùng.
TIKI có toàn quyền với việc cập và thu hồi điểm thưởng của người dùng dựa theo chính sách kinh doanh của công ty. 
Điểm thưởng hạng thành viên có thời gian hết hạn. Dựa theo chính sách ban hành vào tháng 07/2025, thời gian hết hạn là 90 ngày, tính từ thời điểm phát sinh giao dịch hoàn tiền cuối cùng. Vd một khách hàng nhận hoàn điểm thưởng vào ngày 1 tháng 1, thì thời gian hết hạn sẽ là 31/03, sang tháng 01/02 nếu phát sinh tiếp giao dịch hoàn điểm thưởng, thì thời hạn hết hạn sẽ được mở rộng tới 30/04. Giao dịch hoàn tiền khi đơn hàng giao thành công (tham khảo phần chính sách hoàn điểm thưởng)
 3.2. Chính sách hoàn điểm thưởng.
Khi khách hàng mua hàng, tuỳ theo thứ hạng của khách hàng thì sẽ nhận được mức hoàn điểm thưởng khác nhau (chi tiết tham khảo mục quyền lợi). Mỗi khách hàng mỗi tháng sẽ có hạn mức hoàn điểm thưởng. Tuỳ theo thứ hạng sẽ có hạn mức hoàn điểm thưởng khác nhau, thông thường tối đa không quá 500k vnđ/tháng. 

Điểm thưởng tính trên giá trị đơn hàng (bao gồm cả phí ship) sau khi trừ đi tất cả các chi phí khuyến mại. 

Khi đơn hàng được giao thành công, kượng điểm thưởng được hoàn tính tại thời điểm đơn hàng được đặt.

Điểm thưởng sẽ được hoàn cho khách hàng sau khi đơn hàng giao hàng thành công. Theo chính sách hiện tại, thời gian hoàn tiền là T = 24h tính từ thời điểm giao hàng thành công. 

Điểm thưởng không được hoàn cho các category: dịch vụ, thẻ cào, thẻ game... Chi tiết danh sách do Business cung cấp (bổ sung sau). Trước mắt thì không cho khách hàng dùng điểm thưởng mua hàng ở các category này.

 3.3. Sử dụng điểm thưởng.
Khách hàng có thể sử dụng điểm thưởng để mua hàng. Điểm thưởng được quy đổi tương đương tiền - một điểm thưởng tương đương một đồng. Khách hàng không được sử dụng quá 50% giá trị đơn hàng. 

Khách hàng có thể sử dụng điểm thưởng đồng thời với Xu, Astra. Thứ tứ áp dụng sẽ là:

Chương trình khuyến mại
Điểm thưởng
Astra 
TIKI Xu
Điểm thưởng được ghi nhận chi tiết trên đơn hàng như một coupon khuyến mại platform. Rules khuyến mại platform do business team cung cấp.

Trường hợp đơn hàng được tách, điểm thưởng cũng được phân bổ cho các đơn hàng con theo tỉ lệ giá trị đơn hàng (tham khảo logic của TIKI Xu)

 3.4. Vận hành đơn hàng.
Sau khi khách hàng thanh toán thành công, sẽ có hai phần điểm thưởng liên quan tới hoạt động vận hành:

Điểm thưởng khách hàng sử dụng để thanh toán đơn hàng.
Điểm thưởng khách hàng nhận được khi mua hàng.
 3.5. Hoàn điểm thưởng đã sử dụng khi mua hàng.
Khi khách hàng thanh toán không thành công, điểm thưởng được sử dụng sẽ được hoàn lại cho khách hàng. Thời gian hoàn tuỳ thuộc chính sách của nghiệp vụ thanh toán (Tham khảo các chính sách huỷ đơn, thanh toán lại của nghiệp vụ hiện hành).

Khi đơn hàng không được giao tới khách hàng thành công vì lý do khách hàng hay TIKI, thì phần điểm thưởng mà đã sử dụng sẽ được hoàn lại cho khách hàng.

Điểm thưởng sẽ được extend thời điểm expiration kể từ ngày được hoàn theo chính sách chung của điểm thưởng. Tức là sẽ có thêm 90 ngày để sử dụng

 3.6 Thu hồi điểm thưởng.
Khách hàng có thể đổi ý và nhận lại tiền, hoặc khi khách hàng đổi hàng lỗi và nhận tiền bồi thưởng:

Toàn bộ số tiền khách hàng đã sử dụng mua hàng, bao gồm cả Xu, Astra, VIP Points, sẽ được hoàn lại cho khách hàng theo chính sách hoàn tiền.
Phần điểm thưởng khách hàng được nhận do mua hàng sẽ được thu hồi lại. Số điểm thưởng thu hồi sẽ được trừ khỏi ví điểm thưởng của người dùng. Trường hợp ví điểm thưởng của người dùng không đủ thì sẽ bị ghi nhận âm.
Cần lưu ý, có thể trong thời gian từ khi khách hàng nhận được điểm thưởng, tới khi khách hàng đổi ý, thì khách hàng đã sử dụng hết điểm thưởng được nhận. Dẫn tới rủi ro không thu hồi được hết điểm thưởng.
Nếu khách hàng trao đổi hàng hoá theo chính sách đổi hàng, thì điểm thưởng đã được hoàn sẽ được giữ nguyên. Theo thống nhất với team kế toán tài chính: chấp nhận việc không thu hồi được nếu số dư điểm thưởng của người dùng không đủ. 


