---
date: 2026-01-09
description: Tìm hiểu cách thêm watermark vào hình ảnh với Aspose.Imaging cho Java.
  Hướng dẫn xử lý ảnh bằng Java này trình bày từng bước cách tạo watermark chéo nhanh
  chóng.
linktitle: Diagonal Image Watermarking
second_title: Aspose.Imaging Java Image Processing API
title: Cách Thêm Đánh Dấu Nước – Đánh Dấu Nước Hình Ảnh Đường Chéo (Java)
url: /vi/java/image-processing-and-enhancement/diagonal-image-watermarking/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Cách Thêm Watermark – Đánh Dấu Nước Hình Ảnh Chéo (Java)

Nếu bạn đang muốn **how to add watermark** cho ảnh của mình với hướng chéo thời trang, Aspose.Imaging for Java giúp việc này trở nên dễ dàng. Trong hướng dẫn từng bước này, chúng tôi sẽ hướng dẫn cách thêm watermark dạng văn bản quay 45 độ vào ảnh JPG (hoặc bất kỳ định dạng nào được hỗ trợ). Bạn không cần phải là chuyên gia Java – mỗi khối đều được giải thích bằng ngôn ngữ đơn giản để bạn có thể sao chép kết quả trong vài phút.

## Câu trả lời nhanh
- **Thư viện nào được sử dụng?** Aspose.Imaging for Java  
- **Từ khóa chính được đề cập?** how to add watermark  
- **Định dạng ảnh được hỗ trợ?** JPEG, PNG, BMP, TIFF, GIF và hơn nữa  
- **Cần bao nhiêu mã?** Chỉ bảy khối mã ngắn gọn  
- **Có cần giấy phép để thử nghiệm không?** Có bản dùng thử miễn phí; giấy phép cần thiết cho môi trường sản xuất  

## “how to add watermark” là gì trong xử lý ảnh?
Thêm watermark có nghĩa là phủ lên ảnh một văn bản hoặc đồ họa bán trong suốt để bảo vệ quyền sở hữu hoặc truyền tải thương hiệu. Watermark chéo đặc biệt hiệu quả vì nó phủ toàn bộ bức ảnh và khó bị cắt bỏ.

## Tại sao nên sử dụng Aspose.Imaging cho Java?
Aspose.Imaging cung cấp một API cấp cao trừu tượng hoá việc thao tác pixel mức thấp, hỗ trợ hàng chục định dạng và hoạt động trên bất kỳ môi trường Java nào. Nó cho phép bạn tập trung vào *điều* mình muốn đạt được—như thêm watermark chéo—mà không phải lo lắng về các quirks của định dạng ảnh.

## Yêu cầu trước

Trước khi bắt đầu, hãy chắc chắn bạn có những thứ sau:

1. **Aspose.Imaging for Java** – tải phiên bản mới nhất từ trang chính thức **[here](https://releases.aspose.com/imaging/java/)**.  
2. **Java Development Environment** – JDK 8+ và IDE yêu thích của bạn (IntelliJ, Eclipse, VS Code, v.v.).  
3. **An image to watermark** – đặt một ảnh mẫu JPG/TIFF/PNG trong thư mục mà bạn sẽ tham chiếu trong mã.

## Nhập các Gói

Đầu tiên, nhập các lớp bạn sẽ cần. Việc nhóm các import lại với nhau giúp mã dễ đọc và bảo trì hơn.

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## Bước 1: Tải ảnh hiện có

Chúng ta bắt đầu bằng việc tải ảnh nguồn. Phương thức `Image.load` tự động phát hiện định dạng.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Load an existing JPG image
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Rest of the code goes here
}
```

> **Mẹo:** Đặt đối tượng `Image` trong một khối try‑with‑resources (như trong ví dụ) để nó được giải phóng tự động, ngăn ngừa rò rỉ bộ nhớ.

## Bước 2: Chuẩn bị Văn bản và Đồ họa Watermark

Tạo một đối tượng `Graphics` liên kết với ảnh đã tải và lưu kích thước ảnh để tính toán sau.

```java
// Declare a String object with Watermark Text
String theString = "45 Degree Rotated Text";

// Create and initialize an instance of Graphics class
Graphics graphics = new Graphics(image);

// Initialize an object of SizeF to store image Size
Size sz = graphics.getImage().getSize();
```

## Bước 3: Định nghĩa Font và Brush

Chọn một font nổi bật và một brush xác định màu và độ trong suốt của watermark. Điều chỉnh độ trong suốt để watermark bán trong suốt.

```java
// Create an instance of Font, initialize it with Font Face, Size, and Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Create an instance of SolidBrush and set its various properties
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Bước 4: Định dạng Văn bản của Bạn

Đặt các cờ căn chỉnh và định dạng để văn bản được căn giữa khi vẽ.

```java
// Initialize an object of StringFormat class and set its various properties
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Bước 5: Áp dụng Biến đổi

Ma trận biến đổi cho phép chúng ta di chuyển gốc tới trung tâm ảnh và sau đó quay văn bản -45° (theo chiều kim đồng hồ).

```java
// Create an object of Matrix class for transformation
Matrix matrix = new Matrix();
// First a translation then a rotation
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Set the Transformation through Matrix
graphics.setTransform(matrix);
```

## Bước 6: Vẽ và Lưu

Cuối cùng, vẽ chuỗi lên ảnh và ghi kết quả ra đĩa.

```java
// Draw the string on Image
graphics.drawString(theString, font, brush, 0, 0, format);

// Save output to disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

Khi bạn mở `AddDiagonalWatermarkToImage_out.jpg` bạn sẽ thấy văn bản màu đỏ, bán trong suốt nghiêng qua trung tâm của bức ảnh.

## Các vấn đề thường gặp & Giải pháp

| Problem | Reason | Fix |
|---------|--------|-----|
| Watermark xuất hiện quá nhạt | Độ trong suốt được đặt thành 0 (hoàn toàn trong suốt) | Tăng độ trong suốt, ví dụ `brush.setOpacity(0.5f);` |
| Văn bản bị cắt ở các cạnh | Dịch chuyển không được căn giữa cho ảnh không phải hình vuông | Sử dụng `matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);` như trên, sau đó điều chỉnh góc quay nếu cần |
| Lỗi định dạng ảnh không được hỗ trợ | Sử dụng phiên bản Aspose.Imaging cũ | Cập nhật lên phiên bản Aspose.Imaging mới nhất |

## Câu hỏi thường gặp

### Q1: Aspose.Imaging cho Java có phù hợp cho người mới bắt đầu không?
**A:** Chắc chắn! API trực quan, và tài liệu cung cấp các ví dụ rõ ràng. Ngay cả các nhà phát triển mới với xử lý ảnh cũng có thể theo dõi hướng dẫn này và tạo ra kết quả chuyên nghiệp nhanh chóng.

### Q2: Tôi có thể tùy chỉnh văn bản và kiểu dáng của watermark không?
**A:** Có. Thay đổi biến `theString`, chọn một `Font` khác, sửa `brush.setColor(...)`, hoặc điều chỉnh góc quay trong ma trận để phù hợp với thương hiệu của bạn.

### Q3: Aspose.Imaging cho Java có hỗ trợ các định dạng ảnh khác ngoài JPG không?
**A:** Có. Thư viện hỗ trợ BMP, PNG, GIF, TIFF, PSD và nhiều định dạng khác. Chỉ cần truyền đường dẫn phù hợp cho phương thức `Image.load`.

### Q4: Có bản dùng thử miễn phí cho Aspose.Imaging cho Java không?
**A:** Có, bạn có thể dùng thử Aspose.Imaging cho Java với bản dùng thử miễn phí. Tải về **[here](https://releases.aspose.com/)**.

### Q5: Tôi có thể tìm trợ giúp hoặc hỗ trợ cho Aspose.Imaging cho Java ở đâu?
**A:** Đối với câu hỏi, báo cáo lỗi hoặc lời khuyên thực tiễn, hãy truy cập diễn đàn hỗ trợ Aspose.Imaging cho Java **[here](https://forum.aspose.com/)**.

---

**Cập nhật lần cuối:** 2026-01-09  
**Kiểm tra với:** Aspose.Imaging for Java 24.11 (phiên bản mới nhất tại thời điểm viết)  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}