---
date: 2026-01-12
description: Tìm hiểu cách điều chỉnh độ tương phản trong hình ảnh DICOM – hướng dẫn
  từng bước cách điều chỉnh độ tương phản bằng Aspose.Imaging cho Java và chuyển đổi
  DICOM sang BMP.
linktitle: DICOM Image Contrast Adjustment
second_title: Aspose.Imaging Java Image Processing API
title: Cách điều chỉnh độ tương phản trong ảnh DICOM bằng Aspose.Imaging cho Java
url: /vi/java/image-processing-and-enhancement/dicom-image-contrast-adjustment/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Cách Điều Chỉnh Độ Tương Phản Trong Hình Ảnh DICOM Bằng Aspose.Imaging cho Java

Trong lĩnh vực chẩn đoán hình ảnh y tế hiện đại, **cách điều chỉnh độ tương phản** có thể tạo ra sự khác biệt giữa một chẩn đoán rõ ràng và một chi tiết bị bỏ lỡ. Hướng dẫn này sẽ đưa bạn qua các bước chính xác để điều chỉnh độ tương phản trong các tệp DICOM bằng Aspose.Imaging cho Java, và chỉ cho bạn cách chuyển các hình ảnh DICOM sang BMP để dễ xem hoặc xử lý tiếp theo. Khi hoàn thành, bạn sẽ có một đoạn mã sẵn sàng sử dụng mà có thể chèn vào bất kỳ dự án Java nào.

## Câu Trả Lời Nhanh
- **Điều chỉnh độ tương phản làm gì?** Nó mở rộng dải giữa các pixel tối và sáng, làm cho các cấu trúc nổi bật.
- **Thư viện nào được yêu cầu?** Aspose.Imaging cho Java.
- **Có thể xuất ra BMP không?** Có – bạn có thể chuyển DICOM sang BMP sau khi điều chỉnh độ tương phản.
- **Có cần giấy phép cho môi trường sản xuất không?** Cần giấy phép thương mại cho việc sử dụng không phải đánh giá.
- **Phiên bản Java nào được hỗ trợ?** Java 8 và các phiên bản mới hơn.

## Điều Chỉnh Độ Tương Phản Là Gì và Tại Sao Nó Quan Trọng?
Việc điều chỉnh độ tương phản tăng cường sự khác biệt trực quan giữa các đặc điểm giải phẫu, giúp các bác sĩ hình ảnh phát hiện bất thường nhanh hơn. Trong quy trình DICOM, điều chỉnh độ tương phản trước khi chuyển đổi đảm bảo đầu ra BMP giữ được chất lượng chẩn đoán cần thiết cho việc báo cáo hoặc lưu trữ.

## Yêu Cầu Trước

Trước khi bắt đầu viết mã, hãy xác nhận rằng bạn đã có:

1. **Aspose.Imaging cho Java** – tải xuống từ trang chính thức [tại đây](https://releases.aspose.com/imaging/java/).  
2. **Môi trường phát triển Java** – JDK 8+ và IDE yêu thích của bạn (IntelliJ, Eclipse, VS Code, v.v.).  
3. **Một hình ảnh DICOM** – bất kỳ tệp .dcm nào bạn muốn cải thiện; các tệp mẫu có sẵn trực tuyến hoặc bạn có thể sử dụng dữ liệu lâm sàng của riêng mình.

## Nhập Các Gói

Các import này cung cấp cho bạn quyền truy cập vào các tính năng xử lý DICOM và lưu BMP.

```java
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.dicom.DicomImage;
import java.io.File;
import java.io.FileInputStream;
import java.io.IOException;
```

## Cách Điều Chỉnh Độ Tương Phản Trong Hình Ảnh DICOM

Dưới đây là quy trình hoàn chỉnh, từng bước. Mỗi bước được giải thích bằng ngôn ngữ đơn giản để bạn có thể theo dõi ngay cả khi mới bắt đầu với Aspose.Imaging.

### Bước 1: Xác Định Đường Dẫn Tệp

Đặt vị trí DICOM đầu vào và đường dẫn BMP đầu ra mong muốn. Thay thế phần giữ chỗ bằng thư mục thực tế trên máy của bạn.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "AdjustingContrast_out.bmp";
```

### Bước 2: Tải Hình Ảnh DICOM

Chúng tôi mở tệp DICOM bằng `FileInputStream`. Khối `try‑with‑resources` đảm bảo luồng được đóng tự động.

```java
File file = new File(inputFile);

try (FileInputStream fis = new FileInputStream(file)) {
    try (DicomImage image = (DicomImage) Image.load(fis)) {
        // All further processing happens inside this block
    }
} catch (IOException ex) {
    Logger.println(ex.getMessage());
    ex.printStackTrace();
}
```

### Bước 3: Điều Chỉnh Độ Tương Phản

Bên trong khối `try` bên trong, gọi `adjustContrast`. Giá trị có thể nằm trong khoảng **‑100** (giảm) đến **+100** (tăng). Trong ví dụ này chúng tôi tăng độ tương phản lên 50 đơn vị.

```java
image.adjustContrast(50);
```

### Bước 4: Chuyển Đổi DICOM Sang BMP và Lưu Hình Ảnh

Sau khi điều chỉnh độ tương phản, chúng tôi tạo một thể hiện `BmpOptions` và lưu kết quả dưới dạng tệp BMP. Bước này **chuyển đổi DICOM sang BMP**, cung cấp cho bạn một định dạng raster được hỗ trợ rộng rãi.

```java
image.save(outputFile, new BmpOptions());
```

## Các Vấn Đề Thường Gặp & Mẹo
- **Tệp DICOM không hợp lệ** – Đảm bảo tệp .dcm không được nén bằng một giao thức truyền không được hỗ trợ. Aspose.Imaging hỗ trợ hầu hết các mã hoá DICOM tiêu chuẩn.
- **Giá trị độ tương phản ngoài phạm vi** – Các giá trị vượt ±100 sẽ bị giới hạn; chọn một số phù hợp với biểu đồ histogram của ảnh.
- **Sử dụng bộ nhớ** – Các chuỗi DICOM lớn có thể tiêu tốn RAM đáng kể. Xử lý từng lát một nếu gặp `OutOfMemoryError`.

## Kết Luận

Bạn đã học được **cách điều chỉnh độ tương phản** trong hình ảnh DICOM bằng Aspose.Imaging cho Java và **cách chuyển DICOM sang BMP** cho các tác vụ tiếp theo. Quy trình này nhanh, đáng tin cậy và có thể tích hợp vào các pipeline hình ảnh y tế lớn hơn, dù bạn đang xây dựng một trình xem PACS, công cụ nghiên cứu, hay hệ thống báo cáo tự động.

Aspose.Imaging cho Java trừu tượng hoá việc xử lý DICOM ở mức thấp, cho phép bạn tập trung vào giá trị lâm sàng của hình ảnh.

## Câu Hỏi Thường Gặp

**Q: DICOM là gì và tại sao nó là tiêu chuẩn trong hình ảnh y tế?**  
A: DICOM (Digital Imaging and Communications in Medicine) là định dạng toàn cầu để lưu trữ, truyền tải và chia sẻ hình ảnh y tế, đảm bảo khả năng tương tác giữa các thiết bị và tổ chức.

**Q: Tôi có thể điều chỉnh độ sáng cùng với độ tương phản không?**  
A: Có, phương thức `adjustBrightness(int value)` hoạt động tương tự và có thể được gọi liên tiếp trước khi lưu.

**Q: Aspose.Imaging có hỗ trợ các định dạng đầu ra khác ngoài BMP không?**  
A: Chắc chắn – bạn có thể xuất ra PNG, JPEG, TIFF và nhiều định dạng khác bằng cách sử dụng lớp `*Options` tương ứng.

**Q: Có cần giấy phép thương mại cho việc sử dụng trong môi trường sản xuất không?**  
A: Có. Bạn có thể mua giấy phép [tại đây](https://purchase.aspose.com/buy) hoặc nhận giấy phép đánh giá tạm thời [tại đây](https://purchase.aspose.com/temporary-license/).

**Q: Tôi có thể tìm thêm trợ giúp và ví dụ ở đâu?**  
A: Diễn đàn cộng đồng Aspose.Imaging cho Java cung cấp tài liệu chi tiết và mã mẫu: [Diễn đàn Aspose.Imaging cho Java](https://forum.aspose.com/).

---

**Cập nhật lần cuối:** 2026-01-12  
**Kiểm tra với:** Aspose.Imaging for Java 24.11  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}