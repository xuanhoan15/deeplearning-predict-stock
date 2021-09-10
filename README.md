##  10 Model Machine Learning phổ biến trong dự báo xu hướng giá cổ phiếu

Thị trường chứng khoán là nơi mà mọi người đều mong muốn tìm ra các "câu thần chú" để dự đoán thành công giá cổ phiếu. Mặc dù vậy, hầu như giá là thứ không thể dự đoán một cách chính xác. 

Trong bài viết này, mình sẽ giới thiệu qua một thư viện rất hay, hỗ trợ cả 10 Model phổ biến nhất trong dự báo chuỗi thời gian. Và áp dụng thử 4 Model là SARIMA, Facebook Prophet, HoltWinters & Vector autoregression (VAR), để mô phỏng lại quá trình dự báo giá dựa trên lịch sử giá.

Thư viện Kats do Facebook's Data Science team xây dựng và phát triển. Trong thư viện có support hầu hết các model dự báo Time Series phổ biến như: Linear
, Quadratic, ARIMA, SARIMA, Holt-Winters, Prophet, AR-Net, Theta, VAR. Hay thậm chí model Deep Learning là LSTM.

Lưu ý:
* Model được áp dụng đơn giản, chưa Tuning Parameter cũng như khung thời gian train là rất ngắn. Do đó những Model trong bài viết mang tính chất giới thiệu là chính, còn hiệu quả về mặt đầu tư thì cần phải có thời gian đánh giá lại. Việc chỉ dùng giá mở cửa, cao nhất, thấp nhất, khối lượng để dự báo giá đóng cửa mang rất nhiều rủi ro (đọc thêm bài viết https://towardsdatascience.com/is-it-possible-to-predict-stock-prices-with-a-neural-network-d750af3de50b)
* Model thiết lập đơn giản đến mức bạn có thể clone một bản trên colab, và chỉ thay đổi dữ liệu đầu vào theo đúng cấu trúc là được.
* Thư viện KATS cũng có hỗ trợ cả việc điều chỉnh tham số (Tuning Parameter) của các Model, cũng như Backtesting error như MAE, MSE, RMSE, MAPE,... Tuy nhiên, mình sẽ viết về phần này trong một bài viết khác!
* Dữ liệu bên dưới là dữ liệu của Vn-Index từ 2009 đến 2021, mình trích xuất từ V-Pro của Chứng Khoán Bản Việt (HoSE:VCI). Bên dưới cũng có hướng dẫn cách export nhanh cho ai muốn vọc thử liền. (ai muốn dùng thử VPro thì mở tk ở đây: https://invest.vcsc.com.vn/mo-tai-khoan-online?ref=hieult)
* Mình cũng có viết những bài viết khác về áp dụng AI trong đầu tư như: Algo Trading trong phân tích tâm lí thị trường (Sentiment), Áp dụng Machine Learning trong dự báo lợi nhuận đầu tư,... Tham khảo thêm tại: https://www.cafechungkhoan.com/search/label/ai?&max-results=12
