# Research Portfolio

Portfolio cá nhân về nền tảng toán học, machine learning và computer vision. Repository ghi lại quá trình học qua các phần giải thích, triển khai thuật toán, thực nghiệm có thể tái lập và phân tích kết quả.

## Mục tiêu học tập

- Củng cố đại số tuyến tính, giải tích, xác suất và tối ưu hóa phục vụ machine learning.
- Hiểu thuật toán bằng cách tự triển khai trước khi sử dụng thư viện cấp cao.
- Sử dụng PyTorch để xây dựng, huấn luyện và đánh giá mô hình computer vision.
- Thiết kế benchmark và thực nghiệm có đối chứng, ghi rõ dữ liệu, metric và giới hạn.
- Khảo sát cân bằng giữa chất lượng phân đoạn ảnh và chi phí lưu trữ/tính toán của mô hình.

## Mục tiêu nghiên cứu

Xây dựng các nghiên cứu nhỏ, có thể kiểm chứng và tái lập: xác định câu hỏi, lập baseline, chọn metric phù hợp, so sánh phương pháp trong cùng điều kiện và trình bày giới hạn của kết quả. Hai hướng ứng dụng dự kiến là phát hiện biên trên hiện vật văn hóa và phân đoạn ảnh lũ lụt với các phương pháp nén mô hình.

Kết quả số liệu, kết luận và trạng thái hoàn thành sẽ chỉ được cập nhật sau khi có thực nghiệm. Dữ liệu lớn, dữ liệu có bản quyền hoặc dữ liệu nhạy cảm không được đưa vào repository nếu chưa xác định rõ quyền sử dụng.

## Lộ trình checkpoint

Các checkpoint dưới đây là lộ trình dự kiến theo cấu trúc dự án hiện tại. Mỗi checkpoint cần có ghi chú hoặc mã nguồn tương ứng; các kết quả thực nghiệm cần kèm cấu hình và cách tái lập.

### CP0 — Thiết lập portfolio

- [ ] **CP0.1 — Nền tảng repository:** tạo repository public; hoàn thiện README, CHANGELOG và cấu trúc dự án; liệt kê toàn bộ checkpoint; tạo tag `cp-0.1`.
- [ ] **CP0.2 — Môi trường và quy ước:** xác định Python/tooling, quy ước đặt tên, quản lý dependency, cấu hình kiểm tra chất lượng và cách tổ chức thí nghiệm.
- [ ] **CP0.3 — Kế hoạch thực nghiệm:** chốt câu hỏi nghiên cứu, phạm vi dữ liệu, baseline, metric và tiêu chí hoàn thành cho hai dự án ứng dụng.

### CP1 — Nền tảng toán học cho ML (`math-for-ml/`)

- [ ] **CP1.1 — Đại số tuyến tính:** vector, ma trận, phép biến đổi tuyến tính, trị riêng và trực giác hình học.
- [ ] **CP1.2 — Giải tích và xác suất:** đạo hàm/gradient, quy tắc dây chuyền, phân phối xác suất và kỳ vọng.
- [ ] **CP1.3 — Tối ưu hóa:** hàm mất mát, gradient descent, learning rate và liên hệ với việc huấn luyện mô hình.

### CP2 — Machine learning từ đầu (`ml-methods-from-scratch/`)

- [ ] **CP2.1 — Dữ liệu và baseline:** pipeline dữ liệu, chia tập, tiền xử lý và metric phù hợp.
- [ ] **CP2.2 — Thuật toán cốt lõi:** triển khai một số thuật toán ML cơ bản, nêu rõ giả định và kiểm thử bằng ví dụ nhỏ.
- [ ] **CP2.3 — Đánh giá và phân tích:** so sánh với thư viện tham chiếu, phân tích lỗi và ghi lại giới hạn của triển khai.

### CP3 — Computer vision với PyTorch (`pytorch-cv-fundamentals/`)

- [ ] **CP3.1 — PyTorch căn bản:** tensor, autograd, `Dataset`/`DataLoader` và vòng lặp huấn luyện.
- [ ] **CP3.2 — Mô hình và huấn luyện:** xây dựng CNN, theo dõi quá trình học và lưu/tải checkpoint.
- [ ] **CP3.3 — Đánh giá computer vision:** thiết lập baseline thị giác máy tính, metric, phân tích lỗi và quy trình tái lập.

### CP4 — Benchmark phát hiện biên (`cultural-object-edge-benchmark/`)

- [ ] **CP4.1 — Phạm vi benchmark:** xác định câu hỏi, nguồn dữ liệu được phép dùng, tiêu chí gán nhãn và quy trình chia tập.
- [ ] **CP4.2 — Phương pháp và metric:** chọn baseline phát hiện biên, chuẩn hóa đầu vào/đầu ra và xác định metric đánh giá.
- [ ] **CP4.3 — Thực nghiệm:** chạy so sánh trong điều kiện nhất quán, phân tích kết quả và công bố giới hạn/tính tái lập.

### CP5 — Phân đoạn lũ lụt và nén mô hình (`flood-segmentation-compression/`)

- [ ] **CP5.1 — Baseline phân đoạn:** xác định dữ liệu và quyền sử dụng, pipeline tiền xử lý, mô hình baseline và metric.
- [ ] **CP5.2 — Nén mô hình:** khảo sát phương pháp nén phù hợp; đo chất lượng, kích thước mô hình và chi phí suy luận.
- [ ] **CP5.3 — So sánh và báo cáo:** so sánh baseline với mô hình nén, phân tích đánh đổi và trình bày hướng phát triển tiếp theo.

## Cấu trúc repository

```text
Research-portfolio/
├── README.md
├── CHANGELOG.md
├── .gitignore
├── math-for-ml/
├── ml-methods-from-scratch/
├── pytorch-cv-fundamentals/
├── cultural-object-edge-benchmark/
└── flood-segmentation-compression/
```

Mỗi thư mục dự án có README riêng mô tả phạm vi và trạng thái. Dữ liệu, mô hình đã huấn luyện và kết quả lớn sẽ được quản lý riêng; không commit các tệp này trước khi kiểm tra giấy phép và dung lượng.

## Trạng thái

- **CP0.1:** tài liệu và cấu trúc local đang được chuẩn bị; việc xuất bản repository public, push và tag trên GitHub cần hoàn tất sau khi xác thực GitHub.
- **Các checkpoint còn lại:** chưa bắt đầu.

## Ngôn ngữ

Tài liệu portfolio hiện viết bằng tiếng Việt; tên dự án và thuật ngữ kỹ thuật được giữ bằng tiếng Anh khi phù hợp.
