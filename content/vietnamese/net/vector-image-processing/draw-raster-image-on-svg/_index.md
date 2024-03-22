---
title: Cách vẽ hình ảnh raster trên SVG trong Aspose.Imaging cho .NET
linktitle: Vẽ hình ảnh raster trên SVG trong Aspose.Imaging cho .NET
second_title: API xử lý hình ảnh Aspose.Imaging .NET
description: Tìm hiểu cách vẽ hình ảnh raster trên SVG bằng Aspose.Imaging for .NET. Nâng cao ứng dụng .NET của bạn bằng hình ảnh động.
type: docs
weight: 11
url: /vi/net/vector-image-processing/draw-raster-image-on-svg/
---

Trong thế giới lập trình .NET, Aspose.Imaging là một thư viện đáng tin cậy và linh hoạt để xử lý các tác vụ khác nhau liên quan đến hình ảnh. Một khả năng hấp dẫn mà nó mang lại là khả năng vẽ hình ảnh raster trên khung vẽ SVG. Trong hướng dẫn từng bước này, chúng tôi sẽ hướng dẫn bạn quy trình vẽ hình ảnh raster trên SVG bằng Aspose.Imaging for .NET.

## Điều kiện tiên quyết

Trước khi chúng ta đi sâu vào chi tiết, hãy đảm bảo bạn có sẵn các điều kiện tiên quyết sau:

-  Aspose.Imaging for .NET: Bạn phải cài đặt thư viện. Nếu không, bạn có thể tải xuống từ[Trang tải xuống Aspose.Imaging for .NET](https://releases.aspose.com/imaging/net/).

-  Thư mục tài liệu của bạn: Thay thế`"Your Document Directory"` với đường dẫn thực tế đến thư mục làm việc của bạn.

Bây giờ, hãy chia quy trình thành các bước dễ thực hiện:

## Bước 1: Nhập các không gian tên cần thiết

Bạn cần nhập các không gian tên cần thiết để hoạt động với Aspose.Imaging:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Bước 2: Tải hình ảnh

- Đầu tiên, tải hình ảnh raster mà bạn muốn vẽ trên khung vẽ SVG.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Tiếp theo, tải hình ảnh canvas SVG vào nơi bạn muốn vẽ hình ảnh raster.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Bước 3: Vẽ lên ảnh SVG

Bây giờ, bạn có thể bắt đầu vẽ trên hình ảnh SVG hiện có. Để làm điều này, bạn cần tạo một thể hiện của`SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Bước 4: Vẽ hình ảnh raster

- Xác định giới hạn nơi bạn muốn vẽ hình ảnh raster và chỉ định vùng nguồn từ hình ảnh raster.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Bước 5: Lưu kết quả

Sau khi vẽ hình ảnh raster trên canvas SVG, bạn có thể lưu hình ảnh thu được:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Phần kết luận

Chúc mừng! Bạn đã vẽ thành công hình ảnh raster trên canvas SVG bằng Aspose.Imaging for .NET. Điều này có thể cực kỳ hữu ích để tạo hình ảnh phong phú và năng động trong các ứng dụng .NET của bạn.

 Để biết thêm thông tin và tài liệu chi tiết, hãy truy cập[Aspose.Imaging cho tài liệu .NET](https://reference.aspose.com/imaging/net/).

## Các câu hỏi thường gặp

### Aspose.Imaging cho .NET là gì?
   Aspose.Imaging for .NET là một thư viện xử lý hình ảnh mạnh mẽ cho phép các nhà phát triển tạo, thao tác và chuyển đổi hình ảnh ở nhiều định dạng khác nhau trong các ứng dụng .NET.

### Tôi có thể sử dụng Aspose.Imaging cho .NET trong các dự án thương mại không?
    Có, bạn có thể sử dụng Aspose.Imaging for .NET trong cả dự án thương mại và phi thương mại. Chi tiết cấp phép có thể được tìm thấy trên[trang mua hàng](https://purchase.aspose.com/buy).

### Có bản dùng thử miễn phí không?
    Có, bạn có thể dùng thử miễn phí Aspose.Imaging cho .NET từ[đây](https://releases.aspose.com/).

### Tôi có thể nhận hỗ trợ hoặc đặt câu hỏi ở đâu?
    Nếu có thắc mắc hoặc cần hỗ trợ, bạn có thể truy cập[Diễn đàn Aspose.Imaging](https://forum.aspose.com/).

### Làm cách nào tôi có thể nhận được giấy phép tạm thời cho Aspose.Imaging cho .NET?
    Bạn có thể nhận được giấy phép tạm thời từ[đây](https://purchase.aspose.com/temporary-license/).


