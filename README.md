# Phát hiện và xử lý dữ liệu bị mất với tập dữ liệu về chất lượng không khí AQI tại thành phố Kolkata của Ấn Độ
## 1. Phát hiện dữ liệu bị mất bằng thư viện missingno
## 2. Các cách xử lý mất dữ liệu
### 2.1. Xóa bỏ: Sử dụng khi tập dữ liệu đầu vào có RẤT ít sample bị missing. 
* Xóa bỏ hàng: Khi trong tập dữ liệu có phần trăm sample missing < 4% có thể loại bỏ
* Xóa bỏ cột: áp dụng khi phần trăm missing data quá lớn 70 80%.
### 2.2. Thay thế: Cách này thường áp dụng hơn
#### 2.2.1. Với dữ liệu theo dạng chuỗi thời gian
* Foward fill: thay các giá trị bị thiếu bằng các giá trị phía trên nó. Thường áp dụng khi các giá trị bị thiếu ở cuối tập dữ liệu
* Back fill: thay thế các giá trị bị thiếu bằng các giá trị phía sau nó. Thường áp dụng khi các giá trị bị thiếu ở đầu tập dữ liệu
* Linear Interpolation (Nội suy tuyến tính): ước lượng giá trị bị thiếu trên các giá trị xung quanh nó. Sử dụng các giá trị có sẵn gần nhất giữa 2 bên (trên và dưới) để ước lượng giá trị đó và giả định mối quan hệ giữa các giá trị là tuyến tính
#### 2.2.1. Với dữ liệu không theo dạng chuỗi thời gian  
* Thay thế bằng hằng số
* Thay thế bằng giá trị trung bình, trung vị hay phổ biến nhất của cột đó
### 2.3. Một số cách nâng cao
* KNN
* MICE
* XGBoost Algorithms
* LightGBM Algorithms
