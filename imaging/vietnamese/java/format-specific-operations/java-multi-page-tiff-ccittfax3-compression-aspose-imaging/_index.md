---
date: '2026-09-28'
description: Tìm hiểu cách sử dụng ccittfax3 compression java để tạo các tệp TIFF
  đa trang với Aspose.Imaging. Quét, lưu trữ hiệu quả và giảm kích thước tệp cho quy
  trình công việc tài liệu.
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: Khám phá hướng dẫn từng bước cách sử dụng ccittfax3 compression java
  với Aspose.Imaging để xây dựng các tệp TIFF đa trang hiệu quả cho việc quét và lưu
  trữ.
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: Cách tạo TIFF đa trang bằng nén ccittfax3 trong java
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to use ccittfax3 compression java to create multi-page TIFF
    files with Aspose.Imaging. Efficiently scan, archive, and reduce file size for
    document workflows.
  headline: How to create multi-page TIFF with ccittfax3 compression java
  type: TechArticle
- questions:
  - answer: CCITTFAX3 is limited to monochrome data; for color use JPEG or LZW compression
      instead.
    question: Can I use this approach with color images?
  - answer: Yes—the library writes each frame directly to the output stream, keeping
      memory usage low even for thousands of pages.
    question: Does Aspose.Imaging support streaming for huge TIFFs?
  - answer: Load the `.lic` file with `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.
    question: How do I apply a temporary license programmatically?
  - answer: You can render each `TiffFrame` to a `BufferedImage` and display it in
      a Swing component.
    question: Is there a way to preview the TIFF before saving?
  - answer: Aspose.Imaging supports Java 8 through Java 21, including LTS releases.
    question: Which Java versions are officially supported?
  type: FAQPage
tags:
- ccittfax3 compression
- Aspose.Imaging
- Java TIFF
- image compression
- document scanning
title: Cách tạo TIFF đa trang bằng nén ccittfax3 trong java
url: /vi/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Làm chủ việc tạo TIFF đa trang với nén ccittfax3 trong Java sử dụng Aspose.Imaging

## Giới thiệu

Nếu bạn cần lưu trữ một khối lượng lớn tài liệu đã quét trong khi giữ kích thước tệp thấp, **ccittfax3 compression java** là giải pháp tối ưu. Hướng dẫn này sẽ chỉ cho bạn cách tạo các tệp TIFF đa trang với nén CCITTFAX3 trong Java bằng Aspose.Imaging. Bạn sẽ tìm hiểu tại sao việc nén này hoạt động tốt cho các bản quét đơn sắc, cách cấu hình thư viện và cách thêm mỗi trang dưới dạng khung.

**Bạn sẽ học gì**
- Cách thêm Aspose.Imaging vào dự án Java.
- Cách cấu hình `TiffOptions` cho nén CCITTFAX3.
- Cách tạo `TiffImage`, thay đổi kích thước ảnh nguồn và thêm chúng dưới dạng khung.
- Cách lưu TIFF đa trang cuối cùng một cách hiệu quả.

Hãy cùng đi qua triển khai đầy đủ.

## Câu trả lời nhanh
- **Lợi ích chính của nén CCITTFAX3 là gì?** Giảm tới 80 % kích thước tệp cho các bản quét đen‑trắng.  
- **Thư viện nào cung cấp hỗ trợ tích hợp?** Aspose.Imaging cho Java, phiên bản 25.5+.  
- **Tôi có cần giấy phép cho việc phát triển không?** Giấy phép dùng thử miễn phí hoạt động cho tất cả tính năng; giấy phép trả phí cần thiết cho môi trường sản xuất.  
- **Tôi có thể xử lý hàng trăm trang không?** Có — Aspose.Imaging truyền các trang, vì vậy việc sử dụng bộ nhớ vẫn thấp.  
- **Mã có tương thích với Java 11 và các phiên bản sau không?** Hoàn toàn; API nhắm tới Java 8+.

## ccittfax3 compression java là gì?
`CCITTFAX3` là một thuật toán nén đơn sắc, không mất dữ liệu, được thiết kế cho fax và ảnh tài liệu đã quét. Nó mã hoá mỗi pixel thành một bit duy nhất, cung cấp đầu ra chất lượng cao trong khi giảm đáng kể kích thước tệp — thường giảm 70‑80 % so với TIFF không nén. Điều này làm cho nó lý tưởng cho việc lưu trữ tài liệu đen‑trắng nơi cần duy trì độ chính xác.

## Tại sao nên sử dụng Aspose.Imaging cho nhiệm vụ này?
Aspose.Imaging hỗ trợ **hơn 100** định dạng đầu vào và đầu ra, bao gồm PDF, PNG, JPEG và TIFF. Kiến trúc streaming của nó có thể xử lý các tệp TIFF **hàng trăm trang** mà không cần tải toàn bộ tài liệu vào bộ nhớ, làm cho nó trở thành lựa chọn lý tưởng cho các dự án lưu trữ quy mô lớn.

## Yêu cầu trước

- **Java Development Kit (JDK)** 8 hoặc mới hơn đã được cài đặt.
- **IDE** như IntelliJ IDEA hoặc Eclipse.
- **Maven** hoặc **Gradle** để quản lý phụ thuộc.
- Kiến thức cơ bản về Java (lớp, đối tượng, collection).

## Cài đặt Aspose.Imaging cho Java

Thêm thư viện vào tệp build của bạn.

**Maven:**  
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```  

**Gradle:**  
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```  

### Tải trực tiếp

Bạn cũng có thể tải JAR mới nhất từ [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

### Nhận giấy phép

Giấy phép dùng thử miễn phí có sẵn tại [Aspose's Free Trial page](https://releases.aspose.com/imaging/java/). Đối với sử dụng trong môi trường sản xuất, mua giấy phép vĩnh viễn hoặc yêu cầu giấy phép tạm thời tại [Aspose Purchase](https://purchase.aspose.com/temporary-license/).

Để biết chi tiết cách sử dụng API, xem tài liệu Aspose.Imaging cho Java [documentation](https://reference.aspose.com/imaging/java/).

### Khởi tạo cơ bản

Sau khi thêm phụ thuộc, khởi tạo thư viện như dưới đây.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## Cách cấu hình ccittfax3 compression java cho TIFF đa trang?

`TiffOptions` là một lớp định nghĩa định dạng đầu ra và cài đặt nén cho tệp TIFF. Tải đối tượng `TiffOptions` với enum `CCITTGroup3FaxCompression`, sau đó đặt nguồn tệp đầu ra. Cấu hình hai bước này chuẩn bị bộ ghi cho nén đơn sắc và đảm bảo rằng mọi trang được thêm sau sẽ được mã hoá bằng thuật toán CCITTFAX3, mang lại việc giảm kích thước đáng kể trong khi giữ nguyên chất lượng ảnh.

```java
    import com.aspose.imaging.fileformats.tiff.TiffExpectedFormat;
    import com.aspose.imaging.imageoptions.TiffOptions;
    import com.aspose.imaging.sources.FileCreateSource;

    TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.TiffCcittFax3);
    ```  

```java
    // Replace "YOUR_OUTPUT_DIRECTORY" with your actual directory path
    outputSettings.setSource(new FileCreateSource("YOUR_OUTPUT_DIRECTORY/output.tiff", false));
    ```  

## Cách tạo một thể hiện TiffImage trong Java?

`TiffImage` đại diện cho một tài liệu TIFF đa trang trong bộ nhớ và cung cấp các phương thức để thao tác các khung. Đầu tiên, xác định chiều rộng và chiều cao mà tất cả các trang sẽ chia sẻ. Sau đó khởi tạo `TiffImage` bằng cách sử dụng `TiffOptions` đã tạo trước đó. Đối tượng `TiffImage` hoạt động như một container cho các khung riêng lẻ, cho phép bạn thêm, xóa hoặc sắp xếp lại các trang trước khi lưu tệp cuối cùng.

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## Cách tải và thay đổi kích thước ảnh nguồn từ thư mục?

Lọc thư mục mục tiêu để tìm các tệp JPEG, đọc từng ảnh và thay đổi kích thước sao cho phù hợp với canvas TIFF. Thay đổi kích thước trước khi thêm khung giảm tiêu thụ bộ nhớ và tăng tốc quá trình lưu. Bằng cách chuyển đổi mỗi ảnh nguồn sang kích thước và định dạng pixel yêu cầu, bạn đảm bảo bố cục trang nhất quán và tránh lỗi thời gian chạy khi các khung được thêm vào tài liệu TIFF.

```java
    import java.io.File;
    import java.io.FilenameFilter;

    final File folder = new File("samples/");
    File[] files = folder.listFiles(new FilenameFilter() {
        public boolean accept(File dir, String name) {
            return name.toLowerCase().endsWith(".jpg");
        }
    });

    if (files == null) return;
    ```  

```java
    import com.aspose.imaging.RasterImage;
    import com.aspose.imaging.ResizeType;

    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);
    }
    ```  

## Cách thêm mỗi ảnh làm khung vào TIFF đa trang?

`TiffFrame` là một đối tượng chứa một ảnh trang duy nhất và siêu dữ liệu liên quan trong TIFF. Lặp qua các ảnh đã thay đổi kích thước, tạo một `TiffFrame` mới và thêm nó vào `TiffImage`. Mỗi khung trở thành một trang riêng trong tài liệu cuối cùng, và thư viện tự động xử lý các cập nhật siêu dữ liệu cần thiết, như số trang và offset, đảm bảo cấu trúc TIFF đa trang hợp lệ.

```java
    import com.aspose.imaging.fileformats.tiff.TiffFrame;

    int index = 0;
    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);

        TiffFrame frame = tiffImage.getActiveFrame();
        frame.savePixels(frame.getBounds(), image.loadPixels(image.getBounds()));

        if (index > 0) {
            frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            tiffImage.addFrame(frame);
        }
        index++;
    }
    ```  

## Cách lưu tệp TIFF đa trang cuối cùng?

Gọi phương thức `save` trên thể hiện `TiffImage`, truyền đường dẫn đầu ra mong muốn. Thư viện tự động ghi tất cả các khung bằng nén CCITTFAX3, truyền dữ liệu ra đĩa một cách hiệu quả và đóng mọi tài nguyên nền. Sau khi thao tác lưu hoàn tất, tệp kết quả chứa tất cả các trang với nén đã chỉ định, sẵn sàng cho việc phân phối hoặc lưu trữ.

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## Ứng dụng thực tiễn

- **Lưu trữ tài liệu:** Lưu các hợp đồng, hoá đơn hoặc hồ sơ pháp lý đã quét với chi phí lưu trữ tối thiểu.  
- **Hình ảnh y tế:** Nén các ảnh chụp X-quang trong khi giữ nguyên chi tiết chẩn đoán.  
- **Sản xuất in ấn:** Tạo các công việc in đa trang mà máy in có thể tiêu thụ trực tiếp.

## Các cân nhắc về hiệu năng

- Sử dụng `ResizeOptions` giữ tỷ lệ khung hình để tránh biến dạng.  
- Đóng mỗi đối tượng `Image` sau khi thêm khung để giải phóng bộ nhớ gốc.  
- Đối với các lô lớn, xử lý tệp bằng streams song song và ghi mỗi đoạn TIFF một cách bất đồng bộ.

## Những khó khăn thường gặp và cách khắc phục

- **Định dạng pixel không đúng:** CCITTFAX3 chỉ hoạt động với ảnh 1‑bit (đen‑trắng). Chuyển ảnh màu sang thang xám trước khi thay đổi kích thước.  
- **Rò rỉ bộ nhớ:** Luôn gọi `dispose()` trên các đối tượng `Image` tạm thời; nếu không, bộ đệm gốc sẽ vẫn được cấp phát.  
- **Kích thước tệp không giảm:** Đảm bảo thuộc tính nén của `TiffOptions` được đặt; nếu không, mặc định (không nén) sẽ được sử dụng.

## Câu hỏi thường gặp

**Q: Tôi có thể sử dụng cách này với ảnh màu không?**  
A: CCITTFAX3 chỉ giới hạn cho dữ liệu đơn sắc; đối với màu, sử dụng nén JPEG hoặc LZW thay thế.

**Q: Aspose.Imaging có hỗ trợ streaming cho các TIFF khổng lồ không?**  
A: Có — thư viện ghi mỗi khung trực tiếp vào luồng đầu ra, giữ mức sử dụng bộ nhớ thấp ngay cả với hàng ngàn trang.

**Q: Làm thế nào để áp dụng giấy phép tạm thời bằng chương trình?**  
A: Tải tệp `.lic` bằng `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.

**Q: Có cách nào để xem trước TIFF trước khi lưu không?**  
A: Bạn có thể render mỗi `TiffFrame` thành `BufferedImage` và hiển thị trong một component Swing.

**Q: Các phiên bản Java nào được hỗ trợ chính thức?**  
A: Aspose.Imaging hỗ trợ Java 8 đến Java 21, bao gồm các bản phát hành LTS.

## Kết luận

Bây giờ bạn đã có một quy trình hoàn chỉnh, sẵn sàng cho sản xuất để tạo các tệp TIFF đa trang với **ccittfax3 compression java** bằng Aspose.Imaging. Bằng cách làm theo các bước trên, bạn có thể lưu trữ hiệu quả các bộ sưu tập tài liệu lớn trong khi giảm chi phí lưu trữ và duy trì chất lượng ảnh cao. Khám phá các tính năng bổ sung của Aspose.Imaging — như OCR, xử lý siêu dữ liệu và chuyển đổi định dạng — để nâng cao hơn nữa quy trình xử lý tài liệu của bạn.

---

**Cập nhật lần cuối:** 2026-09-28  
**Kiểm tra với:** Aspose.Imaging 25.5 for Java  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Cách tạo TIFF đa trang với Aspose.Imaging cho Java – Hướng dẫn đầy đủ](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [Cách giảm kích thước tệp ảnh bằng nén LZW trong Java](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [Tách các khung TIFF đa trang với Aspose.Imaging cho Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}