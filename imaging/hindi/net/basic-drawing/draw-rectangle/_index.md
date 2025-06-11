---
"description": "Aspose.Imaging for .NET में आयत बनाना सीखें - यह आपके .NET अनुप्रयोगों में छवि हेरफेर के लिए एक बहुमुखी उपकरण है।"
"linktitle": ".NET के लिए Aspose.Imaging में आयत बनाएं"
"second_title": "Aspose.Imaging .NET इमेज प्रोसेसिंग API"
"title": ".NET के लिए Aspose.Imaging में आयत बनाना"
"url": "/hi/net/basic-drawing/draw-rectangle/"
"weight": 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.Imaging में आयत बनाना

.NET अनुप्रयोगों में छवियाँ बनाना और उनमें हेरफेर करना एक जटिल कार्य हो सकता है, लेकिन Aspose.Imaging for .NET की शक्ति के साथ, यह उल्लेखनीय रूप से सरल हो जाता है। इस चरण-दर-चरण मार्गदर्शिका में, हम आपको Aspose.Imaging for .NET का उपयोग करके आयत बनाने की प्रक्रिया से परिचित कराएँगे। आप सीखेंगे कि छवि कैसे बनाएँ, उसके गुण कैसे सेट करें, आयत कैसे बनाएँ और अपना काम कैसे सेव करें। चलिए शुरू करते हैं!

## आवश्यक शर्तें

आरंभ करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

1. Aspose.Imaging for .NET: सुनिश्चित करें कि आपने Aspose.Imaging for .NET लाइब्रेरी स्थापित की है। यदि आपने पहले से ऐसा नहीं किया है, तो आप इसे यहाँ से डाउनलोड कर सकते हैं। [डाउनलोड पृष्ठ](https://releases.aspose.com/imaging/net/).

2. विकास परिवेश: आपके पास विजुअल स्टूडियो या किसी अन्य .NET विकास उपकरण के साथ एक विकास परिवेश स्थापित होना चाहिए।

अब, आइए चरण-दर-चरण ट्यूटोरियल से शुरुआत करें।

## नामस्थान आयात करना

पहला कदम .NET के लिए Aspose.Imaging के साथ काम करने के लिए आवश्यक नामस्थानों को आयात करना है। यहाँ बताया गया है कि आप इसे कैसे करते हैं:

### चरण 1: नामस्थान आयात करें

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

उपरोक्त कोड में, हम Aspose.Imaging नामस्थानों को आयात कर रहे हैं, जो छवि हेरफेर के लिए आवश्यक कक्षाएं और विधियां प्रदान करते हैं।

## आयताकार चित्र बनाना

अब, आइए एक छवि पर आयत बनाना शुरू करें।

### चरण 2: एक छवि बनाएँ

```csharp
string dataDir = "Your Document Directory";  // अपने दस्तावेज़ निर्देशिका का पथ सेट करें
using (FileStream stream = new FileStream(dataDir, FileMode.Create))
{
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;
    saveOptions.Source = new StreamSource(stream);

    using (Image image = Image.Create(saveOptions, 100, 100))
    {
        // आयत बनाने के लिए आपका कोड यहाँ जाएगा
        image.Save();
    }
}
```

इस चरण में, हम इसका एक उदाहरण बनाते हैं `Image` क्लास और छवि निर्माण के लिए विभिन्न गुण सेट करें, जैसे कि `BitsPerPixel` और आउटपुट स्ट्रीम। फिर हम 100x100 पिक्सेल आकार की एक खाली छवि बनाते हैं।

### चरण 3: ग्राफ़िक्स आरंभ करें और आयत बनाएं

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

इस चरण में, हम एक आरंभीकरण करते हैं `Graphics` ऑब्जेक्ट पर, पीले रंग की पृष्ठभूमि के साथ ग्राफ़िक्स सतह को साफ़ करें, और छवि पर अलग-अलग रंगों और स्थितियों के साथ दो आयताकार बनाएं।

### चरण 4: छवि सहेजें

```csharp
image.Save();
```

अंत में, हम खींची गई आयतों के साथ छवि को सुरक्षित करते हैं।

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा है कि .NET के लिए Aspose.Imaging का उपयोग करके किसी छवि पर आयत कैसे बनाएं। इस गाइड में बताए गए चरणों का पालन करके, आप आसानी से अपने .NET अनुप्रयोगों में छवियाँ बना और उनमें हेरफेर कर सकते हैं। Aspose.Imaging छवि प्रबंधन को सरल बनाता है, जिससे यह डेवलपर्स के लिए एक शक्तिशाली उपकरण बन जाता है।

अब आप Aspose.Imaging का उपयोग करके अपने .NET प्रोजेक्ट में इमेज मैनिपुलेशन को शामिल करने के लिए तैयार हैं। प्रयोग करना शुरू करें और शानदार दृश्य बनाएं!

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: मैं Aspose.Imaging for .NET के साथ और कौन सी आकृतियाँ बना सकता हूँ?

A1: आप Aspose.Imaging लाइब्रेरी का उपयोग करके विभिन्न आकार जैसे दीर्घवृत्त, रेखाएँ और वक्र बना सकते हैं।

### प्रश्न 2: क्या मैं Windows और वेब अनुप्रयोगों दोनों में .NET के लिए Aspose.Imaging का उपयोग कर सकता हूँ?

A2: हां, Aspose.Imaging for .NET का उपयोग विंडोज और वेब अनुप्रयोगों दोनों में किया जा सकता है, जिससे यह विभिन्न परियोजना प्रकारों के लिए बहुमुखी बन जाता है।

### प्रश्न 3: क्या Aspose.Imaging for .NET एक निःशुल्क लाइब्रेरी है?

A3: Aspose.Imaging for .NET एक व्यावसायिक लाइब्रेरी है, लेकिन आप इसे उपलब्ध निःशुल्क परीक्षण के साथ एक्सप्लोर कर सकते हैं [यहाँ](https://releases.aspose.com/).

### प्रश्न 4: क्या Aspose.Imaging for .NET में कोई उन्नत इमेज प्रोसेसिंग सुविधाएं हैं?

A4: हां, Aspose.Imaging for .NET उन्नत छवि प्रसंस्करण सुविधाओं की एक विस्तृत श्रृंखला प्रदान करता है, जिसमें छवि का आकार बदलना, रोटेशन और बहुत कुछ शामिल है।

### प्रश्न 5: मैं Aspose.Imaging for .NET के लिए अधिक संसाधन और समर्थन कहां पा सकता हूं?

A5: आप दस्तावेज़ तक पहुँच सकते हैं [यहाँ](https://reference.aspose.com/imaging/net/) और समर्थन मांगें [Aspose.Imaging फ़ोरम](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}