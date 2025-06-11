---
"description": "जानें कि Aspose.Imaging for .NET के साथ DJVU पेजों को अलग-अलग छवियों में कैसे बदलें। चरण-दर-चरण मार्गदर्शिका, कोड उदाहरण और अक्सर पूछे जाने वाले प्रश्न प्रदान किए गए हैं।"
"linktitle": ".NET के लिए Aspose.Imaging में DJVU पृष्ठों की श्रेणी को अलग-अलग छवियों में बदलें"
"second_title": "Aspose.Imaging .NET इमेज प्रोसेसिंग API"
"title": ".NET के लिए Aspose.Imaging में DJVU पृष्ठों की श्रेणी को अलग-अलग छवियों में बदलें"
"url": "/hi/net/image-format-conversion/convert-range-of-djvu-pages-to-separate-images/"
"weight": 19
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.Imaging में DJVU पृष्ठों की श्रेणी को अलग-अलग छवियों में बदलें

यदि आप छवि रूपांतरण और हेरफेर कार्यों को संभालने के लिए एक शक्तिशाली .NET लाइब्रेरी की तलाश कर रहे हैं, तो Aspose.Imaging for .NET एकदम सही विकल्प है। इस ट्यूटोरियल में, हम आपको Aspose.Imaging का उपयोग करके DJVU पृष्ठों की एक श्रृंखला को अलग-अलग छवियों में बदलने की प्रक्रिया के माध्यम से मार्गदर्शन करेंगे। आपको इस कार्य को पूरा करने में मदद करने के लिए चरण-दर-चरण निर्देश और कोड स्निपेट मिलेंगे।

## आवश्यक शर्तें

इससे पहले कि हम रूपांतरण प्रक्रिया में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

1. Aspose.Imaging for .NET लाइब्रेरी

आपको Aspose.Imaging for .NET इंस्टॉल करना होगा। अगर आपने पहले से ऐसा नहीं किया है, तो आप इसे यहाँ से डाउनलोड कर सकते हैं। [Aspose.Imaging for .NET पृष्ठ](https://releases.aspose.com/imaging/net/).

2. विकास पर्यावरण

इसके साथ आगे बढ़ने के लिए, आपके पास Visual Studio या किसी अन्य .NET IDE के साथ एक विकास परिवेश स्थापित होना चाहिए।

## आवश्यक नामस्थान आयात करना

सबसे पहले, आपको Aspose.Imaging के साथ काम करने के लिए अपने कोड में आवश्यक नेमस्पेस शामिल करने होंगे। आप इसे इस प्रकार कर सकते हैं:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Djvu;
using Aspose.Imaging.FileFormats.Djvu.Options;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.RasterImage;
```

## DJVU पृष्ठों को परिवर्तित करना

अब, आइए Aspose.Imaging for .NET का उपयोग करके DJVU पृष्ठों की एक श्रृंखला को अलग-अलग छवियों में परिवर्तित करने की प्रक्रिया को आसान चरणों की एक श्रृंखला में विभाजित करें।

### चरण 1: DJVU छवि लोड करें

शुरू करने के लिए, आपको उस DJVU छवि को लोड करना चाहिए जिसे आप कनवर्ट करना चाहते हैं। `"Your Document Directory"` आपकी DJVU फ़ाइल का वास्तविक पथ.

```csharp
string dataDir = "Your Document Directory";

// DjVu छवि लोड करें
using (DjvuImage image = (DjvuImage)Image.Load(dataDir + "Sample.djvu"))
{
    // आगे की प्रक्रिया के लिए आपका कोड यहां जाएगा।
}
```

### चरण 2: निर्यात विकल्प सेट करें

अब, इसका एक उदाहरण बनाएं `BmpOptions` और परिणामी छवियों के लिए वांछित विकल्प कॉन्फ़िगर करें। इस उदाहरण में, हमने सेट किया है `BitsPerPixel` 32 तक।

```csharp
BmpOptions exportOptions = new BmpOptions();
exportOptions.BitsPerPixel = 32;
```

### चरण 3: पृष्ठों की सीमा निर्धारित करें

उन पृष्ठों की श्रेणी निर्दिष्ट करने के लिए जिन्हें आप निर्यात करना चाहते हैं, इसका एक उदाहरण बनाएँ `IntRange` और इसे पेज रेंज के साथ आरंभ करें। इस मामले में, हम पेज 0 से 2 तक निर्यात करते हैं।

```csharp
IntRange range = new IntRange(0, 2);
```

### चरण 4: पृष्ठों के माध्यम से लूप करें

अब, निर्दिष्ट सीमा के भीतर पृष्ठों के माध्यम से लूप करें और प्रत्येक पृष्ठ को एक अलग BMP छवि के रूप में सहेजें। DJVU फ़ाइलें लेयरिंग का समर्थन नहीं करती हैं, इसलिए हम प्रत्येक पृष्ठ को अलग से सहेजते हैं।

```csharp
int counter = 0;
foreach (var i in range.Range)
{
    exportOptions.MultiPageOptions = new DjvuMultiPageOptions(range.GetArrayOneItemFromIndex(counter));
    image.Save(dataDir + string.Format("{0}_out.bmp", counter++), exportOptions);
}
```

और बस! आपने Aspose.Imaging for .NET का उपयोग करके DJVU पृष्ठों की एक श्रृंखला को अलग-अलग छवियों में सफलतापूर्वक परिवर्तित कर लिया है।

## निष्कर्ष

Aspose.Imaging for .NET छवि रूपांतरण कार्यों को सरल बनाता है, जिससे यह डेवलपर्स के लिए एक उत्कृष्ट विकल्प बन जाता है। इस ट्यूटोरियल में, हमने आपको DJVU पृष्ठों को अलग-अलग छवियों में बदलने की प्रक्रिया के बारे में चरण दर चरण बताया है। आपके पास सही कोड और लाइब्रेरी होने पर, छवि रूपांतरण आसान हो जाता है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या Aspose.Imaging for .NET एक निःशुल्क लाइब्रेरी है?

A1: नहीं, यह एक व्यावसायिक पुस्तकालय है, लेकिन आप डाउनलोड कर सकते हैं [मुफ्त परीक्षण](https://releases.aspose.com/) अपनी क्षमताओं का परीक्षण करने के लिए।

### प्रश्न 2: क्या मैं Aspose.Imaging for .NET के लिए एक अस्थायी लाइसेंस खरीद सकता हूँ?

A2: हाँ, आप अस्थायी लाइसेंस प्राप्त कर सकते हैं [खरीद पृष्ठ](https://purchase.aspose.com/temporary-license/).

### प्रश्न 3: मैं Aspose.Imaging for .NET के लिए दस्तावेज़ कहां पा सकता हूं?

A3: आप विस्तृत दस्तावेज़ देख सकते हैं [यहाँ](https://reference.aspose.com/imaging/net/).

### प्रश्न 4: Aspose.Imaging for .NET किस छवि प्रारूप का समर्थन करता है?

A4: Aspose.Imaging for .NET कई प्रकार के छवि प्रारूपों का समर्थन करता है, जिसमें BMP, JPEG, PNG, TIFF, आदि शामिल हैं।

### प्रश्न 5: यदि मुझे कोई समस्या आती है तो क्या मुझे समर्थन एवं सहायता मिल सकती है?

A5: हां, आप सहायता मांग सकते हैं और समुदाय से जुड़ सकते हैं [Aspose.Imaging फ़ोरम](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}