---
"description": "Aspose.Imaging for .NET का उपयोग करके SVG पर रास्टर छवियाँ बनाना सीखें। गतिशील छवियों के साथ अपने .NET अनुप्रयोगों को बेहतर बनाएँ।"
"linktitle": ".NET के लिए Aspose.Imaging में SVG पर रास्टर छवि बनाएं"
"second_title": "Aspose.Imaging .NET इमेज प्रोसेसिंग API"
"title": ".NET के लिए Aspose.Imaging में SVG पर रास्टर छवि कैसे बनाएं"
"url": "/hi/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.Imaging में SVG पर रास्टर छवि कैसे बनाएं


.NET प्रोग्रामिंग की दुनिया में, Aspose.Imaging विभिन्न छवि-संबंधी कार्यों को संभालने के लिए एक विश्वसनीय और बहुमुखी लाइब्रेरी के रूप में खड़ा है। यह जो एक आकर्षक क्षमता प्रदान करता है वह है SVG कैनवास पर रास्टर छवि बनाने की क्षमता। इस चरण-दर-चरण मार्गदर्शिका में, हम आपको .NET के लिए Aspose.Imaging का उपयोग करके SVG पर रास्टर छवि बनाने की प्रक्रिया से परिचित कराएँगे।

## आवश्यक शर्तें

इससे पहले कि हम विस्तार से बताएं, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- Aspose.Imaging for .NET: आपके पास लाइब्रेरी इंस्टॉल होनी चाहिए। यदि नहीं, तो आप इसे यहाँ से डाउनलोड कर सकते हैं [Aspose.Imaging for .NET डाउनलोड पृष्ठ](https://releases.aspose.com/imaging/net/).

- आपकी दस्तावेज़ निर्देशिका: प्रतिस्थापित करें `"Your Document Directory"` आपकी कार्यशील निर्देशिका के वास्तविक पथ के साथ.

अब, आइए इस प्रक्रिया को आसान चरणों में विभाजित करें:

## चरण 1: आवश्यक नामस्थान आयात करें

Aspose.Imaging के साथ काम करने के लिए आपको आवश्यक नामस्थानों को आयात करना होगा:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## चरण 2: छवियाँ लोड करें

- सबसे पहले, उस रास्टर छवि को लोड करें जिसे आप SVG कैनवास पर बनाना चाहते हैं।

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- इसके बाद, SVG कैनवास छवि को उस स्थान पर लोड करें जहां आप रास्टर छवि बनाना चाहते हैं।

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## चरण 3: SVG छवि पर चित्र बनाना

अब, आप मौजूदा SVG इमेज पर ड्राइंग शुरू कर सकते हैं। ऐसा करने के लिए, आपको इसका एक इंस्टेंस बनाना होगा। `SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## चरण 4: रास्टर छवि बनाएं

- वह सीमा निर्धारित करें जहां आप रास्टर छवि बनाना चाहते हैं और रास्टर छवि से स्रोत क्षेत्र निर्दिष्ट करें।

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## चरण 5: परिणाम सहेजें

SVG कैनवास पर रेखापुंज छवि बनाने के बाद, आप परिणामी छवि को सहेज सकते हैं:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.Imaging का उपयोग करके SVG कैनवास पर सफलतापूर्वक एक रास्टर छवि बनाई है। यह आपके .NET अनुप्रयोगों के भीतर समृद्ध और गतिशील छवियां बनाने के लिए अविश्वसनीय रूप से उपयोगी हो सकता है।

अधिक जानकारी और विस्तृत दस्तावेज़ीकरण के लिए, कृपया देखें [Aspose.Imaging for .NET दस्तावेज़](https://reference.aspose.com/imaging/net/).

## अक्सर पूछे जाने वाले प्रश्नों

### .NET के लिए Aspose.Imaging क्या है?
   Aspose.Imaging for .NET एक शक्तिशाली इमेज प्रोसेसिंग लाइब्रेरी है जो डेवलपर्स को .NET अनुप्रयोगों के भीतर विभिन्न प्रारूपों में छवियों को बनाने, हेरफेर करने और परिवर्तित करने की अनुमति देती है।

### क्या मैं व्यावसायिक परियोजनाओं में Aspose.Imaging for .NET का उपयोग कर सकता हूँ?
   हां, आप वाणिज्यिक और गैर-वाणिज्यिक दोनों परियोजनाओं में .NET के लिए Aspose.Imaging का उपयोग कर सकते हैं। लाइसेंसिंग विवरण यहां पाया जा सकता है [खरीद पृष्ठ](https://purchase.aspose.com/buy).

### क्या कोई निःशुल्क परीक्षण उपलब्ध है?
   हां, आप यहां से Aspose.Imaging for .NET का निःशुल्क परीक्षण प्राप्त कर सकते हैं [यहाँ](https://releases.aspose.com/).

### मैं सहायता कहां प्राप्त कर सकता हूं या प्रश्न कहां पूछ सकता हूं?
   यदि आपके कोई प्रश्न हों या आपको सहायता की आवश्यकता हो, तो आप यहां जा सकते हैं [Aspose.Imaging फ़ोरम](https://forum.aspose.com/).

### मैं Aspose.Imaging for .NET के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?
   आप यहां से अस्थायी लाइसेंस प्राप्त कर सकते हैं [यहाँ](https://purchase.aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}