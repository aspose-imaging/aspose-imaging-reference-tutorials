---
date: 2026-01-30
description: Tìm hiểu cách vẽ văn bản lên hình ảnh, vẽ các hình dạng lên hình ảnh
  và lấp đầy các hình dạng bằng mẫu sử dụng Aspose.Imaging cho .NET.
linktitle: Draw Using GraphicsPath – draw text on image, shapes and patterns
second_title: Aspose.Imaging .NET Image Processing API
title: Cách vẽ văn bản lên hình ảnh với Aspose.Imaging cho .NET
url: /vi/net/advanced-drawing/draw-using-graphicspath/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Cách Vẽ Văn Bản lên Hình Ảnh với Aspose.Imaging cho .NET

Trong tutorial này chúng ta sẽ hướng dẫn **cách vẽ văn bản lên hình ảnh** đồng thời chỉ ra cách vẽ các hình dạng lên hình ảnh và tô đầy các hình dạng bằng mẫu sử dụng thư viện mạnh mẽ Aspose.Imaging. Dù bạn đang xây dựng công cụ báo cáo, trình tạo thẻ tùy chỉnh, hay chỉ cần chú thích ảnh một cách lập trình, các bước dưới đây sẽ cung cấp nền tảng vững chắc.

## Trả Lời Nhanh
- **Tôi có thể vẽ gì?** Văn bản, các hình dạng cơ bản (ellipse, rectangle) và các tô đầy có mẫu.  
- **Lớp trung tâm là gì?** `GraphicsPath` kết hợp với `Graphics`.  
- **Có cần giấy phép không?** Bản dùng thử miễn phí đủ cho phát triển; giấy phép bắt buộc cho môi trường production.  
- **Các định dạng được hỗ trợ?** BMP, PNG, JPEG, TIFF và nhiều định dạng khác qua Aspose.Imaging.  
- **Yêu cầu trước?** Visual Studio, .NET 6+ (hoặc .NET Framework 4.6+), và Aspose.Imaging cho .NET.

## Aspose.Imaging là gì và cách vẽ văn bản lên hình ảnh?
Aspose.Imaging cung cấp hoá các lời gọi GDI+ cấp thấp. Bằng cách sử dụng đối tượng `Graphics` vector — văn bản, hình dạng và các tô đầy có mẫu — và render chúng lên bitmap hoặc bất kỳ định dạng ảnh nào được hỗ trợ.

## Tại sao lại vẽ hình dạng lên ảnh và tô đầy.  
 bản và đồ họa.  
- **Đồ họa động:** Tạo biểu đồ, thẻ, hoặc chứng chỉ ngay lập tức mà không cần công cụ thiết kế bên ngoài.

## Yêu Cầu Trước

1. **Visual Studio** – bất kỳ phiên bản gần đây nào (Community, Professional, hoặc Enterprise).  
2. **Aspose.Imaging cho .NET** – tải về từ trang chính thức: [Tải xuống Aspose.Imaging cho .NET](https://releases.aspose.com/imaging/net/).  
3. **Kiến thức C# cơ bản** – bạn nên quen thuộc với lớp, không gian tên và chỉ thị `using`.

## Nhập Các Namespace

Mở dự án của bạn và chắc chắn rằng namespace Aspose.Imaging đã sẵn sàng:

```csharp
using Aspose.Imaging;
```

## Bước 1: Thiết Lập Môi Trường

Đầu tiên chúng ta tạo một canvas trống để chứa các bản vẽ.

```csharp
public static void Run()
{
    Console.WriteLine("Running example DrawingUsingGraphicsPath");
    string dataDir = "Your Document Directory";

    // Create an instance of BmpOptions and set its various properties
    BmpOptions ImageOptions = new BmpOptions();
    ImageOptions.BitsPerPixel = 24;

    // Create an instance of FileCreateSource and assign it to Source property
    ImageOptions.Source = new FileCreateSource(dataDir + "sample_1.bmp", false);

    // Create an instance of Image and initialize an instance of Graphics
    using (Image image = Image.Create(ImageOptions, 500, 500))
    {
        Graphics graphics = new Graphics(image);
        graphics.Clear(Color.White);
```

Ở đây chúng ta cấu hình một BMP kích thước 500 × 500 pixel với nền trắng, sẵn sàng cho việc vẽ.

## Bước 2: Tạo GraphicsPath, Thêm Hình Dạng và Văn Bản

Bây giờ chúng ta xây dựng một `GraphicsPath` chứa cả hình dạng **và văn bản chúng ta muốn vẽ lên ảnh**.

```csharp
        GraphicsPath graphicspath = new GraphicsPath();
        Figure figure = new Figure();

        figure.AddShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
        figure.AddShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
        figure.AddShape(new TextShape("Aspose.Imaging", new RectangleF(170, 225, 170, 100), new Font("Arial", 20), StringFormat.GenericTypographic));

        graphicspath.AddFigures(new[] { figure });
```

- **EllipseShape** và **RectangleShape** cho phép chúng ta **vẽ hình dạng lên ảnh**.  
- **TextShape** là nơi chúng ta **vẽ văn bản lên ảnh** – chuỗi “Aspose.Imaging” sẽ được render bên trong hình chữ nhật đã chỉ định.

## Bước 3: Vẽ Đường Path và Tô Đầy Bằng Mẫu Hatch

Khi path đã sẵn sàng, chúng ta vẽ viền bằng bút và sau đó tô đầy bên trong bằng một brush hatch — điều này minh họa **việc tô đầy hình dạng bằng mẫu**.

```csharp
        graphics.DrawPath(new Pen(Color.Blue), graphicspath);

        // Create an instance of HatchBrush and set its properties
        HatchBrush hatchbrush = new HatchBrush();
        hatchbrush.BackgroundColor = Color.Brown;
        hatchbrush.ForegroundColor = Color.Blue;
        hatchbrush.HatchStyle = HatchStyle.Vertical;

        graphics.FillPath(hatchbrush, graphicspath);

        image.Save();
        Console.WriteLine("Processing completed successfully.");
    }
    Console.WriteLine("Finished example DrawingUsingGraphicsPath");
}
```

`HatchBrush` vẽ một mẫu đường thẳng đứng màu xanh dương trên nền nâu, tạo nên vẻ ngoài đặc trưng cho các hình dạng.

## Các Trường Hợp Sử Dụng Thông Thường

| Kịch bản | Cách mã giúp |
|----------|--------------|
| **Tạo thẻ** | Kết hợp logo công ty (ellipse), viền (rectangle) và tên nhân viên (text) trong một ảnh. |
| **Biểu đồ động** | Vẽ các hình dạng dựa trên dữ liệu và chú thích chúng bằng giá trị sử dụng `TextShape`. |
| **Watermark** | Render văn bản bán trong suốt lên ảnh hiện có và tô nền bằng mẫu để thương hiệu nhẹ nhàng. |

## Khắc Phục Sự Cố & Mẹo

- **Đường dẫn file** – Đảm bảo `dataDir` trỏ tới thư mục có quyền ghi; nếu không `FileCreateSource` sẽ ném ngoại lệ.  
- **Độ tương phản màu** – Khi dùng các tô đầy có mẫu, chọn màu nền và màu nền trước sao cho đủ tương phản để đọc được.  
- **Hiệu năng** – Đối với ảnh lớn, cân nhắc sử dụng `RasterImage` thay vì `BmpOptions` để giảm tiêu thụ bộ nhớ.

## Câu Hỏi Thường Gặp

**H: Aspose.Imaging cho .: cập, . thể chuyển đổi ảnh đã vẽ sang định dạng khác (ví dụ PNG hoặc JPEG) không?**  
Đ: Chắc chắn. Sau khi lưu BMP, bạn có thể tải lại bằng `Image.Load` và gọi `Save` với phần mở rộng file khác.

**H: Tôi có thể tìm tài liệu chi tiết hơn ở đâu?**  
Đ: Tham khảo tài liệu chính thức tại [tài liệu Aspose.Imaging](https://reference.aspose.com/imaging/net/).

**H: Có phiên bản dùng thử miễn phí không?**  
Đ: Có, bạn có thể tải phiên bản dùng thử từ [đây](https://releases.aspose.com/).

**H: Làm thế nào để mua giấy phép cho môi trường production?**  
Đ: Giấy phép có thể mua trực tiếp từ cửa hàng Aspose: [liên kết này](https://purchase.aspose.com/buy).

## Kết Luận

Bạn đã học cách **vẽ văn bản lên ảnh**, **vẽ hình dạng lên ảnh**, và **tô đầy hình dạng bằng mẫu** bằng API `GraphicsPath` của Aspose.Imaging. Với những khối xây dựng này, bạn có thể tạo ra các đồ họa phong phú, lập trình cho báo cáo, bảng điều khiển, hoặc bất kỳ đầu ra hình ảnh tùy chỉnh nào trong ứng dụng .NET của mình.

Nếu gặp vấn đề hoặc muốn chia sẻ các sáng tạo, hãy tham gia cộng đồng tại [Diễn đàn Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Cập nhật lần cuối:** 2026-01-30  
**Đã kiểm tra với:** Aspose.Imaging 24.12 cho .NET  
**Tác giả:** Aspose