---
title: .NET के लिए Aspose.Imaging में SVG पर रैस्टर इमेज कैसे बनाएं
linktitle: .NET के लिए Aspose.Imaging में SVG पर रैस्टर छवि बनाएं
second_title: Aspose.Imaging .NET इमेज प्रोसेसिंग एपीआई
description: .NET के लिए Aspose.Imaging का उपयोग करके SVG पर रेखापुंज चित्र बनाना सीखें। गतिशील छवियों के साथ अपने .NET अनुप्रयोगों को बेहतर बनाएं।
type: docs
weight: 11
url: /hi/net/vector-image-processing/draw-raster-image-on-svg/
---

.NET प्रोग्रामिंग की दुनिया में, Aspose.Imaging विभिन्न छवि-संबंधी कार्यों को संभालने के लिए एक विश्वसनीय और बहुमुखी लाइब्रेरी के रूप में खड़ा है। इसकी एक आकर्षक क्षमता एसवीजी कैनवास पर रेखापुंज छवि बनाने की क्षमता है। इस चरण-दर-चरण मार्गदर्शिका में, हम आपको .NET के लिए Aspose.Imaging का उपयोग करके SVG पर एक रेखापुंज छवि बनाने की प्रक्रिया के बारे में बताएंगे।

## आवश्यक शर्तें

इससे पहले कि हम विवरण में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

-  .NET के लिए Aspose.Imaging: आपके पास लाइब्रेरी स्थापित होनी चाहिए। यदि नहीं, तो आप इसे यहां से डाउनलोड कर सकते हैं[.NET डाउनलोड पेज के लिए Aspose.Imaging](https://releases.aspose.com/imaging/net/).

-  आपकी दस्तावेज़ निर्देशिका: बदलें`"Your Document Directory"` आपकी कार्यशील निर्देशिका के वास्तविक पथ के साथ।

अब, आइए इस प्रक्रिया को पालन करने में आसान चरणों में विभाजित करें:

## चरण 1: आवश्यक नामस्थान आयात करें

Aspose.Imaging के साथ काम करने के लिए आपको आवश्यक नामस्थान आयात करने की आवश्यकता है:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## चरण 2: छवियाँ लोड करें

- सबसे पहले, उस रेखापुंज छवि को लोड करें जिसे आप एसवीजी कैनवास पर बनाना चाहते हैं।

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- इसके बाद, एसवीजी कैनवास छवि को लोड करें जहां आप रेखापुंज छवि बनाना चाहते हैं।

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## चरण 3: एसवीजी छवि पर चित्रण

अब, आप मौजूदा एसवीजी छवि पर चित्र बनाना शुरू कर सकते हैं। ऐसा करने के लिए, आपको इसका एक उदाहरण बनाना होगा`SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## चरण 4: रेखापुंज छवि बनाएं

- उन सीमाओं को परिभाषित करें जहां आप रेखापुंज छवि बनाना चाहते हैं और रेखापुंज छवि से स्रोत क्षेत्र निर्दिष्ट करें।

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## चरण 5: परिणाम सहेजें

एसवीजी कैनवास पर रेखापुंज छवि खींचने के बाद, आप परिणामी छवि को सहेज सकते हैं:

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## निष्कर्ष

बधाई हो! आपने .NET के लिए Aspose.Imaging का उपयोग करके SVG कैनवास पर सफलतापूर्वक एक रेखापुंज छवि खींची है। यह आपके .NET अनुप्रयोगों में समृद्ध और गतिशील छवियां बनाने के लिए अविश्वसनीय रूप से उपयोगी हो सकता है।

 अधिक जानकारी और विस्तृत दस्तावेज़ीकरण के लिए, पर जाएँ[.NET दस्तावेज़ीकरण के लिए Aspose.Imaging](https://reference.aspose.com/imaging/net/).

## अक्सर पूछे जाने वाले प्रश्नों

### .NET के लिए Aspose.Imaging क्या है?
   .NET के लिए Aspose.Imaging एक शक्तिशाली इमेज प्रोसेसिंग लाइब्रेरी है जो डेवलपर्स को .NET अनुप्रयोगों के भीतर विभिन्न प्रारूपों में छवियां बनाने, हेरफेर करने और परिवर्तित करने की अनुमति देती है।

### क्या मैं व्यावसायिक परियोजनाओं में .NET के लिए Aspose.Imaging का उपयोग कर सकता हूँ?
    हां, आप वाणिज्यिक और गैर-व्यावसायिक दोनों परियोजनाओं में .NET के लिए Aspose.Imaging का उपयोग कर सकते हैं। लाइसेंसिंग विवरण यहां पाया जा सकता है[खरीद पृष्ठ](https://purchase.aspose.com/buy).

### क्या कोई निःशुल्क परीक्षण उपलब्ध है?
    हाँ, आप .NET के लिए Aspose.Imaging का निःशुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).

### मुझे समर्थन कहां मिल सकता है या प्रश्न कहां से पूछे जा सकते हैं?
    यदि आपके कोई प्रश्न हैं या सहायता की आवश्यकता है, तो आप यहां जा सकते हैं[Aspose.इमेजिंग फोरम](https://forum.aspose.com/).

### मैं .NET के लिए Aspose.Imaging के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूँ?
    आप यहां से अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).


