  # 🎄 Cây Thông Noel 3D Tương Tác Sang Trọng

  > Một ứng dụng Web 3D Cây Thông Noel độ trung thực cao được xây dựng dựa trên **React**, **Three.js (R3F)** và **Nhận dạng Cử chỉ AI**.

  Dự án này không chỉ là một cây thông, nó là một phòng trưng bày tương tác mang đầy kỷ niệm. Hàng chục nghìn hạt có phát sáng, ánh sáng rực rỡ và những bức ảnh Polaroid lơ lửng tạo nên một cây thông noel sang trọng. Người dùng có thể kiểm soát hình dạng của cây (nhập/phân tán) và xoay góc nhìn thông qua cử chỉ, tận hưởng trải nghiệm hình ảnh cấp bộ phim.

  ## ✨ Tính Năng Cốt Lõi

  * **Trải Nghiệm Hình Ảnh Tuyệt Vời**：Thân cây được tạo thành từ 45,000+ hạt phát sáng, kết hợp với hiệu ứng sáng động (Bloom) và hiệu ứng phát sáng, tạo không khí mơ mộng.
  * **Phòng Trưng Bày Kỷ Niệm**：Ảnh lơ lửng trên cây theo kiểu "Polaroid", mỗi cái đều là một bộ phát sáng độc lập, hỗ trợ kết xuất hai mặt.
  * **Kiểm Soát Cử Chỉ Bằng AI**：Không cần chuột, chỉ cần bắt chước cử chỉ qua camera để kiểm soát hình dạng cây (nhập/phân tán) và xoay góc nhìn.
  * **Chi Tiết Phong Phú**：Bao gồm ánh sáng màu động nhấp nháy, bông tuyết vàng bạc rơi xuống, cũng như các quà tặng Noel và trang trí kẹo phân bố ngẫu nhiên.
  * **Có Thể Tùy Chỉnh Cao**：**Hỗ trợ người dùng dễ dàng thay thế bằng ảnh của riêng họ và tự do điều chỉnh số lượng ảnh.**

  ## 🛠️ Ngăn xếp Công nghệ

  * **Framework**: React 18, Vite
  * **3D Engine**: React Three Fiber (Three.js)
  * **Thư viện công cụ**: @react-three/drei, Maath
  * **Xử lý hậu kỳ**: @react-three/postprocessing
  * **AI Vision**: MediaPipe Tasks Vision (Google)

  ## 🚀 Bắt Đầu Nhanh

  ### 1. Chuẩn Bị Môi Trường
  Đảm bảo rằng máy tính của bạn đã cài đặt [Node.js](https://nodejs.org/) (khuyến nghị v18 hoặc cao hơn).

  ### 2. Cài Đặt Phụ Thuộc
  Mở terminal ở thư mục gốc của dự án và chạy:

  ```bash
  npm install
  ```

  ### 3. Khởi Động Dự Án

  ```bash
  npm run dev
  ```

  ## 🖼️ Tùy Chỉnh Ảnh

  ### 1. Chuẩn Bị Ảnh
  Tìm thư mục `public/photos/` trong thư mục dự án.

  Ảnh lớn ở đầu/ảnh bìa：Đặt tên là `top.jpg` (sẽ hiển thị trên ngôi sao năm cạnh 3D ở đỉnh cây).

  Ảnh thân cây：Đặt tên là `1.jpg, 2.jpg, 3.jpg` ... và cứ tiếp tục như vậy.

  Khuyến nghị：Sử dụng ảnh có tỷ lệ vuông hoặc 4:3, kích thước file không nên quá lớn (khuyến nghị dưới 500kb mỗi ảnh để đảm bảo mượt mà)

  ### 2. Thay Thế Ảnh
  Chỉ cần sao chép ảnh của bạn vào thư mục `public/photos/` để ghi đè lên ảnh cũ. Vui lòng giữ nguyên định dạng tên file (`1.jpg, 2.jpg` v.v.).

  ### 3. Sửa Đổi Số Lượng Ảnh (Tăng hoặc Giảm)
  Nếu bạn đặt thêm ảnh (ví dụ từ mặc định 31 ảnh tăng lên 100 ảnh), bạn cần sửa đổi mã để thông báo cho chương trình tải chúng.

  Mở file：`src/App.tsx`

  Tìm mã ở dòng 19：

  ```javascript
  // --- Tạo danh sách ảnh động (top.jpg + 1.jpg đến 31.jpg) ---
  const TOTAL_NUMBERED_PHOTOS = 31; // <--- Sửa đổi số này!
  ```
  ### 🖐️ Hướng Dẫn Kiểm Soát Cử Chỉ
  * **Dự án này có sẵn hệ thống nhận dạng cử chỉ AI, vui lòng đứng trước camera để hoạt động (nút DEBUG ở góc dưới bên phải để xem hình ảnh camera)**：
  🖐 Mở lòng bàn tay (Open Palm)	Phân tán (Disperse)	Cây Noel nổ thành hàng ngàn hạt và ảnh bay lên
  ✊ Nắm chặt nằm (Closed Fist)	Nhập (Assemble)	Tất cả các phần tử tập hợp lại thành cây Noel hoàn hảo
  👋 Chuyển động tay trái/phải	Xoay góc nhìn	Tay sang trái, cây quay trái; tay sang phải, cây quay phải
  👋 Chuyển động tay lên/xuống	Thay đổi góc nhìn dọc	Tay lên, góc nhìn nâng cao; tay xuống, góc nhìn hạ thấp
  ### ⚙️ Cấu Hình Nâng Cao
  * **Nếu bạn quen thuộc với mã, bạn có thể điều chỉnh thêm các tham số hình ảnh trong đối tượng CONFIG trong src/App.tsx**：
    const CONFIG = {
    colors: { ... }, // Sửa đổi màu sắc của cây, ánh sáng, viền
    counts: {
      foliage: 15000,   // Sửa đổi số lượng hạt lá (cấu hình thấp có thể bị giật)
      ornaments: 300,   // Sửa đổi số lượng ảnh/Polaroid treo
      lights: 400       // Sửa đổi số lượng đèn màu
    },
    tree: { height: 22, radius: 9 }, // Sửa đổi kích thước của cây
    // ...
  };

  ### 📄 Giấy Phép
  MIT License. Tự do sử dụng và sửa đổi cho các lễ kỷ niệm của riêng bạn!

  ### Chúc Mừng Giáng Sinh! 🎄✨

