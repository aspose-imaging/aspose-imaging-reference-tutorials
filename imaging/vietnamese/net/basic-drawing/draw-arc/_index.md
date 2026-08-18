---
date: 2026-02-09
description: Tìm hiểu cách vẽ cung bằng Aspose.Imaging cho .NET, bao gồm cách lưu
  tệp BMP, thiết lập kích thước ảnh và đặt nền đồ họa. Hướng dẫn từng bước để tạo
  ảnh BMP.
linktitle: Draw Arc in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Cách vẽ cung tròn bằng Aspose.Imaging cho .NET
url: /vi/net/basic-drawing/draw-arc/
weight: 10
---

.{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Cách Vẽ Cung với Aspose.Imaging cho .NET

Trong thế giới xử lý ảnh, **how to draw arc** là một nhiệm vụ phổ biến có thể thêm nét thẩm mỹ cho bất kỳ đồ họa nào. Với Aspose.Imaging cho .NET, bạn có thể tạo ảnh BMP, đặt kích thước ảnh và vẽ một cung bằng bút chỉ trong vài dòng C#. Khi kết thúc hướng dẫn này, bạn sẽ biết chính xác cách vẽ cung, đặt nền đồ họa và lưu tệp BMP kết quả một cách dễ dàng.

## Câu trả lời nhanh
- **What does the code produce?** Ảnh BMP 100 × 100 pixel với nền màu vàng và một cung màu đen.  
- **Which library is used?** Aspose.Imaging cho .NET.  
- **Do I need a license?** Bản dùng thử miễn phí hoạt động cho phát triển; cần giấy phép thương mại cho môi trường sản xuất.  
- **Can I change the image size?** Có – sửa các tham số width và height trong lời gọi `Image.Create`.  
- **Is the output format fixed?** Ví dụ lưu tệp BMP, nhưng bất kỳ định dạng nào được Aspose.Imaging hỗ trợ đều có thể được sử dụng.

## “how to draw arc” là gì trong Aspose.Imaging?
Vẽ một cung có nghĩa là hiển thị một đoạn đường cong được xác định bởi một hình chữ nhật bao quanh, một góc bắt đầu và một góc quét. Aspose.Imaging cung cấp phương thức `Graphics.DrawArc`, cho phép bạn **draw arc with pen** và kiểm soát mọi khía cạnh hình ảnh.

## Tại sao nên sử dụng Aspose.Imaging cho nhiệm vụ này?
- **Full control** trên kích thước ảnh, độ sâu màu và định dạng tệp.  
- **No external dependencies** – mọi thứ chạy trên .NET thuần.  
- **High performance** để tạo ra số lượng lớn đồ họa trên phía máy chủ.  

## Yêu cầu trước

Trước khi chúng ta bắt đầu với mã, hãy chắc chắn rằng bạn có những thứ sau:

1. **Aspose.Imaging cho .NET** – tải xuống từ trang chính thức [here](https://releases.aspose.com/imaging/net/).  
2. **Môi trường phát triển .NET** (Visual Studio, VS Code, hoặc bất kỳ trình biên dịch C# nào).  

Bây giờ chúng ta đã có các yêu cầu trước, hãy bắt đầu vẽ!

## Nhập các Namespace cần thiết

Để làm việc với Aspose.Imaging, bạn cần đưa các namespace liên quan vào phạm vi sử dụng:

### Bước 1: Nhập các Namespace

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.Sources;
using System;
using System.Drawing;
using System.IO;
```

Các câu lệnh `using` này cho phép bạn truy cập các lớp tạo ảnh, xử lý đồ họa và I/O tệp.

## Cách Vẽ Cung với Aspose.Imaging cho .NET

Chúng ta sẽ chia quá trình thành ba bước rõ ràng: tạo ảnh, chuẩn bị bề mặt đồ họa, và cuối cùng vẽ cung.

### Bước 1: Thiết lập Ảnh (đặt kích thước ảnh & tạo ảnh BMP)

```csharp
// Specify the directory where you want to save the image
string dataDir = "Your Document Directory";

// Create an instance of FileStream to save the image
using (FileStream stream = new FileStream(dataDir + "DrawingArc_out.bmp", FileMode.Create))
{
    // Create an instance of BmpOptions and set its properties
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;

    // Set the source for BmpOptions and create an instance of Image
    saveOptions.Source = new StreamSource(stream);
    using (Image image = Image.Create(saveOptions, 100, 100))
    {
```

Ở đây chúng tôi **set image size** thành 100 × 100 pixel và cấu hình các tùy chọn BMP. `FileStream` đảm bảo chúng tôi **save BMP file** tới vị trí mong muốn.

### Bước 2: Khởi tạo Graphics và Đặt Nền Đồ họa

```csharp
        // Create and initialize an instance of Graphics class and clear the graphics surface
        Graphics graphic = new Graphics(image);
        graphic.Clear(Color.Yellow);
```

Đối tượng `Graphics` cho phép chúng ta vẽ lên ảnh. Bằng cách gọi `Clear(Color.Yellow)` chúng tôi **set graphics background** thành màu vàng sáng, làm cho cung nổi bật.

### Bước 3: Định nghĩa Tham số Cung và Vẽ Cung với Pen

```csharp
        // Define the parameters for the arc
        int width = 100;
        int height = 200;
        int startAngle = 45;
        int sweepAngle = 270;

        // Draw the arc
        graphic.DrawArc(new Pen(Color.Black), 0, 0, width, height, startAngle, sweepAngle);

        // Save the changes
        image.Save();
    }
    stream.Close();
}
```

- `width` và `height` xác định hình chữ nhật bao quanh, thực tế **set image size** cho cung.  
- Đối tượng `Pen` là thứ cho phép chúng ta **draw arc with pen** màu đen.  
- Sau khi vẽ, `image.Save()` ghi **BMP file** vào đĩa.

## Các vấn đề thường gặp & Mẹo

- **Arc not visible?** Đảm bảo màu pen tương phản với nền (ví dụ, đen trên vàng).  
- **Incorrect dimensions?** Hãy nhớ rằng hình chữ nhật bao quanh của cung có thể lớn hơn ảnh; điều chỉnh `width`/`height` hoặc kích thước ảnh cho phù hợp.  
- **Performance tip:** Tái sử dụng một thể hiện `Graphics` duy nhất nếu bạn cần vẽ nhiều hình trên cùng một ảnh.

## Câu hỏi thường gặp

### Q1: Tôi có thể tìm tài liệu cho Aspose.Imaging cho .NET ở đâu?

A1: Bạn có thể tham khảo tài liệu [here](https://reference.aspose.com/imaging/net/) để có thông tin chi tiết về Aspose.Imaging cho .NET.

### Q2: Làm sao tôi có thể tải Aspose.Imaging cho .NET?

A2: Bạn có thể tải Aspose.Imaging cho .NET từ trang web [here](https://releases.aspose.com/imaging/net/).

### Q3: Có bản dùng thử miễn phí cho Aspose.Imaging cho .NET không?

A3: Có, bạn có thể nhận phiên bản dùng thử miễn phí [here](https://releases.aspose.com/) để thử Aspose.Imaging cho .NET.

### Q4: Tôi có cần giấy phép tạm thời cho Aspose.Imaging cho .NET không?

A4: Nếu bạn cần giấy phép tạm thời, bạn có thể lấy một giấy phép [here](https://purchase.aspose.com/temporary-license/).

### Q5: Tôi có thể tìm hỗ trợ hoặc đặt câu hỏi về Aspose.Imaging cho .NET ở đâu?

A5: Bạn có thể truy cập diễn đàn Aspose.Imaging để được hỗ trợ và thảo luận [here](https://forum.aspose.com/).

---

**Cập nhật lần cuối:** 2026-02-09  
**Kiểm tra với:** Aspose.Imaging 24.11 cho .NET  
**Tác giả:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}