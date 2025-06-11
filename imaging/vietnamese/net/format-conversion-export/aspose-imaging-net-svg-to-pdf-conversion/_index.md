---
"date": "2025-06-03"
"description": "Làm chủ việc chuyển đổi SVG sang PDF với Aspose.Imaging .NET trong khi vẫn giữ nguyên chất lượng phông chữ. Tìm hiểu cách thiết lập thư mục, nhúng phông chữ và nhiều hơn nữa."
"title": "Chuyển đổi SVG sang PDF hiệu quả bằng cách sử dụng Aspose.Imaging .NET&#58; Quản lý phông chữ và kỹ thuật"
"url": "/vi/net/format-conversion-export/aspose-imaging-net-svg-to-pdf-conversion/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Chuyển đổi SVG sang PDF hiệu quả bằng Aspose.Imaging .NET

## Giới thiệu

Chuyển đổi đồ họa vector sang các định dạng đa năng như PDF là rất quan trọng để chia sẻ và in tài liệu trong thời đại kỹ thuật số ngày nay. Duy trì tính toàn vẹn của phông chữ trong quá trình chuyển đổi này có thể là một thách thức. Hướng dẫn này trình bày cách chuyển đổi SVG sang PDF liền mạch trong khi vẫn giữ nguyên chất lượng phông chữ bằng Aspose.Imaging cho .NET.

**Những gì bạn sẽ học được:**
- Thiết lập thư mục và xuất tệp SVG dưới dạng PDF.
- Các kỹ thuật nhúng hoặc xuất phông chữ trong tệp SVG.
- Triển khai trình xử lý gọi lại tùy chỉnh để quản lý phông chữ SVG trong quá trình lưu.

Với những kỹ năng này, bạn có thể đảm bảo tài liệu của mình trông chuyên nghiệp và nhất quán trên nhiều nền tảng khác nhau. Hãy bắt đầu bằng cách thiết lập môi trường của chúng ta!

## Điều kiện tiên quyết

Trước khi tìm hiểu mã, hãy đảm bảo bạn có những điều sau:

### Thư viện bắt buộc
- **Aspose.Imaging cho .NET**: Cần thiết để xử lý chuyển đổi hình ảnh.
- **Không gian tên System.IO**: Dành cho các thao tác liên quan đến tập tin và thư mục.

### Thiết lập môi trường
Đảm bảo bạn có môi trường phát triển tương thích như Visual Studio hoặc bất kỳ IDE nào hỗ trợ các dự án .NET. Sự quen thuộc với lập trình C# cơ bản là có lợi.

## Thiết lập Aspose.Imaging cho .NET

Để sử dụng Aspose.Imaging trong dự án của bạn, hãy làm theo các bước cài đặt sau:

**Sử dụng .NET CLI:**
```bash
dotnet add package Aspose.Imaging
```

**Sử dụng Trình quản lý gói:**
```powershell
Install-Package Aspose.Imaging
```

**Thông qua Giao diện người dùng của Trình quản lý gói NuGet:**
Tìm kiếm "Aspose.Imaging" và cài đặt phiên bản mới nhất.

### Mua lại giấy phép
- **Dùng thử miễn phí**:Bắt đầu bằng bản dùng thử miễn phí để kiểm tra các tính năng.
- **Giấy phép tạm thời**: Xin giấy phép tạm thời để đánh giá mở rộng.
- **Mua**: Hãy cân nhắc mua nếu Aspose.Imaging đáp ứng được nhu cầu của bạn.

#### Khởi tạo và thiết lập
Để sử dụng Aspose.Imaging, hãy thêm nó như một phần phụ thuộc vào dự án của bạn. Sau đây là thiết lập cơ bản:

```csharp
using Aspose.Imaging;
```

Đảm bảo `Aspose.Imaging` không gian tên được bao gồm ở đầu tệp của bạn để truy cập các lớp và phương thức của tệp đó.

## Hướng dẫn thực hiện

Phần này chia nhỏ từng tính năng thành các bước dễ quản lý.

### Thiết lập thư mục và xuất SVG sang PDF

#### Tổng quan
Chuyển đổi tệp SVG thành PDF trong khi đảm bảo đường dẫn thư mục được thiết lập chính xác để xuất ra.

**Bước 1: Đảm bảo thư mục đầu ra tồn tại**
```csharp
string SourceFolder = "YOUR_DOCUMENT_DIRECTORY";
string OutFolderName = "Out";
string OutFolder = Path.Combine(SourceFolder, OutFolderName);

if (!Directory.Exists(OutFolder))
{
    Directory.CreateDirectory(OutFolder);
}
```
*Giải thích*:Đoạn mã này kiểm tra xem thư mục đầu ra có tồn tại hay không và tạo thư mục đó nếu cần.

**Bước 2: Tải SVG và Xuất sang PDF**
```csharp
public void ReadAndExportToPdf(string inputFileName)
{
    string inputFile = Path.Combine(SourceFolder, inputFileName);
    string outFile = Path.Combine(OutFolder, inputFileName + ".pdf");
    
    using (Image image = Image.Load(inputFile))
    {
        image.Save(outFile,
            new PdfOptions { VectorRasterizationOptions = new SvgRasterizationOptions { PageSize = image.Size } });
    }
}
```
*Giải thích*: Các `PdfOptions` cho phép cấu hình quá trình quét nội dung SVG, đảm bảo kích thước trang khớp với kích thước hình ảnh gốc.

### Lưu SVG với Tùy chọn nhúng phông chữ

#### Tổng quan
Lưu tệp SVG trong khi kiểm soát cài đặt nhúng phông chữ để duy trì độ trung thực của phông chữ.

**Bước 1: Xác định thư mục đầu ra và phông chữ**
```csharp
string FontFolderName = "fonts";
string FontFolder = Path.Combine(OutFolder, FontFolderName);

if (!Directory.Exists(FontFolder))
{
    Directory.CreateDirectory(FontFolder);
}
```
*Giải thích*: Đảm bảo các thư mục được thiết lập trước khi lưu tệp.

**Bước 2: Lưu SVG với Tùy chọn Phông chữ Tùy chỉnh**
```csharp
public void Save(bool useEmbedded, string fileName, int expectedCountFonts)
{
    string fontStoreType = useEmbedded ? "Embedded" : "Stream";
    string inputFile = Path.Combine(SourceFolder, fileName);
    string outFileName = $"{Path.GetFileNameWithoutExtension(fileName)}_{fontStoreType}.svg";
    string outputFile = Path.Combine(OutFolder, outFileName);

    using (Image image = Image.Load(inputFile))
    {
        EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions
        {
            BackgroundColor = Color.White,
            PageWidth = image.Width,
            PageHeight = image.Height
        };

        string testingFileName = Path.GetFileNameWithoutExtension(inputFile);
        string fontFolder = Path.Combine(FontFolder, testingFileName);

        image.Save(outputFile,
            new SvgOptions
            {
                VectorRasterizationOptions = emfRasterizationOptions,
                Callback = new SvgCallbackFontTest(useEmbedded, fontFolder)
                {
                    Link = FontFolderName + "/" + testingFileName
                }
            });
    }

    if (!useEmbedded)
    {
        string[] files = Directory.GetFiles(fontFolder);
        if (files.Length != expectedCountFonts)
        {
            throw new Exception($"Expected count font files = {expectedCountFonts}, Current count font files = {files.Length}");
        }
    }
}
```
*Giải thích*:Phương pháp này cho phép bạn chỉ định phông chữ sẽ được nhúng hay phát trực tuyến, ảnh hưởng đến cách chúng được lưu trữ và truy cập.

### Trình xử lý gọi lại phông chữ SVG tùy chỉnh

#### Tổng quan
Triển khai trình xử lý tùy chỉnh để quản lý tài nguyên phông chữ trong quá trình lưu SVG.

**Bước 1: Triển khai lớp SvgCallbackFontTest**
```csharp
public class SvgCallbackFontTest : SvgResourceKeeperCallback
{
    private readonly string outFolder;
    private readonly bool useEmbeddedFont;
    private int fontCounter = 0;

    public string Link { get; set; }

    public SvgCallbackFontTest(bool useEmbeddedFont, string outFolder)
    {
        this.useEmbeddedFont = useEmbeddedFont;
        this.outFolder = outFolder;
        
        if (Directory.Exists(outFolder))
        {
            Directory.Delete(this.outFolder, true);
        }
    }

    public override void OnFontResourceReady(FontStoringArgs args)
    {
        if (this.useEmbeddedFont)
        {
            args.FontStoreType = FontStoreType.Embedded;
        }
        else
        {
            args.FontStoreType = FontStoreType.Stream;
            string fontFolder = this.outFolder;

            if (!Directory.Exists(fontFolder))
            {
                Directory.CreateDirectory(fontFolder);
            }

            string fName = args.SourceFontFileName;
            if (!File.Exists(fName))
            {
                fName = $"font_{this.fontCounter++}.ttf";
            }

            string fileName = Path.Combine(fontFolder, Path.GetFileName(fName));
            
            args.DestFontStream = new FileStream(fileName, FileMode.OpenOrCreate);
            args.DisposeStream = true;
            args.FontFileUri = $".{this.Link}/{Path.GetFileName(fName)}";
        }
    }
}
```
*Giải thích*: Lớp này xử lý các tài nguyên phông chữ bằng cách quyết định nhúng chúng trực tiếp hay lưu trữ chúng riêng biệt. Nó đảm bảo rằng phông chữ được tham chiếu và lưu chính xác trong quá trình xuất SVG.

## Ứng dụng thực tế

1. **Tạo báo cáo tự động**: Sử dụng Aspose.Imaging để chuyển đổi bản thảo thiết kế thành PDF để phân phối thống nhất.
2. **Xuất bản kỹ thuật số**Đảm bảo hiển thị phông chữ chất lượng cao khi chuyển đổi các bài viết có đồ họa nhúng từ SVG sang PDF.
3. **Chia sẻ tài liệu đa nền tảng**: Duy trì tính toàn vẹn trực quan của các tài liệu được chia sẻ giữa các hệ điều hành khác nhau.

## Cân nhắc về hiệu suất

### Mẹo để tối ưu hóa hiệu suất
- Sử dụng các biện pháp xử lý tệp hiệu quả, chẳng hạn như xóa luồng ngay sau khi sử dụng.
- Giảm thiểu việc sử dụng bộ nhớ bằng cách xóa các đối tượng và thư mục không sử dụng sau khi xử lý hoàn tất.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}