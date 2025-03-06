---
title: .NET के लिए Aspose.Imaging में DJVU पेजों की रेंज को अलग-अलग छवियों में बदलें
linktitle: .NET के लिए Aspose.Imaging में DJVU पेजों की रेंज को अलग-अलग छवियों में बदलें
second_title: Aspose.Imaging .NET इमेज प्रोसेसिंग एपीआई
description: जानें कि .NET के लिए Aspose.Imaging के साथ DJVU पृष्ठों को अलग-अलग छवियों में कैसे परिवर्तित किया जाए। चरण-दर-चरण मार्गदर्शिका, कोड उदाहरण और अक्सर पूछे जाने वाले प्रश्न प्रदान किए गए।
weight: 19
url: /hi/net/image-format-conversion/convert-range-of-djvu-pages-to-separate-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.Imaging में DJVU पेजों की रेंज को अलग-अलग छवियों में बदलें

यदि आप छवि रूपांतरण और हेरफेर कार्यों को संभालने के लिए एक शक्तिशाली .NET लाइब्रेरी की तलाश में हैं, तो .NET के लिए Aspose.Imaging सही विकल्प है। इस ट्यूटोरियल में, हम Aspose.Imaging का उपयोग करके DJVU पृष्ठों की एक श्रृंखला को अलग-अलग छवियों में परिवर्तित करने की प्रक्रिया में आपका मार्गदर्शन करेंगे। इस कार्य को प्राप्त करने में सहायता के लिए आपको चरण-दर-चरण निर्देश और कोड स्निपेट मिलेंगे।

## आवश्यक शर्तें

इससे पहले कि हम रूपांतरण प्रक्रिया में उतरें, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

1. .NET लाइब्रेरी के लिए Aspose.Imaging

 आपको .NET के लिए Aspose.Imaging स्थापित करना होगा। यदि आपने पहले से नहीं किया है, तो आप इसे यहां से डाउनलोड कर सकते हैं[.NET पेज के लिए Aspose.Imaging](https://releases.aspose.com/imaging/net/).

2. विकास पर्यावरण

अनुसरण करने के लिए, आपके पास विज़ुअल स्टूडियो या किसी अन्य .NET IDE के साथ एक विकास वातावरण स्थापित होना चाहिए।

## आवश्यक नामस्थान आयात करना

सबसे पहले, आपको Aspose.Imaging के साथ काम करने के लिए अपने कोड में आवश्यक नेमस्पेस शामिल करना होगा। यहां बताया गया है कि आप यह कैसे कर सकते हैं:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Djvu;
using Aspose.Imaging.FileFormats.Djvu.Options;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.RasterImage;
```

## डीजेवीयू पेज परिवर्तित करना

अब, आइए .NET के लिए Aspose.Imaging का उपयोग करके DJVU पृष्ठों की एक श्रृंखला को अलग-अलग छवियों में परिवर्तित करने की प्रक्रिया को आसान चरणों की एक श्रृंखला में विभाजित करें।

### चरण 1: डीजेवीयू छवि लोड करें

 आरंभ करने के लिए, आपको डीजेवीयू छवि लोड करनी चाहिए जिसे आप कनवर्ट करना चाहते हैं। प्रतिस्थापित करें`"Your Document Directory"` आपकी DJVU फ़ाइल के वास्तविक पथ के साथ।

```csharp
string dataDir = "Your Document Directory";

// एक DjVu छवि लोड करें
using (DjvuImage image = (DjvuImage)Image.Load(dataDir + "Sample.djvu"))
{
    // आगे की प्रक्रिया के लिए आपका कोड यहां जाएगा।
}
```

### चरण 2: निर्यात विकल्प सेट करें

अब, का एक उदाहरण बनाएं`BmpOptions` और परिणामी छवियों के लिए वांछित विकल्पों को कॉन्फ़िगर करें। इस उदाहरण में, हमने सेट किया है`BitsPerPixel` से 32.

```csharp
BmpOptions exportOptions = new BmpOptions();
exportOptions.BitsPerPixel = 32;
```

### चरण 3: पृष्ठों की श्रेणी परिभाषित करें

 उन पृष्ठों की श्रेणी निर्दिष्ट करने के लिए जिन्हें आप निर्यात करना चाहते हैं, इसका एक उदाहरण बनाएं`IntRange` और इसे पृष्ठ श्रेणी के साथ प्रारंभ करें। इस मामले में, हम पृष्ठ 0 से 2 तक निर्यात करते हैं।

```csharp
IntRange range = new IntRange(0, 2);
```

### चरण 4: पृष्ठों के माध्यम से लूप करें

अब, निर्दिष्ट सीमा के भीतर पृष्ठों के माध्यम से लूप करें और प्रत्येक पृष्ठ को एक अलग बीएमपी छवि के रूप में सहेजें। DJVU फ़ाइलें लेयरिंग का समर्थन नहीं करती हैं, इसलिए हम प्रत्येक पृष्ठ को अलग-अलग सहेजते हैं।

```csharp
int counter = 0;
foreach (var i in range.Range)
{
    exportOptions.MultiPageOptions = new DjvuMultiPageOptions(range.GetArrayOneItemFromIndex(counter));
    image.Save(dataDir + string.Format("{0}_out.bmp", counter++), exportOptions);
}
```

और बस! आपने .NET के लिए Aspose.Imaging का उपयोग करके DJVU पृष्ठों की एक श्रृंखला को अलग-अलग छवियों में सफलतापूर्वक परिवर्तित कर दिया है।

## निष्कर्ष

.NET के लिए Aspose.Imaging छवि रूपांतरण कार्यों को सरल बनाता है, जिससे यह डेवलपर्स के लिए एक उत्कृष्ट विकल्प बन जाता है। इस ट्यूटोरियल में, हमने आपको चरण दर चरण डीजेवीयू पेजों को अलग-अलग छवियों में परिवर्तित करने की प्रक्रिया के बारे में बताया। आपके पास सही कोड और लाइब्रेरी होने से, छवि रूपांतरण आसान हो जाता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या .NET के लिए Aspose.Imaging एक निःशुल्क लाइब्रेरी है?

 A1: नहीं, यह एक व्यावसायिक लाइब्रेरी है, लेकिन आप इसे डाउनलोड कर सकते हैं[मुफ्त परीक्षण](https://releases.aspose.com/) इसकी क्षमताओं का परीक्षण करने के लिए।

### Q2: क्या मैं .NET के लिए Aspose.Imaging के लिए एक अस्थायी लाइसेंस खरीद सकता हूँ?

 उ2: हां, आप यहां से अस्थायी लाइसेंस प्राप्त कर सकते हैं[खरीद पृष्ठ](https://purchase.aspose.com/temporary-license/).

### Q3: मुझे .NET के लिए Aspose.Imaging के लिए दस्तावेज़ कहां मिल सकते हैं?

 A3: आप व्यापक दस्तावेज़ीकरण का पता लगा सकते हैं[यहाँ](https://reference.aspose.com/imaging/net/).

### Q4: .NET के लिए Aspose.Imaging किस छवि प्रारूप का समर्थन करता है?

A4: .NET के लिए Aspose.Imaging BMP, JPEG, PNG, TIFF और अन्य सहित छवि प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है।

### Q5: यदि मुझे कोई समस्या आती है तो क्या मुझे समर्थन और सहायता मिल सकती है?

 A5: हां, आप मदद मांग सकते हैं और समुदाय से जुड़ सकते हैं[Aspose.इमेजिंग फोरम](https://forum.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
