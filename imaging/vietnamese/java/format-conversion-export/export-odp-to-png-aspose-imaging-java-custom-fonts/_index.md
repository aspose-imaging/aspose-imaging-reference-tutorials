---
date: '2026-06-28'
description: Tìm hiểu cách chuyển đổi ODP sang PNG bằng Aspose.Imaging cho Java, thiết
  lập phông chữ tùy chỉnh và tắt phông chữ hệ thống để hiển thị chính xác.
keywords:
- how to convert odp
- maven aspose imaging
- aspose imaging license
- disable system fonts
- java convert presentation image
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  headline: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts
    & Export Guide
  type: TechArticle
- description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  name: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts & Export
    Guide
  steps:
  - name: '**Free Trial** – No license required, limited features.'
    text: '**Free Trial** – No license required, limited features.'
  - name: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
    text: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
  - name: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
    text: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
  - name: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
    text: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
  type: HowTo
- questions:
  - answer: Aspose.Imaging for Java works with JDK 8 and newer; JDK 11 is recommended
      for long‑term support.
    question: What is the minimum Java version required?
  - answer: Yes, set `rasterizationOptions.setPageNumber(specificSlideIndex)` before
      calling `save`.
    question: Can I convert only selected slides?
  - answer: Load the file with `LoadOptions` that includes the password, then proceed
      with the same font settings.
    question: How do I handle password‑protected ODP files?
  - answer: It marginally improves speed because the engine skips the lookup of system
      fonts, especially noticeable on machines with large font collections.
    question: Does disabling system fonts affect performance?
  - answer: Explore the official [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      for additional scenarios such as batch conversion and image transformations.
    question: Where can I find more code samples?
  type: FAQPage
title: Cách chuyển đổi ODP sang PNG với Aspose.Imaging cho Java – Hướng dẫn phông
  chữ tùy chỉnh & xuất
url: /vi/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Cách Chuyển Đổi ODP sang PNG với Aspose.Imaging cho Java – Phông chữ Tùy chỉnh & Hướng dẫn Xuất

Trong các ứng dụng Java hiện đại, việc chuyển đổi các tệp OpenDocument Presentation (ODP) sang hình ảnh PNG chất lượng cao là một yêu cầu phổ biến—đặc biệt khi bạn cần giữ nguyên thương hiệu thông qua phông chữ tùy chỉnh. Hướng dẫn này trình bày **cách chuyển đổi ODP** sang PNG bằng Aspose.Imaging cho Java, hướng dẫn bạn cách thiết lập thư mục phông chữ tùy chỉnh, tắt phông chữ dự phòng của hệ thống, và tinh chỉnh các tùy chọn rasterization để đạt hiệu suất tối ưu.

**Bạn sẽ học được**
- Cách thiết lập thư mục phông chữ tùy chỉnh cho việc chuyển đổi ODP.  
- Cách tắt phông chữ thay thế của hệ thống để chỉ sử dụng các kiểu chữ bạn chọn.  
- Cách xuất tệp ODP sang PNG với kích thước và cài đặt phông chữ chính xác.  
- Mẹo cải thiện tốc độ và việc sử dụng bộ nhớ khi xử lý các bản trình bày lớn.

## Câu trả lời nhanh
- **Có thể sử dụng Maven để thêm Aspose.Imaging không?** Có, thêm phụ thuộc Maven và chạy `mvn install`.  
- **Có cần giấy phép cho môi trường sản xuất không?** Cần một giấy phép Aspose.Imaging hợp lệ để sử dụng không giới hạn.  
- **Phông chữ tùy chỉnh của tôi có được tôn trọng không?** Thiết lập thư mục phông chữ và tắt các phông chữ thay thế của hệ thống để áp dụng chúng.  
- **Các định dạng hình ảnh nào được hỗ trợ?** Aspose.Imaging hỗ trợ hơn 120 định dạng raster và vector, bao gồm PNG, JPEG, TIFF và WebP.  
- **API có an toàn với đa luồng không?** Có, hầu hết các lớp Aspose.Imaging đều an toàn khi sử dụng đồng thời nếu bạn tạo các instance riêng cho mỗi luồng.

## “how to convert odp” là gì?
*“How to convert odp”* đề cập đến quá trình chuyển đổi một tệp OpenDocument Presentation sang định dạng khác—thường là PNG—trong khi giữ nguyên bố cục, phông chữ và độ trung thực hình ảnh. Aspose.Imaging cho Java cung cấp một quy trình làm việc bằng một phương thức duy nhất, xử lý việc chuyển đổi này mà không cần công cụ bên ngoài, cho phép các nhà phát triển tích hợp chuyển đổi trực tiếp vào ứng dụng của họ với ít mã nhất.

## Tại sao nên sử dụng Aspose.Imaging cho Java?
Aspose.Imaging hỗ trợ **hơn 120 định dạng đầu ra** và có thể rasterize các tệp ODP đa trang mà không cần tải toàn bộ tài liệu vào bộ nhớ, giảm mức sử dụng RAM tối đa lên tới 70 % trên các bản trình bày lớn. Thư viện còn cung cấp quản lý phông chữ tích hợp, loại bỏ nhu cầu sử dụng các engine render của bên thứ ba.

## Yêu cầu trước
- **Thư viện**: Aspose.Imaging cho Java ≥ 25.5.  
- **JDK**: Phiên bản 8 hoặc mới hơn.  
- **IDE**: IntelliJ IDEA, Eclipse, hoặc bất kỳ trình soạn thảo nào hỗ trợ Java.  
- **Kiến thức cơ bản**: Java I/O, lập trình hướng đối tượng, và các khái niệm về hình ảnh.

## Hướng dẫn Cài đặt

### Maven
Thêm phụ thuộc sau vào tệp `pom.xml` của bạn và chạy `mvn clean install`:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
Bao gồm thư viện trong tệp `build.gradle` của bạn và làm mới dự án:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Tải trực tiếp
Tải xuống JAR mới nhất từ [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

## Các bước lấy giấy phép
Để mở khóa đầy đủ chức năng, áp dụng giấy phép tạm thời hoặc vĩnh viễn:

1. **Dùng thử miễn phí** – Không cần giấy phép, tính năng có hạn.  
2. **Giấy phép tạm thời** – Yêu cầu một giấy phép trên [trang web Aspose](https://purchase.aspose.com/temporary-license/).  
3. **Mua** – Mua giấy phép thuê bao hoặc vĩnh viễn từ [trang mua Aspose](https://purchase.aspose.com/buy).

Khởi tạo thư viện với tệp giấy phép của bạn:

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## Cách thiết lập thư mục phông chữ tùy chỉnh cho việc chuyển đổi ODP?
`FontSettings` là một lớp quản lý tài nguyên phông chữ cho Aspose.Imaging. Tải các phông chữ tùy chỉnh của bạn trước khi bất kỳ xử lý hình ảnh nào bắt đầu. Điều này đảm bảo mỗi slide sử dụng đúng kiểu chữ bạn cung cấp.

Thiết lập đường dẫn thư mục phông chữ bằng cách sử dụng `FontSettings` của Aspose.Imaging:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*Định nghĩa*: `FontSettings.setFontsFolder` cho Aspose.Imaging biết nơi tìm các phông chữ TrueType và OpenType trên hệ thống tệp.

## Cách tắt phông chữ thay thế của hệ thống trong quá trình chuyển đổi ODP?
Việc tắt các phông chữ thay thế của hệ thống buộc engine render bỏ qua các phông chữ đã cài đặt trên hệ điều hành, đảm bảo chỉ các phông chữ bạn cung cấp mới được sử dụng. Điều này loại bỏ các sự thay thế phông chữ không mong muốn có thể làm thay đổi giao diện hình ảnh của các slide.

Tắt các phông chữ thay thế của hệ thống bằng lệnh sau:

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*Định nghĩa*: `FontSettings.setGetSystemAlternativeFont(false)` buộc engine chỉ sử dụng các phông chữ nằm trong thư mục bạn đã định nghĩa, loại bỏ các sự thay thế không mong muốn.

## Cách xuất tệp ODP sang PNG với phông chữ được chỉ định?
`RasterizationOptions` xác định cách các trang vector được rasterize thành hình ảnh bitmap. Bằng cách kết hợp cấu hình phông chữ với các cài đặt rasterization, bạn có thể kiểm soát DPI, màu nền và kích thước trang cho mỗi PNG được xuất.

Triển khai phương thức xuất như dưới đây:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.Image;
  import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
  import com.aspose.imaging.imageoptions.PngOptions;

  private static void exportToPng(String filePath, String defaultFontName, String outfileName) {
      FontSettings.setDefaultFontName(defaultFontName);
      try (Image document = Image.load(filePath)) {
          PngOptions saveOptions = new PngOptions();
          
          OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
          rasterizationOptions.setPageWidth(1000); // Set the page width for rendering
          rasterizationOptions.setPageHeight(1000);  // Set the page height for rendering

          saveOptions.setVectorRasterizationOptions(rasterizationOptions);
          document.save(outfileName, saveOptions);
      }
  }

  ```

*Định nghĩa*: Lớp `RasterizationOptions` kiểm soát DPI, kích thước trang và màu nền cho các tệp PNG được tạo.

### Các vấn đề thường gặp & Giải pháp
- **Thiếu tệp phông chữ** – Kiểm tra rằng mọi tệp `.ttf` hoặc `.otf` được tham chiếu trong ODP đều có trong thư mục bạn đã thiết lập.  
- **Đường dẫn tệp không đúng** – Sử dụng đường dẫn tuyệt đối hoặc giải quyết đường dẫn tương đối dựa trên `System.getProperty("user.dir")`.  
- **Quyền không đủ** – Đảm bảo quá trình Java có thể đọc thư mục phông chữ và ghi vào thư mục đầu ra.

## Ứng dụng thực tiễn
1. **Bộ slide đồng nhất thương hiệu** – Xuất bản trình chiếu dưới dạng PNG cho việc xuất bản trên web đồng thời giữ nguyên phông chữ doanh nghiệp.  
2. **Tự động tạo báo cáo** – Chuyển đổi mỗi slide thành hình ảnh để chèn vào báo cáo PDF hoặc bản tin email.  
3. **Tạo kho lưu trữ cũ** – Lưu nội dung ODP dưới dạng PNG để đảm bảo khả năng truy cập trong tương lai mà không cần trình xem ODP.

## Các cân nhắc về hiệu suất
- Sử dụng phiên bản Aspose.Imaging mới nhất để tận dụng các cải tiến rasterization đa luồng (tốc độ lên tới 2× nhanh hơn trên CPU 8 nhân).  
- Đặt xử lý hình ảnh trong khối try‑with‑resources để đảm bảo giải phóng tài nguyên gốc kịp thời.  
- Điều chỉnh `RasterizationOptions` (ví dụ, giảm DPI) khi xử lý hàng ngàn slide để cân bằng chất lượng và việc sử dụng bộ nhớ.

## Câu hỏi thường gặp

**Hỏi: Yêu cầu tối thiểu phiên bản Java nào?**  
Trả lời: Aspose.Imaging cho Java hoạt động với JDK 8 và mới hơn; JDK 11 được khuyến nghị cho hỗ trợ lâu dài.

**Hỏi: Có thể chuyển đổi chỉ các slide được chọn không?**  
Trả lời: Có, thiết lập `rasterizationOptions.setPageNumber(specificSlideIndex)` trước khi gọi `save`.

**Hỏi: Làm thế nào để xử lý các tệp ODP được bảo vệ bằng mật khẩu?**  
Trả lời: Tải tệp bằng `LoadOptions` có chứa mật khẩu, sau đó tiếp tục với cùng các cài đặt phông chữ.

**Hỏi: Việc tắt phông chữ hệ thống có ảnh hưởng đến hiệu suất không?**  
Trả lời: Nó cải thiện tốc độ một chút vì engine bỏ qua việc tra cứu phông chữ hệ thống, đặc biệt rõ rệt trên máy có bộ sưu tập phông chữ lớn.

**Hỏi: Tôi có thể tìm thêm mẫu mã ở đâu?**  
Trả lời: Khám phá [tài liệu chính thức của Aspose.Imaging](https://reference.aspose.com/imaging/java/) để biết các kịch bản bổ sung như chuyển đổi hàng loạt và biến đổi hình ảnh.

## Tài nguyên bổ sung
- [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging Releases](https://releases.aspose.com/imaging/java/)  
- [Bắt đầu dùng thử miễn phí](https://releases.aspose.com/imaging/java/)  
- [Tài liệu Aspose.Imaging](https://reference.aspose.com/imaging/java/)  
- [Diễn đàn Aspose.Imaging](https://forum.aspose.com/c/imaging/14)  
- [Mua giấy phép Aspose](https://purchase.aspose.com/buy)  
- [Đăng ký giấy phép tạm thời](https://purchase.aspose.com/temporary-license/)  

---

**Cập nhật lần cuối:** 2026-06-28  
**Kiểm tra với:** Aspose.Imaging cho Java 25.5  
**Tác giả:** Aspose

## Hướng dẫn liên quan

- [Chuyển đổi ODG sang PNG với Aspose.Imaging cho Java: Hướng dẫn đầy đủ](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [Chuyển đổi hình ảnh hiệu quả trong Java với Aspose.Imaging: Hướng dẫn đầy đủ](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}