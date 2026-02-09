---
date: 2026-02-09
description: Aspose.Imaging for .NET का उपयोग करके आर्क कैसे बनाएं, जिसमें BMP फ़ाइल
  को सहेजना, इमेज का आकार सेट करना और ग्राफ़िक्स बैकग्राउंड सेट करना शामिल है। BMP
  इमेज बनाने के लिए चरण-दर-चरण गाइड।
linktitle: Draw Arc in Aspose.Imaging for .NET
second_title: Aspose.Imaging .NET Image Processing API
title: Aspose.Imaging for .NET के साथ आर्क कैसे बनाएं
url: /hi/net/basic-drawing/draw-arc/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for .NET के साथ आर्क कैसे बनाएं

## त्वरित उत्तर
- **कोड क्या उत्पन्न करता है?** 100 × 100 पिक्सेल BMP इमेज जिसमें पीला बैकग्राउंड और काली आर्क है।  
- **कौनसी लाइब्रेरी उपयोग की गई है?** Aspose.Imaging for .NET।  
- **क्या मुझे लाइसेंस चाहिए?** विकास के लिए फ्री ट्रायल काम करता है; उत्पादन के लिए कमर्शियल लाइसेंस आवश्यक है।  
- **क्या मैं इमेज का आकार बदल सकता हूँ?** हाँ – `Image.Create` कॉल में चौड़ाई और ऊँचाई पैरामीटर को बदलें।  
- **क्या आउटपुट फॉर्मेट स्थिर है?** उदाहरण BMP फ़ाइल सहेजता है, लेकिन Aspose.Imaging द्वारा समर्थित कोई भी फॉर्मेट उपयोग किया जा सकता है।

## Aspose.Imaging में “आर्क कैसे बनाएं” क्या है?
आर्क बनाना का अर्थ है एक वक्र रेखा खंड को रेंडर करना जो बाउंडिंग रेक्टेंगल, प्रारंभिक कोण, और स्वेप कोण द्वारा परिभाषित होता है। Aspose.Imaging `Graphics.DrawArc` मेथड प्रदान करता है, जो आपको **draw arc with pen** करने और हर दृश्य पहलू को नियंत्रित करने देता है।

## इस कार्य के लिए Aspose.Imaging क्यों उपयोग करें?
- **Full control** इमेज डाइमेंशन, कलर डेप्थ, और फ़ाइल फॉर्मेट पर।  
- **No external dependencies** – सब कुछ शुद्ध .NET पर चलता है।  
- **High performance** सर्वर साइड पर बड़ी संख्या में ग्राफ़िक्स उत्पन्न करने के लिए।  

## पूर्वापेक्षाएँ

कोड में जाने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **Aspose.Imaging for .NET** – आधिकारिक साइट से [यहाँ](https://releases.aspose.com/imaging/net/) डाउनलोड करें।  
2. **एक .NET विकास पर्यावरण** (Visual Studio, VS Code, या कोई भी C# कंपाइलर)।  

अब जब हमारी पूर्वापेक्षाएँ तैयार हैं, चलिए ड्रॉ करना शुरू करते हैं!

## आवश्यक नेमस्पेसेस आयात करना

Aspose.Imaging के साथ काम करने के लिए आपको संबंधित नेमस्पेसेस को स्कोप में लाना होगा:

### चरण 1: नेमस्पेसेस आयात करें

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Brushes;
using Aspose.Imaging.FileFormats.Bmp;
using Aspose.Imaging.Sources;
using System;
using System.Drawing;
using System.IO;
```

ये `using` स्टेटमेंट्स आपको इमेज निर्माण, ग्राफ़िक्स हैंडलिंग, और फ़ाइल I/O क्लासेज़ तक पहुँच प्रदान करते हैं।

## Aspose.Imaging for .NET के साथ आर्क कैसे बनाएं

हम प्रक्रिया को तीन स्पष्ट चरणों में विभाजित करेंगे: इमेज बनाना, ग्राफ़िक्स सतह तैयार करना, और अंत में आर्क बनाना।

### चरण 1: इमेज सेट अप करें (इमेज आकार सेट करें और BMP इमेज जनरेट करें)

```csharp
// Specify the directory where you want to save the image
string dataDir = "Your Document Directory";

// Create an instance of FileStream to save the image
using (FileStream stream = new FileStream(dataDir + "DrawingArc_out.bmp", FileMode.Create))
{
    // Create an instance of BmpOptions and set its properties
    BmpOptions saveOptions = new BmpOptions();
    saveOptions.BitsPerPixel = 32;

    // Set the source for BmpOptions and create an instance of Image
    saveOptions.Source = new StreamSource(stream);
    using (Image image = Image.Create(saveOptions, 100, 100))
    {
```

यहाँ हम इमेज आकार को 100 × 100 पिक्सेल पर **set image size** करते हैं और BMP विकल्प कॉन्फ़िगर करते हैं। `FileStream` यह सुनिश्चित करता है कि हम इच्छित स्थान पर **save BMP file** कर सकें।

### चरण 2: ग्राफ़िक्स इनिशियलाइज़ करें और ग्राफ़िक्स बैकग्राउंड सेट करें

```csharp
        // Create and initialize an instance of Graphics class and clear the graphics surface
        Graphics graphic = new Graphics(image);
        graphic.Clear(Color.Yellow);
```

`Graphics` ऑब्जेक्ट हमें इमेज पर पेंट करने देता है। `Clear(Color.Yellow)` कॉल करके हम **set graphics background** को चमकीले पीले रंग में सेट करते हैं, जिससे आर्क उभर कर दिखे।

### चरण 3: आर्क पैरामीटर परिभाषित करें और Pen के साथ आर्क बनाएं

```csharp
        // Define the parameters for the arc
        int width = 100;
        int height = 200;
        int startAngle = 45;
        int sweepAngle = 270;

        // Draw the arc
        graphic.DrawArc(new Pen(Color.Black), 0, 0, width, height, startAngle, sweepAngle);

        // Save the changes
        image.Save();
    }
    stream.Close();
}
```

- `width` और `height` बाउंडिंग रेक्टेंगल को परिभाषित करते हैं, प्रभावी रूप से आर्क के लिए **set image size** तय करते हैं।  
- `Pen` ऑब्जेक्ट वह है जो हमें काले रंग में **draw arc with pen** करने देता है।  
- ड्रॉ करने के बाद, `image.Save()` **BMP file** को डिस्क पर लिखता है।

## सामान्य समस्याएँ और टिप्स

- **Arc दिखाई नहीं दे रहा?** सुनिश्चित करें कि पेन का रंग बैकग्राउंड के साथ कंट्रास्ट में है (जैसे, पीले पर काला)।  
- **गलत डाइमेंशन?** याद रखें कि आर्क का बाउंडिंग रेक्टेंगल इमेज से बड़ा हो सकता है; `width`/`height` या इमेज आकार को उसी अनुसार समायोजित करें।  
- **परफ़ॉर्मेंस टिप:** यदि आपको एक ही इमेज पर कई शैप्स ड्रॉ करने हैं तो एक ही `Graphics` इंस्टेंस को पुनः उपयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: Aspose.Imaging for .NET की दस्तावेज़ीकरण कहाँ मिल सकती है?

A1: आप Aspose.Imaging for .NET के व्यापक जानकारी के लिए दस्तावेज़ीकरण [यहाँ](https://reference.aspose.com/imaging/net/) देख सकते हैं।

### प्रश्न 2: Aspose.Imaging for .NET कैसे डाउनलोड करें?

A2: आप वेबसाइट से Aspose.Imaging for . .NET [यहाँ](https://releases.aspose.com/imaging/net/) डाउनलोड कर सकते हैं।

### प्रश्न 3: क्या Aspose.Imaging for .NET के लिए फ्री ट्रायल उपलब्ध है?

A3: हाँ, आप Aspose.Imaging for .NET को आज़माने के लिए फ्री ट्रायल संस्करण [यहाँ](https://releases.aspose.com/) प्राप्त कर सकते हैं।

### प्रश्न 4: क्या Aspose.Imaging for .NET के लिए अस्थायी लाइसेंस चाहिए?

A4: यदि आपको अस्थायी लाइसेंस चाहिए, तो आप इसे [यहाँ](https://purchase.aspose.com/temporary-license/) प्राप्त कर सकते हैं।

### प्रश्न 5: Aspose.Imaging for .NET के बारे में समर्थन या प्रश्न कहाँ पूछ सकते हैं?

A5: आप समर्थन और चर्चा के लिए Aspose.Imaging फ़ोरम [यहाँ](https://forum.aspose.com/) पर जा सकते हैं।

---

**अंतिम अपडेट:** 2026-02-09  
**परीक्षित संस्करण:** Aspose.Imaging 24.11 for .NET  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}