---
title: .NET के लिए Aspose.Imaging के साथ APS को PSD में बदलें
linktitle: .NET के लिए Aspose.Imaging में APS को PSD में बदलें
second_title: Aspose.Imaging .NET इमेज प्रोसेसिंग एपीआई
description: .NET के लिए Aspose.Imaging के साथ APS को PSD में बदलें। रूपांतरण के दौरान वेक्टर गुणों को सुरक्षित रखें।
type: docs
weight: 11
url: /hi/net/advanced-features/convert-aps-to-psd/
---
क्या आप वेक्टर गुणों को संरक्षित करते हुए आसानी से एपीएस फ़ाइलों को पीएसडी प्रारूप में परिवर्तित करना चाहते हैं? .NET के लिए Aspose.Imaging आपके कार्य को सरल बनाने के लिए यहां है। इस चरण-दर-चरण मार्गदर्शिका में, हम आपको दिखाएंगे कि इस रूपांतरण को कैसे प्राप्त किया जाए। 

## आवश्यक शर्तें

इससे पहले कि हम इस प्रक्रिया में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

1.  .NET लाइब्रेरी के लिए Aspose.Imaging: आपको .NET के लिए Aspose.Imaging लाइब्रेरी को डाउनलोड और इंस्टॉल करना होगा। आप इसे यहां से प्राप्त कर सकते हैं[डाउनलोड पेज](https://releases.aspose.com/imaging/net/).

2. आपकी दस्तावेज़ निर्देशिका: सुनिश्चित करें कि आपके पास अपनी दस्तावेज़ निर्देशिका का पथ तैयार है। यहीं पर APS फ़ाइल स्थित है.

3. C# का बुनियादी ज्ञान: रूपांतरण प्रक्रिया को लागू करने के लिए C# प्रोग्रामिंग भाषा से परिचित होना आवश्यक है।

## नामस्थान आयात करें

आइए .NET के लिए Aspose.Imaging के साथ काम करने के लिए आवश्यक नेमस्पेस आयात करके शुरुआत करें। सुनिश्चित करें कि आपने अपने प्रोजेक्ट में Aspose.Imaging लाइब्रेरी का संदर्भ जोड़ा है।

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Vectorization;
```

## चरण 1: एपीएस फ़ाइल लोड करें

उस एपीएस फ़ाइल को लोड करके शुरुआत करें जिसे आप PSD में कनवर्ट करना चाहते हैं। आप दस्तावेज़ निर्देशिका का पथ भी निर्दिष्ट करेंगे जहां एपीएस फ़ाइल स्थित है।

```csharp
string dataDir = "Your Document Directory";
string inputFileName = dataDir + "SimpleShapes.cdr";

using (Image image = Image.Load(inputFileName))
{
    // आपका कोड यहां जाता है
}
```

## चरण 2: रूपांतरण विकल्प कॉन्फ़िगर करें

इस चरण में, आपको एपीएस फ़ाइल को PSD प्रारूप में निर्यात करने के लिए रूपांतरण विकल्प सेट करने की आवश्यकता है। Aspose.Imaging वेक्टर छवि रूपांतरण के लिए विभिन्न विकल्प प्रदान करता है।

```csharp
PsdOptions imageOptions = new PsdOptions()
{
    VectorRasterizationOptions = new VectorRasterizationOptions(),
    VectorizationOptions = new PsdVectorizationOptions()
    {
        VectorDataCompositionMode = VectorDataCompositionMode.SeparateLayers
    }
};

imageOptions.VectorRasterizationOptions.PageWidth = image.Width;
imageOptions.VectorRasterizationOptions.PageHeight = image.Height;
```

## चरण 3: PSD फ़ाइल सहेजें

अब, परिवर्तित PSD फ़ाइल को आपके इच्छित स्थान पर सहेजने का समय आ गया है।

```csharp
image.Save(dataDir + "result.psd", imageOptions);
```

## चरण 4: साफ़ करें

रूपांतरण पूरा होने के बाद, आप प्रक्रिया के दौरान बनाई गई अस्थायी PSD फ़ाइल को हटाना चाह सकते हैं।

```csharp
File.Delete(dataDir + "result.psd");
```

## निष्कर्ष

.NET के लिए Aspose.Imaging के साथ APS को PSD प्रारूप में परिवर्तित करना सीधा और कुशल है। यह शक्तिशाली लाइब्रेरी आपको रूपांतरण के दौरान वेक्टर गुणों को बनाए रखने की अनुमति देती है, जिससे यह ग्राफिक डिजाइनरों और डेवलपर्स के लिए एक मूल्यवान उपकरण बन जाता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या .NET के लिए Aspose.Imaging एक निःशुल्क लाइब्रेरी है?

 A1: .NET के लिए Aspose.Imaging एक व्यावसायिक लाइब्रेरी है। आप पर लाइसेंसिंग विकल्प तलाश सकते हैं[खरीद पृष्ठ](https://purchase.aspose.com/buy).

### Q2: क्या मैं इसे खरीदने से पहले .NET के लिए Aspose.Imaging आज़मा सकता हूँ?

 उ2: हाँ, आप .NET के लिए Aspose.Imaging का निःशुल्क परीक्षण प्राप्त कर सकते हैं[परीक्षण पृष्ठ](https://releases.aspose.com/imaging/net/).

### Q3: PSD में रूपांतरण के लिए कौन से वेक्टर छवि प्रारूप समर्थित हैं?

A3: .NET के लिए Aspose.Imaging CDR, EMF, EPS, ODG, SVG और WMF जैसे वेक्टर छवि प्रारूपों को PSD प्रारूप में बदलने का समर्थन करता है।

### Q4: क्या रूपांतरण के दौरान आकृतियों की जटिलता की कोई सीमाएँ हैं?

A4: वर्तमान में, Aspose.Imaging बनावट ब्रश के बिना या स्ट्रोक के साथ खुली आकृतियों के बिना बहुत जटिल आकृतियों के निर्यात का समर्थन करता है। हालाँकि, आगामी रिलीज़ में इसमें सुधार किया जा सकता है।

### Q5: मैं .NET के लिए Aspose.Imaging से संबंधित सहायता कहां से प्राप्त कर सकता हूं या प्रश्न पूछ सकता हूं?

 A5: यदि आपके कोई प्रश्न हैं या सहायता की आवश्यकता है, तो आप यहां जा सकते हैं[Aspose.इमेजिंग फ़ोरम](https://forum.aspose.com/)सहायता के लिए।
