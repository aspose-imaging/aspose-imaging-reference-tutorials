---
date: '2026-07-08'
description: Tìm hiểu cách xuất TIFF từ DjVu bằng Aspose.Imaging cho Java. Hướng dẫn
  từng bước bao gồm việc tải, chọn trang và các tùy chọn xuất.
keywords:
- how to export tiff
- java image processing
- maven aspose imaging
- how to load djvu
lastmod: '2026-07-08'
og_description: Khám phá cách xuất TIFF từ DjVu trong Java bằng Aspose.Imaging. Thực
  hiện theo hướng dẫn từng bước của chúng tôi để chuyển đổi hình ảnh nhanh chóng và
  đáng tin cậy.
og_image_alt: Guide showing Java code to convert DjVu pages to TIFF with Aspose.Imaging
og_title: Cách xuất TIFF – Hướng dẫn Java với Aspose.Imaging
schemas:
- author: Aspose
  dateModified: '2026-07-08'
  description: Learn how to export TIFF from DjVu using Aspose.Imaging for Java. Step-by-step
    guide covering loading, page selection, and export options.
  headline: How to Export TIFF – Load and Export DjVu Pages in Java with Aspose.Imaging
  type: TechArticle
- description: Learn how to export TIFF from DjVu using Aspose.Imaging for Java. Step-by-step
    guide covering loading, page selection, and export options.
  name: How to Export TIFF – Load and Export DjVu Pages in Java with Aspose.Imaging
  steps:
  - name: '**Archival Systems** – Preserve scanned documents in a universally accepted
      format.'
    text: '**Archival Systems** – Preserve scanned documents in a universally accepted
      format.'
  - name: '**Document Review Workflows** – Pull out only the pages that need annotation.'
    text: '**Document Review Workflows** – Pull out only the pages that need annotation.'
  - name: '**Integration with DMS** – Feed TIFF images into existing document‑management
      pipelines that do not understand DjVu.'
    text: '**Integration with DMS** – Feed TIFF images into existing document‑management
      pipelines that do not understand DjVu.'
  type: HowTo
- questions:
  - answer: '`DjvuImage` represents a DjVu document in memory.'
    question: What is the main class for DjVu handling?
  - answer: Just two lines after loading the image.
    question: How many lines of code are needed to export a page to TIFF?
  - answer: '`com.aspose:aspose-imaging` (version 25.5+).'
    question: Which Maven artifact provides DjVu support?
  - answer: Yes, use `IntRange` to specify a range.
    question: Can I export multiple pages at once?
  - answer: A full license is required; a temporary trial is available.
    question: Do I need a license for production?
  type: FAQPage
tags:
- convert DjVu
- Aspose.Imaging
- Java image conversion
title: Cách xuất TIFF – Tải và xuất các trang DjVu trong Java với Aspose.Imaging
url: /vi/java/format-conversion-export/load-export-djvu-tiff-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Cách xuất TIFF – Tải và xuất các trang DjVu trong Java với Aspose.Imaging

## Giới thiệu

Nếu bạn cần **how to export TIFF** từ một tài liệu DjVu trong ứng dụng Java, bạn đã đến đúng nơi. DjVu là định dạng nén cho tài liệu quét, nhưng nhiều hệ thống downstream yêu cầu TIFF. Hướng dẫn này sẽ chỉ cho bạn cách tải tệp DjVu, chọn các trang cần thiết và xuất chúng dưới dạng hình ảnh TIFF chất lượng cao bằng Aspose.Imaging cho Java. Khi hoàn thành, bạn sẽ có một đoạn mã có thể tái sử dụng, phù hợp với bất kỳ quy trình xử lý ảnh dựa trên Java nào.

**Bạn sẽ học được**
- Cách tải ảnh DjVu bằng Aspose.Imaging trong Java  
- Xuất các trang DjVu cụ thể sang định dạng TIFF  
- Cấu hình các tùy chọn xuất và hiểu các tham số chính  

Trước khi chúng ta bắt đầu, hãy đảm bảo môi trường phát triển của bạn đáp ứng các điều kiện tiên quyết được liệt kê bên dưới.

## Câu trả lời nhanh
- **Lớp chính để xử lý DjVu là gì?** `DjvuImage` đại diện cho một tài liệu DjVu trong bộ nhớ.  
- **Cần bao nhiêu dòng mã để xuất một trang sang TIFF?** Chỉ cần hai dòng sau khi tải ảnh.  
- **Artifact Maven nào cung cấp hỗ trợ DjVu?** `com.aspose:aspose-imaging` (phiên bản 25.5+).  
- **Tôi có thể xuất nhiều trang cùng lúc không?** Có, sử dụng `IntRange` để chỉ định một phạm vi.  
- **Tôi có cần giấy phép cho môi trường sản xuất không?** Cần giấy phép đầy đủ; một bản dùng thử tạm thời có sẵn.

## “how to export tiff” là gì?
**“How to export TIFF”** đề cập đến quá trình chuyển đổi một hình ảnh hoặc trang tài liệu sang Định dạng Tệp Hình ảnh Đánh dấu (TIFF), một định dạng không mất dữ liệu được sử dụng rộng rãi cho lưu trữ và in ấn. Aspose.Imaging thực hiện chuyển đổi này trong một lời gọi API duy nhất đồng thời giữ nguyên độ phân giải và cài đặt nén. Quá trình chuyển đổi giữ lại mọi chi tiết hình ảnh, làm cho nó phù hợp cho lưu trữ lưu trữ chất lượng cao và xử lý downstream.

## Tại sao nên sử dụng Aspose.Imaging cho xử lý ảnh Java?
Aspose.Imaging hỗ trợ **150+** định dạng đầu vào và đầu ra, xử lý các tệp lên tới **5.000 trang** mà không cần tải toàn bộ tài liệu vào bộ nhớ, và cung cấp các thao tác an toàn đa luồng. Những khả năng được định lượng này khiến nó trở thành lựa chọn đáng tin cậy cho các khối lượng công việc xử lý ảnh Java có thông lượng cao, đặc biệt khi làm việc với các bộ tài liệu lớn cần chuyển đổi hàng loạt và tiêu thụ bộ nhớ tối thiểu.

## Điều kiện tiên quyết
- **Thư viện Aspose.Imaging cho Java** – phiên bản 25.5 trở lên.  
- **Bộ công cụ phát triển Java (JDK)** – 8 hoặc mới hơn, được cấu hình đúng trên máy của bạn.  
- **Kiến thức Java cơ bản** – bạn nên quen thuộc với I/O tệp và xử lý ngoại lệ.  

## Cách thiết lập Maven Aspose Imaging?
Để đưa Aspose.Imaging vào một dự án Maven, thêm phụ thuộc vào tệp `pom.xml` của dự án. Maven sẽ tải xuống thư viện và các phụ thuộc truyền tải, làm cho API có sẵn cho việc biên dịch và chạy. Sau khi thêm đoạn mã, chạy `mvn clean install` để đảm bảo artifact được giải quyết và dự án xây dựng thành công.

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

## Cách thiết lập Gradle Aspose Imaging?
Đối với các dự án Gradle, khai báo phụ thuộc Aspose.Imaging trong tệp `build.gradle`. Gradle sẽ tải thư viện từ Maven Central, cho phép bạn sử dụng API trong mã Java. Sau khi cập nhật script, làm mới dự án để tải xuống JAR và đồng bộ các phụ thuộc.

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

## Tải xuống trực tiếp
Bạn cũng có thể tải xuống JAR mới nhất từ [Aspose.Imaging releases](https://releases.aspose.com/imaging/java/).

### Mua giấy phép
- **Dùng thử miễn phí** – nhận giấy phép tạm thời để đánh giá.  
- **Mua** – cân nhắc mua giấy phép đầy đủ cho việc sử dụng trong môi trường sản xuất.

## Khởi tạo và Cấu hình
Trước khi sử dụng bất kỳ API nào, bạn phải khởi tạo thư viện. `License` là một lớp được sử dụng để áp dụng tệp giấy phép Aspose.Imaging của bạn vào thư viện, đảm bảo đầy đủ chức năng mà không có giới hạn đánh giá.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path/to/your/license.lic");
```

## Cách tải DjVu?
DjvuImage là đối tượng cấp cao nhất đại diện cho một tệp DjVu trong bộ nhớ. Để đọc tài liệu DjVu, gọi phương thức tĩnh `Image.load()` với đường dẫn tệp; phương thức này trả về một thể hiện `Image` mà bạn sẽ ép kiểu thành `DjvuImage`. `Image.load()` là một phương thức tĩnh đọc tệp ảnh và trả về một đối tượng `Image` đại diện cho nội dung đã tải.

```java
   String dataDir = "YOUR_DOCUMENT_DIRECTORY" + "/Sample.djvu";
   ```

```java
   try (DjvuImage image = (DjvuImage) Image.load(dataDir)) {
       // The image is now loaded and ready for further processing.
   }
   ```

### Khắc phục sự cố
- Xác minh đường dẫn tệp đúng và có thể truy cập.  
- Bao quanh lời gọi load trong khối try‑catch để xử lý `IOException` hoặc `ImageLoadException`.

## Cách xuất TIFF?
Xuất một trang DjVu sang TIFF bao gồm việc tạo một đối tượng `TiffOptions` để chỉ định nén, độ phân giải và các cài đặt khác, sau đó gọi phương thức `save()` trên trang mong muốn. `TiffOptions` là một lớp chứa cấu hình cho đầu ra TIFF, như loại nén và độ sâu màu. Sử dụng `IntRange` để chọn các trang cần chuyển đổi, sau đó lặp và lưu mỗi trang dưới dạng một tệp TIFF riêng.

Tạo thư mục đầu ra, thiết lập `TiffOptions`, chọn các trang bằng `IntRange`, và cuối cùng lưu mỗi trang dưới dạng tệp TIFF.

```java
   String outputDir = "YOUR_OUTPUT_DIRECTORY" + "/ConvertDjvuPagesToTiff_out.tiff";
   ```

```java
   TiffOptions exportOptions = new TiffOptions(TiffExpectedFormat.TiffDeflateBw);
   ```

```java
   IntRange range = new IntRange(0, 2); // Export the first three pages.
   exportOptions.setMultiPageOptions(new DjvuMultiPageOptions(range));
   ```

```java
   try (DjvuImage image = (DjvuImage) Image.load(dataDir)) {
       image.save(outputDir, exportOptions);
   }
   ```

### Những lỗi thường gặp
- Đảm bảo `outputDir` tồn tại; nếu không `save()` sẽ ném ra ngoại lệ.  
- Nhớ rằng chỉ mục trang là **zero‑based**; trang 1 có chỉ mục 0.

## Ứng dụng thực tiễn
Xuất các trang DjVu sang TIFF hữu ích trong nhiều kịch bản:

1. **Hệ thống lưu trữ** – Bảo quản tài liệu quét ở định dạng được chấp nhận rộng rãi.  
2. **Quy trình xem xét tài liệu** – Lấy ra chỉ những trang cần chú thích.  
3. **Tích hợp với DMS** – Cung cấp hình ảnh TIFF vào các pipeline quản lý tài liệu hiện có không hỗ trợ DjVu.

## Xem xét hiệu năng
Khi xử lý các tệp DjVu lớn:

- Sử dụng **try‑with‑resources** để tự động đóng các luồng và giải phóng bộ nhớ.  
- Xử lý tệp theo từng khối (ví dụ, 10 trang mỗi lần) để giữ dung lượng heap thấp.  
- Ưu tiên `TiffCompression.CCITT4` cho các bản quét đen‑trắng để giảm kích thước tệp mà không mất chất lượng.

## Câu hỏi thường gặp
**Q:** Làm thế nào để cài đặt Aspose.Imaging cho Java trong dự án của tôi?  
**A:** Sử dụng Maven hoặc Gradle như đã trình bày ở trên, hoặc tải trực tiếp từ [trang phát hành của Aspose](https://releases.aspose.com/imaging/java/).

**Q:** Tôi có thể xuất ảnh DjVu sang các định dạng khác ngoài TIFF không?  
**A:** Có, Aspose.Imaging cũng hỗ trợ PNG, JPEG, BMP và nhiều định dạng khác.

**Q:** Tôi nên làm gì nếu tệp giấy phép của tôi không được nhận dạng?  
**A:** Kiểm tra lại đường dẫn giấy phép đúng và bạn đã gọi `License.setLicense()` trước bất kỳ lần sử dụng API nào khác.

**Q:** Làm thế nào để xử lý hiệu quả các tệp DjVu rất lớn?  
**A:** Xử lý tài liệu theo các phạm vi trang nhỏ hơn và giải phóng nhanh mỗi thể hiện `DjvuImage` để tránh áp lực bộ nhớ.

**Q:** Aspose.Imaging có miễn phí cho việc sử dụng thương mại không?  
**A:** Giấy phép dùng thử tạm thời là miễn phí, nhưng cần mua giấy phép cho các triển khai sản xuất.

## Tài nguyên
- **Tài liệu**: [Aspose.Imaging Java API Reference](https://reference.aspose.com/imaging/java/)  
- **Tải xuống**: [Aspose.Imaging for Java Releases](https://releases.aspose.com/imaging/java/)  
- **Mua**: [Buy Aspose.Imaging](https://purchase.aspose.com/buy)  
- **Giấy phép miễn phí**: [Get a Free License](https://releases.aspose.com/imaging/java/)  
- **Giấy phép tạm thời**: [Request a Temporary License](https://purchase.aspose.com/temporary-license/)  
- **Hỗ trợ**: [Aspose Community Forum](https://forum.aspose.com/c/imaging/14)

Bằng cách nắm vững các bước trên, bạn có thể tin cậy **how to export TIFF** từ các tệp DjVu trong bất kỳ giải pháp nào dựa trên Java. Chúc lập trình vui vẻ!

---

**Cập nhật lần cuối:** 2026-07-08  
**Kiểm tra với:** Aspose.Imaging 25.5 for Java  
**Tác giả:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Hướng dẫn liên quan
- [Tạo TIFF đa trang với Aspose.Imaging cho Java: Hướng dẫn toàn diện](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [Chuyển đổi DjVu sang PDF bằng Aspose.Imaging cho Java - Hướng dẫn từng bước](/imaging/java/image-loading-saving/convert-djvu-to-pdf-aspose-imaging-java/)
- [Chuyển đổi DJVU sang BMP trong Java với Aspose.Imaging: Hướng dẫn từng bước](/imaging/java/format-conversion-export/export-djvu-pages-bmp-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}