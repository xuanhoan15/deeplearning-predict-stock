#  Tạo model dự báo giá đơn giản bằng Deep Learning

Thị trường chứng khoán là nơi mà mọi người đều mong muốn tìm ra các "câu thần chú" để dự đoán thành công giá cổ phiếu. Mặc dù vậy, hầu như giá là thứ không thể dự đoán một cách chính xác. 

Chính vì lẽ đó, các nhà đầu tư lại đặt ra câu hỏi: nếu con người có thể ước tính và xem xét tất cả các yếu tố để dự đoán chuyển động hoặc giá trị tương lai của một cổ phiếu thì tại sao máy móc lại không thể? Hay nói cách khác, làm thế nào chúng ta có thể khiến máy móc dự đoán giá của một cổ phiếu? 

Trong bài viết này, mình sẽ áp dụng 2 Model có vẻ mới với giới đầu tư, đó là Facebook Prophet & HoltWinters, để mô phỏng lại những gì thế giới đã và đang phát triển: Giao dịch theo thuật toán (Algo Trading).

Các model này được build sẵn trong thư viện Kats của Facebook Research. Trong thư viện có support hầu hết các model dự báo Time Series phổ biến như: Linear
, Quadratic, ARIMA, SARIMA, Holt-Winters, Prophet, AR-Net, LSTM, Theta, VAR

Lưu ý:
* Model đơn giản, mang tính chất giới thiệu là chính, còn hiệu quả về mặt đầu tư thì cần phải có thời gian đánh giá lại. Việc chỉ dùng giá mở cửa, cao nhất, thấp nhất, khối lượng để dự báo giá đóng cửa mang rất nhiều rủi ro (đọc thêm bài viết https://towardsdatascience.com/is-it-possible-to-predict-stock-prices-with-a-neural-network-d750af3de50b)
* Model thiết lập đơn giản đến mức bạn có thể clone một bản trên colab, và chỉ thay đổi dữ liệu đầu vào theo đúng cấu trúc là được.
* Dữ liệu bên dưới là dữ liệu của cổ phiếu Thế Giới Di Động (HoSE:MWG), mình trích xuất từ V-Pro của Chứng Khoán Bản Việt (HoSE:VCI). Bên dưới cũng có hướng dẫn cách export nhanh cho ai muốn vọc thử liền. (ai muốn dùng thử VPro thì mở tk ở đây: https://invest.vcsc.com.vn/mo-tai-khoan-online?ref=hieult)
