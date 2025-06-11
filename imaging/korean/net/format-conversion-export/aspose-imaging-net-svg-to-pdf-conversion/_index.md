---
"date": "2025-06-03"
"description": "Aspose.Imaging .NET을 사용하여 글꼴 품질을 유지하면서 SVG를 PDF로 변환하는 방법을 익혀보세요. 디렉터리 설정, 글꼴 임베드 등에 대해서도 알아보세요."
"title": "Aspose.Imaging .NET의 글꼴 관리 및 기술을 사용한 효율적인 SVG-PDF 변환"
"url": "/ko/net/format-conversion-export/aspose-imaging-net-svg-to-pdf-conversion/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Aspose.Imaging .NET을 사용한 효율적인 SVG-PDF 변환

## 소개

벡터 그래픽을 PDF와 같은 다재다능한 형식으로 변환하는 것은 오늘날 디지털 시대에 문서 공유 및 인쇄에 매우 중요합니다. 이러한 변환 과정에서 글꼴 무결성을 유지하는 것은 어려울 수 있습니다. 이 튜토리얼에서는 Aspose.Imaging for .NET을 사용하여 글꼴 품질을 유지하면서 SVG를 PDF로 원활하게 변환하는 방법을 보여줍니다.

**배울 내용:**
- 디렉토리를 설정하고 SVG 파일을 PDF로 내보냅니다.
- SVG 파일 내에 글꼴을 포함하거나 내보내는 기술.
- 저장 프로세스 동안 SVG 글꼴을 관리하기 위한 사용자 정의 콜백 핸들러를 구현합니다.

이러한 기술을 활용하면 다양한 플랫폼에서 문서가 전문적이고 일관성 있게 보이도록 할 수 있습니다. 자, 이제 환경 설정부터 시작해 볼까요!

## 필수 조건

코드를 살펴보기 전에 다음 사항이 있는지 확인하세요.

### 필수 라이브러리
- **.NET용 Aspose.Imaging**: 이미지 변환을 처리하는 데 필수적입니다.
- **System.IO 네임스페이스**: 파일 및 디렉토리 작업에 사용됩니다.

### 환경 설정
Visual Studio 또는 .NET 프로젝트를 지원하는 IDE와 같은 호환 가능한 개발 환경을 갖추고 있는지 확인하세요. 기본적인 C# 프로그래밍에 대한 지식이 있으면 더욱 좋습니다.

## .NET용 Aspose.Imaging 설정

프로젝트에서 Aspose.Imaging을 사용하려면 다음 설치 단계를 따르세요.

**.NET CLI 사용:**
```bash
dotnet add package Aspose.Imaging
```

**패키지 관리자 사용:**
```powershell
Install-Package Aspose.Imaging
```

**NuGet 패키지 관리자 UI를 통해:**
"Aspose.Imaging"을 검색하여 최신 버전을 설치하세요.

### 라이센스 취득
- **무료 체험**: 무료 체험판을 통해 기능을 테스트해 보세요.
- **임시 면허**: 장기 평가를 위해 임시 라이센스를 얻으세요.
- **구입**: Aspose.Imaging이 귀하의 요구 사항을 충족하는 경우 구매를 고려해 보세요.

#### 초기화 및 설정
Aspose.Imaging을 사용하려면 프로젝트에 종속성으로 추가하세요. 기본 설정은 다음과 같습니다.

```csharp
using Aspose.Imaging;
```

확인하십시오 `Aspose.Imaging` 네임스페이스는 파일 맨 위에 포함되어 클래스와 메서드에 액세스할 수 있습니다.

## 구현 가이드

이 섹션에서는 각 기능을 관리 가능한 단계로 나누어 설명합니다.

### 디렉토리 설정 및 SVG를 PDF로 내보내기

#### 개요
디렉토리 경로가 출력을 위해 올바르게 설정되었는지 확인하면서 SVG 파일을 PDF로 변환합니다.

**1단계: 출력 디렉토리가 있는지 확인**
```csharp
string SourceFolder = "YOUR_DOCUMENT_DIRECTORY";
string OutFolderName = "Out";
string OutFolder = Path.Combine(SourceFolder, OutFolderName);

if (!Directory.Exists(OutFolder))
{
    Directory.CreateDirectory(OutFolder);
}
```
*설명*: 이 코드 조각은 출력 디렉토리가 존재하는지 확인하고 필요한 경우 생성합니다.

**2단계: SVG를 로드하고 PDF로 내보내기**
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
*설명*: 그 `PdfOptions` SVG 콘텐츠의 래스터화를 구성하여 페이지 크기가 원본 이미지 크기와 일치하도록 할 수 있습니다.

### 글꼴 임베딩 옵션을 사용한 SVG 저장

#### 개요
글꼴 충실도를 유지하기 위해 글꼴 내장 설정을 제어하면서 SVG 파일을 저장합니다.

**1단계: 출력 및 글꼴 디렉토리 정의**
```csharp
string FontFolderName = "fonts";
string FontFolder = Path.Combine(OutFolder, FontFolderName);

if (!Directory.Exists(FontFolder))
{
    Directory.CreateDirectory(FontFolder);
}
```
*설명*: 파일을 저장하기 전에 디렉토리가 설정되어 있는지 확인하세요.

**2단계: 사용자 정의 글꼴 옵션으로 SVG 저장**
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
*설명*: 이 방법을 사용하면 글꼴을 포함할지 스트리밍할지 지정할 수 있으며, 이는 글꼴의 저장 및 액세스 방식에 영향을 미칩니다.

### 사용자 정의 SVG 글꼴 콜백 핸들러

#### 개요
SVG 저장 중에 글꼴 리소스를 관리하기 위한 사용자 정의 핸들러를 구현합니다.

**1단계: SvgCallbackFontTest 클래스 구현**
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
*설명*: 이 클래스는 글꼴 리소스를 직접 포함할지 아니면 별도로 저장할지 결정하여 처리합니다. SVG 내보내기 과정에서 글꼴이 올바르게 참조되고 저장되도록 합니다.

## 실제 응용 프로그램

1. **자동 보고서 생성**: Aspose.Imaging을 사용하여 디자인 초안을 PDF로 변환하여 일관된 배포가 가능합니다.
2. **디지털 출판**SVG에서 PDF로 그래픽이 내장된 문서를 변환할 때 고품질 글꼴 렌더링을 보장합니다.
3. **크로스 플랫폼 문서 공유**: 서로 다른 운영 체제 간에 공유되는 문서의 시각적 무결성을 유지합니다.

## 성능 고려 사항

### 성능 최적화를 위한 팁
- 사용 후 스트림을 즉시 폐기하는 등 효율적인 파일 처리 방식을 사용합니다.
- 처리가 완료되면 사용되지 않는 객체와 디렉터리를 지워 메모리 사용량을 최소화합니다.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}