---
title: .NET के लिए Aspose.Imaging में आयत बनाना
linktitle: .NET के लिए Aspose.Imaging में आयत बनाएं
second_title: Aspose.Imaging .NET इमेज प्रोसेसिंग एपीआई
description: .NET के लिए Aspose.Imaging में आयत बनाना सीखें - आपके .NET अनुप्रयोगों में छवि हेरफेर के लिए एक बहुमुखी उपकरण।
weight: 14
url: /hi/net/basic-drawing/draw-rectangle/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.Imaging में आयत बनाना

.NET अनुप्रयोगों में छवियां बनाना और उनमें हेरफेर करना एक जटिल कार्य हो सकता है, लेकिन .NET के लिए Aspose.Imaging की शक्ति के साथ, यह उल्लेखनीय रूप से सरल हो जाता है। इस चरण-दर-चरण मार्गदर्शिका में, हम आपको .NET के लिए Aspose.Imaging का उपयोग करके आयत बनाने की प्रक्रिया के बारे में बताएंगे। आप सीखेंगे कि एक छवि कैसे बनाएं, उसके गुण कैसे सेट करें, आयत कैसे बनाएं और अपना काम कैसे सहेजें। आइए गोता लगाएँ!

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

1.  .NET के लिए Aspose.Imaging: सुनिश्चित करें कि आपने .NET लाइब्रेरी के लिए Aspose.Imaging इंस्टॉल कर लिया है। यदि आपने पहले से नहीं किया है, तो आप इसे यहां से डाउनलोड कर सकते हैं[डाउनलोड पेज](https://releases.aspose.com/imaging/net/).

2. विकास परिवेश: आपके पास विज़ुअल स्टूडियो या किसी अन्य .NET विकास उपकरण के साथ एक विकास परिवेश स्थापित होना चाहिए।

अब, आइए चरण-दर-चरण ट्यूटोरियल शुरू करें।

## नामस्थान आयात करना

पहला कदम .NET के लिए Aspose.Imaging के साथ काम करने के लिए आवश्यक नामस्थान आयात करना है। यहां बताया गया है कि आप इसे कैसे करते हैं:

### चरण 1: नामस्थान आयात करें

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.ImageOptions;
using Aspose.Imaging.Sources;
```

उपरोक्त कोड में, हम Aspose.Imaging नेमस्पेस आयात कर रहे हैं, जो छवि हेरफेर के लिए आवश्यक कक्षाएं और विधियां प्रदान करते हैं।

## आयत बनाना

अब, आइए एक छवि पर आयत बनाने के लिए आगे बढ़ें।

### चरण 2: एक छवि बनाएं

```csharp
string dataDir = "Your Document Directory";  // अपनी दस्तावेज़ निर्देशिका के लिए पथ सेट करें
using (FileStream stream = new FileStream(dataDir, FileMode.Create))
{
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;
    saveOptions.Source = new StreamSource(stream);

    using (Image image = Image.Create(saveOptions, 100, 100))
    {
        // आयत बनाने के लिए आपका कोड यहां जाएगा
        image.Save();
    }
}
```

 इस चरण में, हम इसका एक उदाहरण बनाते हैं`Image` क्लास बनाएं और छवि निर्माण के लिए विभिन्न गुण सेट करें, जैसे कि`BitsPerPixel` और आउटपुट स्ट्रीम। फिर हम 100x100 पिक्सेल आकार की एक रिक्त छवि बनाते हैं।

### चरण 3: ग्राफ़िक्स प्रारंभ करें और आयत बनाएं

```csharp
Graphics graphic = new Graphics(image);
graphic.Clear(Color.Yellow);
graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));
graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));
```

 इस चरण में, हम a आरंभ करते हैं`Graphics` ऑब्जेक्ट, ग्राफ़िक्स सतह को पीले रंग की पृष्ठभूमि से साफ़ करें, और छवि पर विभिन्न रंगों और स्थितियों के साथ दो आयत बनाएं।

### चरण 4: छवि सहेजें

```csharp
image.Save();
```

अंत में, हम छवि को खींचे गए आयतों के साथ सहेजते हैं।

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा कि .NET के लिए Aspose.Imaging का उपयोग करके किसी छवि पर आयत कैसे बनाएं। इस गाइड में उल्लिखित चरणों का पालन करके, आप अपने .NET अनुप्रयोगों में आसानी से छवियां बना सकते हैं और उनमें हेरफेर कर सकते हैं। Aspose.Imaging छवि प्रबंधन को सरल बनाता है, जिससे यह डेवलपर्स के लिए एक शक्तिशाली उपकरण बन जाता है।

अब आप Aspose.Imaging का उपयोग करके अपने .NET प्रोजेक्ट में छवि हेरफेर को शामिल करने के लिए तैयार हैं। प्रयोग करना और आश्चर्यजनक दृश्य बनाना शुरू करें!

## अक्सर पूछे जाने वाले प्रश्न

### Q1: मैं .NET के लिए Aspose.Imaging से और कौन सी आकृतियाँ बना सकता हूँ?

A1: आप Aspose.Imaging लाइब्रेरी का उपयोग करके विभिन्न आकृतियाँ जैसे दीर्घवृत्त, रेखाएँ और वक्र बना सकते हैं।

### Q2: क्या मैं विंडोज़ और वेब अनुप्रयोगों दोनों में .NET के लिए Aspose.Imaging का उपयोग कर सकता हूँ?

A2: हाँ, .NET के लिए Aspose.Imaging का उपयोग विंडोज़ और वेब अनुप्रयोगों दोनों में किया जा सकता है, जो इसे विभिन्न प्रोजेक्ट प्रकारों के लिए बहुमुखी बनाता है।

### Q3: क्या .NET के लिए Aspose.Imaging एक निःशुल्क लाइब्रेरी है?

 A3: .NET के लिए Aspose.Imaging एक व्यावसायिक लाइब्रेरी है, लेकिन आप इसे निःशुल्क परीक्षण के साथ देख सकते हैं[यहाँ](https://releases.aspose.com/).

### Q4: क्या .NET के लिए Aspose.Imaging में कोई उन्नत इमेज प्रोसेसिंग सुविधाएँ हैं?

A4: हां, .NET के लिए Aspose.Imaging उन्नत छवि प्रसंस्करण सुविधाओं की एक विस्तृत श्रृंखला प्रदान करता है, जिसमें छवि का आकार बदलना, रोटेशन और बहुत कुछ शामिल है।

### Q5: मुझे .NET के लिए Aspose.Imaging के लिए अधिक संसाधन और समर्थन कहां मिल सकता है?

 A5: आप दस्तावेज़ तक पहुंच सकते हैं[यहाँ](https://reference.aspose.com/imaging/net/) और इस पर समर्थन मांगें[Aspose.इमेजिंग फोरम](https://forum.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
