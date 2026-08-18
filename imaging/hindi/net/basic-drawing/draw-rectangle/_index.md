---
date: 2026-02-12
description: Aspose का उपयोग करके खाली इमेज बनाना और Aspose.Imaging के साथ .NET में
  आयत (rectangle) कैसे बनाएं – आपके .NET एप्लिकेशन्स में इमेज मैनिपुलेशन के लिए एक
  त्वरित गाइड।
linktitle: Draw Rectangle in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Aspose के साथ खाली छवि बनाएं – .NET में आयतें बनाएं
url: /hi/net/basic-drawing/draw-rectangle/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# ब्लैंक इमेज Aspose बनाएं – .NET में आयतें बनाएं

.NET अनुप्रयोगों में छवियों को बनाना और संशोधित करना कठिन लग सकता है, लेकिन Aspose.Imaging के साथ आप केवल कुछ पंक्तियों के कोड में **create blank image Aspose** बना सकते हैं और उस पर आकार बना सकते हैं। इस ट्यूटोरियल में हम पूरी प्रक्रिया — ब्लैंक कैनवास सेट करने से लेकर आयतें बनाने तक — को चरणबद्ध रूप से देखेंगे, ताकि आप तुरंत अपने .NET प्रोजेक्ट्स में ग्राफिक्स जोड़ना शुरू कर सकें।

## त्वरित उत्तर
- **“create blank image Aspose” का क्या मतलब है?** इसका अर्थ है Aspose.Imaging API का उपयोग करके एक खाली बिटमैप बनाना।  
- **Aspose के साथ .net में आयत कैसे बनाएं?** `Graphics` ऑब्जेक्ट को इनिशियलाइज़ करने के बाद `Graphics.DrawRectangle` मेथड का उपयोग करें।  
- **कौन सा NuGet पैकेज आवश्यक है?** `Aspose.Imaging` (नवीनतम संस्करण)।  
- **क्या मैं इमेज को PNG, JPEG, या BMP के रूप में सहेज सकता हूँ?** हाँ – केवल इमेज विकल्प बदलें (जैसे `BmpOptions`, `JpegOptions`)।  
- **क्या विकास के लिए लाइसेंस चाहिए?** मूल्यांकन के लिए फ्री ट्रायल काम करता है; उत्पादन के लिए एक कमर्शियल लाइसेंस आवश्यक है।

## “create blank image Aspose” क्या है?
ब्लैंक इमेज बनाना मतलब है एक पिक्सेल बफ़र को परिभाषित चौड़ाई, ऊँचाई और पिक्सेल फ़ॉर्मेट के साथ आवंटित करना। Aspose.Imaging लो‑लेवल विवरणों को संभालता है, जिससे आपको GDI+ या System.Drawing से निपटे बिना एक तैयार‑ड्रॉ कैनवास मिल जाता है।

## .NET में आयतें बनाने के लिए Aspose.Imaging क्यों उपयोग करें?
- **क्रॉस‑प्लेटफ़ॉर्म** – Windows, Linux, और macOS पर काम करता है।  
- **कोई नेटिव डिपेंडेंसी नहीं** – शुद्ध मैनेज्ड कोड, सर्वर वातावरण के लिए उपयुक्त।  
- **समृद्ध ड्रॉइंग API** – पेन, ब्रश, एंटी‑एलियासिंग और कई शैप टाइप्स को सपोर्ट करता है।  
- **उच्च प्रदर्शन** – बड़े इमेज और बैच प्रोसेसिंग के लिए ऑप्टिमाइज़्ड।

## पूर्वापेक्षाएँ

1. **Aspose.Imaging for .NET** – इसे [download page](https://releases.aspose.com/imaging/net/) से डाउनलोड करें।  
2. **डेवलपमेंट एनवायरनमेंट** – Visual Studio, VS Code, या कोई भी .NET‑संगत IDE।  
3. **.NET रनटाइम** – .NET 6+ या .NET Framework 4.7.2+।  

अब जब सभी चीज़ें सेट हो गई हैं, चलिए कोड में डुबकी लगाते हैं।

## .NET में blank image Aspose कैसे बनाएं?

### चरण 1: आवश्यक नेमस्पेसेस इम्पोर्ट करें

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

ये नेमस्पेसेस आपको कोर इमेजिंग क्लासेज़, ब्रश टाइप्स, और इमेज‑सेविंग विकल्पों तक पहुंच प्रदान करते हैं।

### चरण 2: एक ब्लैंक इमेज (कैनवास) बनाएं

```csharp
string dataDir = "Your Document Directory";  // Set the path to your document directory
using (FileStream stream = new FileStream(dataDir, FileMode.Create))
{
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;
    saveOptions.Source = new StreamSource(stream);

    using (Image image = Image.Create(saveOptions, 100, 100))
    {
        // Your drawing code will go here
        image.Save();
    }
}
```

इस ब्लॉक में हम:

* आउटपुट लोकेशन (`dataDir`) निर्धारित करते हैं।  
* `BmpOptions` को 32‑बिट पिक्सेल फ़ॉर्मेट उपयोग करने के लिए कॉन्फ़िगर करते हैं।  
* 100 × 100 पिक्सेल का **blank image** बनाते हैं।

### चरण 3: Aspose.Imaging के साथ .net में आयत कैसे बनाएं

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

* `Graphics.Clear` कैनवास को बैकग्राउंड रंग (इस उदाहरण में पीला) से भरता है।  
* `DrawRectangle` दो आयतें बनाता है—एक साधारण लाल पेन से, दूसरा नीले सॉलिड ब्रश से—दृश्य कंट्रास्ट के लिए।

### चरण 4: इमेज सहेजें

```csharp
image.Save();
```

`Save` को कॉल करने से पहले परिभाषित विकल्पों का उपयोग करके बिटमैप फ़ाइल सिस्टम में लिखा जाता है।

## सामान्य समस्याएँ और टिप्स

| समस्या | कारण | समाधान |
|-------|--------|-----|
| **ब्लैंक इमेज काली दिख रही है** | बैकग्राउंड साफ नहीं किया गया | ड्रॉ करने से पहले `graphic.Clear(Color.YourColor)` कॉल करें। |
| **फ़ाइल नहीं मिली अपवाद** | `dataDir` एक गैर‑मौजूद फ़ोल्डर की ओर इशारा करता है | सुनिश्चित करें कि डायरेक्टरी मौजूद है या `Environment.CurrentDirectory` के साथ `Path.Combine` का उपयोग करें। |
| **गलत रंग** | `Aspose.Imaging.Color` के बजाय `System.Drawing.Color` का उपयोग करना | हमेशा `Aspose.Imaging.Color` इम्पोर्ट करें। |
| **बड़ी इमेज पर प्रदर्शन में देरी** | उच्च बिट‑पर‑पिक्सेल के साथ डिफ़ॉल्ट `BmpOptions` का उपयोग करना | कम्प्रेशन के लिए `JpegOptions` या `PngOptions` में स्विच करें। |

## अक्सर पूछे जाने वाले प्रश्न (विस्तारित)

**प्रश्न: क्या मैं आयतों के अलावा अन्य आकार भी बना सकता हूँ?**  
**उत्तर:** बिल्कुल। Aspose.Imaging `DrawEllipse`, `DrawLine`, और `DrawPolygon` जैसी मेथड्स प्रदान करता है।

**प्रश्न: क्या लाइब्रेरी वाणिज्यिक उपयोग के लिए मुफ्त है?**  
**उत्तर:** नहीं, Aspose.Imaging एक कमर्शियल प्रोडक्ट है, लेकिन आप इसे एक फ्री ट्रायल के साथ [यहाँ](https://releases.aspose.com/) मूल्यांकन कर सकते हैं।

**प्रश्न: क्या यह Windows और वेब एप्लिकेशन दोनों पर काम करता है?**  
**उत्तर:** हाँ, वही कोड ASP.NET, Blazor, और कंसोल ऐप्स में चलता है।

**प्रश्न: आउटपुट फ़ॉर्मेट को PNG में कैसे बदलें?**  
**उत्तर:** `BmpOptions` को `PngOptions` से बदलें और फ़ाइल एक्सटेंशन को उसी अनुसार समायोजित करें।

**प्रश्न: अधिक विस्तृत दस्तावेज़ीकरण कहाँ मिल सकता है?**  
**उत्तर:** पूर्ण API रेफ़रेंस [यहाँ](https://reference.aspose.com/imaging/net/) प्राप्त करें और [Aspose.Imaging फ़ोरम](https://forum.aspose.com/) पर समुदाय से जुड़ें।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**अंतिम अपडेट:** 2026-02-12  
**परीक्षित संस्करण:** Aspose.Imaging 24.12 for .NET  
**लेखक:** Aspose