# Phân Tích Vấn Đề Tai Nạn Giao Thông

## Mô tả dự án

Dự án này tập trung vào phân tích dữ liệu các vụ tai nạn giao thông tại Vương quốc Anh, sử dụng hai bộ dữ liệu chính: **Accident_Information.csv** và **Vehicle_Information.csv**. Mục tiêu là khám phá, làm sạch, phân tích dữ liệu và xây dựng các mô hình dự đoán nhằm hiểu rõ hơn về các yếu tố ảnh hưởng đến tai nạn giao thông, từ đó đề xuất các giải pháp nâng cao an toàn.

## Nội dung chính

- **Khám phá và làm sạch dữ liệu:**  
  Xử lý giá trị thiếu, ngoại lệ, chuẩn hóa kiểu dữ liệu, loại bỏ dữ liệu không hợp lệ và tạo các đặc trưng mới như thời gian trong ngày, mùa, ngày cuối tuần.

- **Phân tích dữ liệu:**  
  - Phân tích theo thời gian (giờ, ngày, mùa, năm)
  - Phân tích theo địa điểm (bản đồ phân bố, đô thị/nông thôn)
  - Ảnh hưởng của điều kiện môi trường (thời tiết, mặt đường, ánh sáng)
  - Đặc điểm phương tiện và người điều khiển (tuổi, giới tính, loại xe, thao tác lái xe)

- **Xây dựng mô hình dự đoán:**  
  - Dự đoán số vụ tai nạn theo khu vực và quý trong năm bằng MLPRegressor
  - Dự đoán mức độ nghiêm trọng của tai nạn (Slight/Serious/Fatal) bằng Logistic Regression và Random Forest

- **Đánh giá mô hình:**  
  Sử dụng các chỉ số MAE, RMSE, R², confusion matrix, ROC-AUC và phân tích feature importance.

## Hướng dẫn sử dụng

1. **Cài đặt thư viện cần thiết:**
    ```sh
    pip install pandas numpy matplotlib seaborn scikit-learn plotly
    ```

2. **Tải dữ liệu gốc:**  
   [UK Road Safety Accidents and Vehicles - Kaggle](https://www.kaggle.com/datasets/tsiaras/uk-road-safety-accidents-and-vehicles/data)

3. **Chạy notebook:**  
   Mở file `Accident_analysis.ipynb` trên Jupyter Notebook hoặc VSCode và chạy tuần tự các cell.

## Kết quả nổi bật

- Tai nạn tập trung vào giờ cao điểm, ngày làm việc, mùa thu và tại các khu vực đô thị đông dân.
- Đa số tai nạn xảy ra trong điều kiện thời tiết tốt, mặt đường khô, ban ngày.
- Nhóm tuổi lao động (26–55 tuổi), đặc biệt là nam giới, có nguy cơ cao nhất.
- Mô hình dự đoán đạt độ chính xác khá cao (R² ≈ 0.81 với MLPRegressor, ROC-AUC ≈ 0.78 với Random Forest).

## Đề xuất

- Tăng cường kiểm soát giao thông vào giờ cao điểm, ngày làm việc và mùa khô.
- Nâng cấp hạ tầng giao thông, đặc biệt ở nông thôn và các điểm thiếu ánh sáng.
- Đẩy mạnh giáo dục an toàn giao thông cho nhóm tuổi lao động, nam giới.
- Ứng dụng mô hình dự báo để cảnh báo sớm và hỗ trợ ra quyết định cho các cơ quan chức năng.

---

**Tác giả:**  
Nguyen Thanh An  
