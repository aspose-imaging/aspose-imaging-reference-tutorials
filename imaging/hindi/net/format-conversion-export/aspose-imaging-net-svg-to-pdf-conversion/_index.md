---
"date": "2025-06-03"
"description": "Aspose.Imaging .NET के साथ SVG को PDF में बदलने में महारत हासिल करें और फ़ॉन्ट की गुणवत्ता बनाए रखें। डायरेक्टरी सेटअप, फ़ॉन्ट एम्बेड करना और बहुत कुछ सीखें।"
"title": "Aspose.Imaging .NET के फ़ॉन्ट प्रबंधन और तकनीकों का उपयोग करके कुशल SVG से PDF रूपांतरण"
"url": "/hi/net/format-conversion-export/aspose-imaging-net-svg-to-pdf-conversion/"
"weight": 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Aspose.Imaging .NET का उपयोग करके SVG से PDF में कुशल रूपांतरण

## परिचय

आज के डिजिटल युग में दस्तावेज़ साझा करने और मुद्रण के लिए वेक्टर ग्राफ़िक्स को PDF जैसे बहुमुखी प्रारूपों में परिवर्तित करना महत्वपूर्ण है। इस रूपांतरण के दौरान फ़ॉन्ट अखंडता बनाए रखना चुनौतीपूर्ण हो सकता है। यह ट्यूटोरियल Aspose.Imaging for .NET का उपयोग करके फ़ॉन्ट गुणवत्ता को संरक्षित करते हुए सहज SVG से PDF रूपांतरण प्रदर्शित करता है।

**आप क्या सीखेंगे:**
- निर्देशिकाएँ स्थापित करना और SVG फ़ाइलों को PDF के रूप में निर्यात करना।
- एसवीजी फाइलों में फ़ॉन्ट एम्बेड करने या निर्यात करने की तकनीकें।
- सेविंग प्रक्रिया के दौरान SVG फ़ॉन्ट्स को प्रबंधित करने के लिए एक कस्टम कॉलबैक हैंडलर को कार्यान्वित करना।

इन कौशलों के साथ, आप यह सुनिश्चित कर सकते हैं कि आपके दस्तावेज़ विभिन्न प्लेटफ़ॉर्म पर पेशेवर और सुसंगत दिखें। आइए अपना वातावरण सेट करके शुरू करें!

## आवश्यक शर्तें

कोड में आगे बढ़ने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

### आवश्यक पुस्तकालय
- **.NET के लिए Aspose.Imaging**: छवि रूपांतरण को संभालने के लिए आवश्यक.
- **सिस्टम.IO नामस्थान**: फ़ाइल और निर्देशिका संचालन के लिए.

### पर्यावरण सेटअप
सुनिश्चित करें कि आपके पास Visual Studio या .NET प्रोजेक्ट को सपोर्ट करने वाला कोई IDE जैसा संगत विकास वातावरण है। बुनियादी C# प्रोग्रामिंग से परिचित होना फ़ायदेमंद है।

## .NET के लिए Aspose.Imaging सेट अप करना

अपने प्रोजेक्ट में Aspose.Imaging का उपयोग करने के लिए, इन स्थापना चरणों का पालन करें:

**.NET CLI का उपयोग करना:**
```bash
dotnet add package Aspose.Imaging
```

**पैकेज मैनेजर का उपयोग करना:**
```powershell
Install-Package Aspose.Imaging
```

**NuGet पैकेज मैनेजर UI के माध्यम से:**
"Aspose.Imaging" खोजें और नवीनतम संस्करण स्थापित करें।

### लाइसेंस अधिग्रहण
- **मुफ्त परीक्षण**: सुविधाओं का परीक्षण करने के लिए निःशुल्क परीक्षण से शुरुआत करें।
- **अस्थायी लाइसेंस**विस्तारित मूल्यांकन के लिए अस्थायी लाइसेंस प्राप्त करें।
- **खरीदना**यदि Aspose.Imaging आपकी आवश्यकताओं को पूरा करता है तो खरीदने पर विचार करें।

#### आरंभीकरण और सेटअप
Aspose.Imaging का उपयोग करने के लिए, इसे अपने प्रोजेक्ट में निर्भरता के रूप में जोड़ें। यहाँ एक बुनियादी सेटअप है:

```csharp
using Aspose.Imaging;
```

सुनिश्चित करें `Aspose.Imaging` नेमस्पेस आपकी फ़ाइल के शीर्ष पर शामिल है ताकि आप इसकी कक्षाओं और विधियों तक पहुँच सकें।

## कार्यान्वयन मार्गदर्शिका

यह अनुभाग प्रत्येक सुविधा को प्रबंधनीय चरणों में विभाजित करता है।

### निर्देशिका सेटअप और SVG को PDF में निर्यात करें

#### अवलोकन
एक SVG फ़ाइल को PDF में परिवर्तित करें, साथ ही यह सुनिश्चित करें कि आउटपुट के लिए निर्देशिका पथ सही ढंग से सेट किए गए हैं।

**चरण 1: सुनिश्चित करें कि आउटपुट निर्देशिका मौजूद है**
```csharp
string SourceFolder = "YOUR_DOCUMENT_DIRECTORY";
string OutFolderName = "Out";
string OutFolder = Path.Combine(SourceFolder, OutFolderName);

if (!Directory.Exists(OutFolder))
{
    Directory.CreateDirectory(OutFolder);
}
```
*स्पष्टीकरण*: यह कोड स्निपेट जाँचता है कि आउटपुट डायरेक्टरी मौजूद है या नहीं और यदि आवश्यक हो तो उसे बनाता है।

**चरण 2: SVG लोड करें और PDF में निर्यात करें**
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
*स्पष्टीकरण*: द `PdfOptions` एसवीजी सामग्री के रास्टराइजेशन को कॉन्फ़िगर करने की अनुमति देता है, यह सुनिश्चित करता है कि पृष्ठ का आकार मूल छवि आयामों से मेल खाता है।

### फ़ॉन्ट एम्बेडिंग विकल्पों के साथ SVG सेव करना

#### अवलोकन
फ़ॉन्ट की विश्वसनीयता बनाए रखने के लिए फ़ॉन्ट एम्बेडिंग सेटिंग्स को नियंत्रित करते हुए SVG फ़ाइल सहेजें।

**चरण 1: आउटपुट और फ़ॉन्ट निर्देशिकाएँ परिभाषित करें**
```csharp
string FontFolderName = "fonts";
string FontFolder = Path.Combine(OutFolder, FontFolderName);

if (!Directory.Exists(FontFolder))
{
    Directory.CreateDirectory(FontFolder);
}
```
*स्पष्टीकरण*: सुनिश्चित करें कि फ़ाइलें सहेजने से पहले निर्देशिकाएँ सेट की गई हैं।

**चरण 2: कस्टम फ़ॉन्ट विकल्पों के साथ SVG सहेजें**
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
*स्पष्टीकरण*यह विधि आपको यह निर्दिष्ट करने की अनुमति देती है कि फ़ॉन्ट को एम्बेड किया जाना चाहिए या स्ट्रीम किया जाना चाहिए, जिससे यह प्रभावित होता है कि उन्हें कैसे संग्रहीत और एक्सेस किया जाता है।

### कस्टम SVG फ़ॉन्ट कॉलबैक हैंडलर

#### अवलोकन
SVG सेव करने के दौरान फ़ॉन्ट संसाधनों को प्रबंधित करने के लिए एक कस्टम हैंडलर लागू करें।

**चरण 1: SvgCallbackFontTest क्लास को लागू करें**
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
*स्पष्टीकरण*: यह क्लास फ़ॉन्ट संसाधनों को संभालता है और यह तय करता है कि उन्हें सीधे एम्बेड किया जाए या अलग से संग्रहीत किया जाए। यह सुनिश्चित करता है कि SVG निर्यात प्रक्रिया के दौरान फ़ॉन्ट को सही तरीके से संदर्भित और सहेजा जाए।

## व्यावहारिक अनुप्रयोगों

1. **स्वचालित रिपोर्ट निर्माण**: सुसंगत वितरण के लिए डिज़ाइन ड्राफ्ट को PDF में परिवर्तित करने के लिए Aspose.Imaging का उपयोग करें।
2. **डिजिटल प्रकाशन**एम्बेडेड ग्राफिक्स वाले लेखों को SVG से PDF में परिवर्तित करते समय उच्च-गुणवत्ता वाले फ़ॉन्ट रेंडरिंग को सुनिश्चित करें।
3. **क्रॉस-प्लेटफ़ॉर्म दस्तावेज़ साझाकरण**: विभिन्न ऑपरेटिंग सिस्टम के बीच साझा किए गए दस्तावेज़ों की दृश्य अखंडता बनाए रखें।

## प्रदर्शन संबंधी विचार

### प्रदर्शन को अनुकूलित करने के लिए सुझाव
- कुशल फ़ाइल प्रबंधन पद्धतियों का उपयोग करें, जैसे उपयोग के बाद स्ट्रीम्स का तुरंत निपटान करना।
- प्रसंस्करण पूर्ण होने के बाद अप्रयुक्त ऑब्जेक्ट्स और निर्देशिकाओं को साफ़ करके मेमोरी उपयोग को न्यूनतम करें।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}