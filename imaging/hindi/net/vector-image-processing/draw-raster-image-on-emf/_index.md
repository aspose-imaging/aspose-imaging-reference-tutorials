---
title: .NET के लिए Aspose.Imaging के साथ EMF पर रेखापुंज छवियाँ बनाएं
linktitle: .NET के लिए Aspose.Imaging में EMF पर रेखापुंज छवि बनाएं
second_title: Aspose.Imaging .NET इमेज प्रोसेसिंग एपीआई
description: .NET के लिए Aspose.Imaging का उपयोग करके EMF फ़ाइलों पर रेखापुंज चित्र बनाना सीखें। सहजता से आश्चर्यजनक दृश्य बनाएं।
weight: 10
url: /hi/net/vector-image-processing/draw-raster-image-on-emf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.Imaging के साथ EMF पर रेखापुंज छवियाँ बनाएं


## परिचय

.NET के लिए Aspose.Imaging का उपयोग करके EMF (एन्हांस्ड मेटाफ़ाइल) पर रैस्टर छवि कैसे बनाएं, इस चरण-दर-चरण ट्यूटोरियल में आपका स्वागत है। Aspose.Imaging एक शक्तिशाली लाइब्रेरी है जो आपको अपने .NET अनुप्रयोगों में विभिन्न छवि प्रारूपों के साथ काम करने की अनुमति देती है। इस ट्यूटोरियल में, हम आपको ईएमएफ फ़ाइल पर एक रेखापुंज छवि बनाने की प्रक्रिया में मार्गदर्शन करेंगे। आप सीखेंगे कि आवश्यक नामस्थान कैसे आयात करें, और हम सीखने की प्रक्रिया को आसान बनाने के लिए प्रत्येक उदाहरण को कई चरणों में तोड़ देंगे।

आएँ शुरू करें!

## आवश्यक शर्तें

इससे पहले कि हम ट्यूटोरियल में उतरें, आपके पास निम्नलिखित पूर्वापेक्षाएँ होनी चाहिए:

1. विजुअल स्टूडियो: .NET कोड लिखने और चलाने के लिए आपको अपने कंप्यूटर पर विजुअल स्टूडियो स्थापित करना होगा।

2.  .NET के लिए Aspose.Imaging: सुनिश्चित करें कि आपके पास .NET के लिए Aspose.Imaging स्थापित है। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/imaging/net/).

3. एक रेखापुंज छवि: एक रेखापुंज छवि (उदाहरण के लिए, एक पीएनजी फ़ाइल) तैयार करें जिसे आप ईएमएफ फ़ाइल पर बनाना चाहते हैं।

## नामस्थान आयात करें

अपने विज़ुअल स्टूडियो प्रोजेक्ट में, आपको Aspose.Imaging के साथ काम करने के लिए आवश्यक नेमस्पेस आयात करने की आवश्यकता होगी। अपनी कोड फ़ाइल में निम्नलिखित नामस्थान जोड़ें:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Emf;
using Aspose.Imaging.FileFormats.Png;
using Aspose.Imaging.Graphics;
using System;
```

अब जबकि हमारे पास पूर्वापेक्षाएँ और नामस्थान मौजूद हैं, आइए उदाहरण को कई चरणों में तोड़ें।

## चरण 1: खींची जाने वाली छवि को लोड करें

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
{
    // चरण 1 के लिए आपका कोड यहां जाता है
}
```

 इस चरण में, हम उस रेखापुंज छवि को लोड करते हैं जिसे आप EMF फ़ाइल पर बनाना चाहते हैं। प्रतिस्थापित करें`"Your Document Directory"` आपकी छवि के पथ के साथ.

## चरण 2: ईएमएफ ड्राइंग सतह को लोड करें

```csharp
using (EmfImage canvasImage = (EmfImage)Image.Load(dataDir + "input.emf"))
{
    // चरण 2 के लिए आपका कोड यहां जाता है
}
```

 यहां, हम ईएमएफ फ़ाइल लोड करते हैं जो हमारी छवि के लिए ड्राइंग सतह के रूप में काम करेगी। प्रतिस्थापित करना सुनिश्चित करें`"input.emf"` आपकी EMF फ़ाइल के पथ के साथ।

## चरण 3: एक ईएमएफ रिकॉर्डर ग्राफ़िक्स बनाएं

```csharp
EmfRecorderGraphics2D graphics = EmfRecorderGraphics2D.FromEmfImage(canvasImage);
```

 इस चरण में, हम एक उदाहरण बनाते हैं`EmfRecorderGraphics2D` ईएमएफ छवि से. यह हमें ड्राइंग संचालन को रिकॉर्ड करने की अनुमति देता है।

## चरण 4: रेखापुंज छवि बनाएं

```csharp
graphics.DrawImage(
    imageToDraw,
    new Rectangle(67, 67, canvasImage.Width, canvasImage.Height),
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    GraphicsUnit.Pixel);
```

 इस चरण में, हम इसका उपयोग करते हैं`DrawImage`लोड की गई रेखापुंज छवि को EMF फ़ाइल पर खींचने की विधि। आप खींची गई छवि की स्थिति और आकार को नियंत्रित करने के लिए स्रोत और गंतव्य आयत निर्दिष्ट कर सकते हैं।

## चरण 5: परिणाम छवि सहेजें

```csharp
using (EmfImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "input.DrawImage.emf");
}
```

 अंत में, हम परिणामी ईएमएफ छवि को खींची गई रेखापुंज छवि के साथ एक फ़ाइल में सहेजते हैं। फ़ाइल को निर्दिष्ट निर्देशिका में "input.DrawImage.emf" नाम से सहेजा जाएगा`dataDir`.

बधाई हो! आपने .NET के लिए Aspose.Imaging का उपयोग करके EMF फ़ाइल पर सफलतापूर्वक एक रेखापुंज छवि खींची है। वांछित प्रभाव प्राप्त करने के लिए विभिन्न स्रोत और गंतव्य आयतों का अन्वेषण और प्रयोग करने के लिए स्वतंत्र महसूस करें।

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा कि EMF फ़ाइल पर रैस्टर छवि बनाने के लिए .NET के लिए Aspose.Imaging का उपयोग कैसे करें। चरण-दर-चरण मार्गदर्शिका का पालन करके, आप इस कार्यक्षमता को अपने .NET अनुप्रयोगों में आसानी से एकीकृत कर सकते हैं।

Aspose.Imaging के साथ आश्चर्यजनक छवियां बनाने का आनंद लें!

## पूछे जाने वाले प्रश्न

### 1. क्या मैं एक ही EMF फ़ाइल पर एकाधिक छवियाँ बना सकता हूँ?

हां, आप अलग-अलग स्रोत और गंतव्य आयतों के साथ ड्राइंग प्रक्रिया को दोहराकर एक ही ईएमएफ फ़ाइल पर कई छवियां बना सकते हैं।

### 2. क्या Aspose.Imaging .NET कोर के साथ संगत है?

हां, .NET के लिए Aspose.Imaging .NET फ्रेमवर्क और .NET कोर दोनों के साथ संगत है।

### 3. मैं खींची गई छवि में परिवर्तन, जैसे रोटेशन या स्केलिंग, कैसे लागू कर सकता हूं?

 आप इसमें स्रोत और गंतव्य आयतों में हेरफेर करके परिवर्तन लागू कर सकते हैं`DrawImage` तरीका।

### 4. क्या मैं ईएमएफ फ़ाइल पर वेक्टर ग्राफ़िक्स भी बना सकता हूँ?

हाँ, आप .NET के लिए Aspose.Imaging का उपयोग करके रेखापुंज छवियों के अलावा वेक्टर ग्राफिक्स और आकृतियाँ बना सकते हैं।

### 5. मुझे Aspose.Imaging के लिए समर्थन कहाँ से मिल सकता है?

 समर्थन और सहायता के लिए, आप Aspose.Imaging फोरम पर जा सकते हैं[यहाँ](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
