---
title: .NET के लिए Aspose.Imaging में रेखापुंज छवि में वेक्टर छवि बनाएं
linktitle: .NET के लिए Aspose.Imaging में रेखापुंज छवि में वेक्टर छवि बनाएं
second_title: Aspose.Imaging .NET इमेज प्रोसेसिंग एपीआई
description: Aspose.Imaging का उपयोग करके .NET में वेक्टर छवियों को रेखापुंज छवियों में बदलने का तरीका जानें। कुशल छवि प्रसंस्करण के लिए चरण-दर-चरण मार्गदर्शिका।
type: docs
weight: 13
url: /hi/net/vector-image-processing/draw-vector-image-to-raster-image/
---

क्या आप अपने .NET अनुप्रयोगों में वेक्टर छवियों को आसानी से रेखापुंज छवियों में परिवर्तित करना चाहते हैं? .NET के लिए Aspose.Imaging इस कार्य के लिए एक कुशल समाधान प्रदान करता है। इस चरण-दर-चरण मार्गदर्शिका में, हम आपको .NET के लिए Aspose.Imaging का उपयोग करके वेक्टर छवियों को रेखापुंज छवियों में खींचने की प्रक्रिया के बारे में बताएंगे। 

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

### 1. .NET के लिए Aspose.Imaging

 आपके पास .NET के लिए Aspose.Imaging स्थापित होना चाहिए। यदि आपके पास यह नहीं है, तो आप इसे वेबसाइट से डाउनलोड कर सकते हैं[.NET के लिए Aspose.Imaging डाउनलोड करें](https://releases.aspose.com/imaging/net/).

### 2. .NET विकास पर्यावरण

सुनिश्चित करें कि आपके कंप्यूटर पर .NET विकास वातावरण स्थापित है। आप विज़ुअल स्टूडियो या किसी अन्य .NET डेवलपमेंट टूल का उपयोग कर सकते हैं।

अब, आइए वेक्टर छवियों को रेखापुंज करने के लिए छवियों को खींचने की प्रक्रिया को सरल, आसानी से पालन किए जाने वाले चरणों में विभाजित करें:

## चरण 1: अपना प्रोजेक्ट प्रारंभ करें

अपने विकास परिवेश में एक नया .NET प्रोजेक्ट बनाकर प्रारंभ करें। सुनिश्चित करें कि आपके प्रोजेक्ट में .NET के लिए Aspose.Imaging एकीकृत है।

## चरण 2: वेक्टर छवि लोड करें

इस चरण में, हम वेक्टर छवि (एसवीजी प्रारूप में) लोड करते हैं जिसे आप रास्टर छवि में परिवर्तित करना चाहते हैं।

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ...
}
```

## चरण 3: वेक्टर छवि को व्यवस्थित करें

अब, हमें एसवीजी छवि को पीएनजी प्रारूप में व्यवस्थित करने की आवश्यकता है। यहीं पर वेक्टर से रैस्टर में रूपांतरण होता है।

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## चरण 4: रेखापुंज छवि लोड करें

रैस्टराइज़ेशन के बाद, आगे की ड्राइंग के लिए स्ट्रीम से पीएनजी छवि लोड करें।

```csharp
drawnImageStream.Seek(0, System.IO.SeekOrigin.Begin);
using (RasterImage imageToDraw = (RasterImage)Image.Load(drawnImageStream))
{
    // ...
}
```

## चरण 5: रेखापुंज छवि बनाएं

अब, हम मौजूदा एसवीजी छवि पर रेखापुंज छवि बना सकते हैं।

```csharp
Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D graphics =
    new Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D(svgImage);

int width = imageToDraw.Width / 2;
int height = imageToDraw.Height / 2;
Point origin = new Point((svgImage.Width - width) / 2, (svgImage.Height - height) / 2);
Size size = new Size(width, height);
graphics.DrawImage(imageToDraw, origin, size);
```

## चरण 6: परिणाम सहेजें

अंत में, परिणाम छवि सहेजें। अब आपके पास एक रेखापुंज छवि है जिसमें आपकी वेक्टर छवि शामिल है।

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने दिखाया है कि .NET के लिए Aspose.Imaging का उपयोग करके वेक्टर छवियों को रेखापुंज छवियों में कैसे परिवर्तित किया जाए। इन सरल चरणों के साथ, आप इस कार्यक्षमता को आसानी से अपने .NET अनुप्रयोगों में एकीकृत कर सकते हैं।

### अक्सर पूछे जाने वाले प्रश्नों

### .NET के लिए Aspose.Imaging क्या है?
.NET के लिए Aspose.Imaging एक .NET लाइब्रेरी है जो शक्तिशाली छवि प्रसंस्करण सुविधाएँ प्रदान करती है, जिसमें विभिन्न छवि प्रारूपों के साथ काम करने, छवियों को परिवर्तित करने और उन्नत छवि हेरफेर कार्य करने की क्षमता शामिल है।

### मुझे .NET के लिए Aspose.Imaging के लिए दस्तावेज़ कहाँ मिल सकते हैं?
 आप .NET के लिए Aspose.Imaging के लिए दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/imaging/net/).

### क्या कोई निःशुल्क परीक्षण संस्करण उपलब्ध है?
 हां, आप .NET के लिए Aspose.Imaging के निःशुल्क परीक्षण तक पहुंच सकते हैं[यहाँ](https://releases.aspose.com/).

### मैं .NET के लिए Aspose.Imaging के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूँ?
 यदि आपको अस्थायी लाइसेंस की आवश्यकता है, तो आप एक प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).

### मुझे .NET के लिए Aspose.Imaging के लिए समर्थन कहाँ से मिल सकता है?
 किसी भी सहायता या प्रश्न के लिए, आप यहां जा सकते हैं[Aspose.इमेजिंग फोरम](https://forum.aspose.com/).
