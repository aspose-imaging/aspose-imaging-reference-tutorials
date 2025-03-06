---
title: जावा के लिए Aspose.Imaging के साथ CMX को PNG में बदलें
linktitle: सीएमएक्स को पीएनजी छवि में बदलें
second_title: Aspose.Imaging जावा इमेज प्रोसेसिंग एपीआई
description: जावा के लिए Aspose.Imaging का उपयोग करके CMX को PNG छवियों में परिवर्तित करना सीखें। निर्बाध छवि रूपांतरण के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
weight: 10
url: /hi/java/image-conversion-and-optimization/convert-cmx-to-png-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा के लिए Aspose.Imaging के साथ CMX को PNG में बदलें

क्या आप जावा का उपयोग करके सीएमएक्स फ़ाइलों को पीएनजी छवियों में परिवर्तित करना चाह रहे हैं? जावा के लिए Aspose.Imaging एक शक्तिशाली और बहुमुखी उपकरण है जो आपको इसे आसानी से हासिल करने में मदद कर सकता है। इस चरण-दर-चरण मार्गदर्शिका में, हम आपको जावा के लिए Aspose.Imaging का उपयोग करके CMX फ़ाइलों को PNG छवियों में परिवर्तित करने की प्रक्रिया के बारे में बताएंगे।

## आवश्यक शर्तें

आरंभ करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

1. जावा विकास पर्यावरण

आपके सिस्टम पर एक जावा डेवलपमेंट वातावरण स्थापित होना चाहिए। सुनिश्चित करें कि आपके पास नवीनतम जावा डेवलपमेंट किट (जेडीके) स्थापित है।

2. जावा के लिए Aspose.Imaging

 जावा के लिए Aspose.Imaging डाउनलोड और इंस्टॉल करें। आप आवश्यक पैकेज और इंस्टॉलेशन निर्देश यहां पा सकते हैं[यहाँ](https://releases.aspose.com/imaging/java/).

3. सीएमएक्स फ़ाइलें

आपको सीएमएक्स फ़ाइलों की आवश्यकता होगी जिन्हें आप पीएनजी छवियों में कनवर्ट करना चाहते हैं। सुनिश्चित करें कि आपके पास ये फ़ाइलें एक निर्देशिका में संग्रहीत हैं।

## पैकेज आयात करें

रूपांतरण आरंभ करने के लिए, आपको Aspose.Imaging से आवश्यक पैकेज आयात करने होंगे। यहां बताया गया है कि आप यह कैसे कर सकते हैं:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.CmxRasterizationOptions;
import com.aspose.imaging.system.drawing.SmoothingMode;
import com.aspose.imaging.positioning.PositioningTypes;
```

## चरण 1: अपनी डेटा निर्देशिका सेट करें

आपको अपनी डेटा निर्देशिका का पथ निर्दिष्ट करना होगा जहां आपकी सीएमएक्स फ़ाइलें स्थित हैं। प्रतिस्थापित करें`"Your Document Directory" + "CMX/"` आपकी निर्देशिका के वास्तविक पथ के साथ।

```java
String dataDir = "Your Document Directory" + "CMX/";
```

## चरण 2: सीएमएक्स फाइलों की सूची तैयार करें

सीएमएक्स फ़ाइल नामों की एक सरणी बनाएं जिन्हें आप पीएनजी छवियों में कनवर्ट करना चाहते हैं। सुनिश्चित करें कि फ़ाइल नाम सटीक हैं और आपकी निर्देशिका की फ़ाइलों से मेल खाते हैं।

```java
String[] fileNames = new String[] {
    "Rectangle.cmx",
    "Rectangle+Fill.cmx",
    "Ellipse.cmx",
    "Ellipse+fill.cmx",
    "brushes.cmx",
    "outlines.cmx",
    "order.cmx",
    "many_images.cmx"
};
```

## चरण 3: सीएमएक्स को पीएनजी में बदलें

अब, आइये रूपांतरण प्रक्रिया पर गौर करें। सूची में प्रत्येक सीएमएक्स फ़ाइल के लिए, हम पीएनजी प्रारूप में रूपांतरण करेंगे।

```java
for (String fileName : fileNames) {
    try (Image image = Image.load(dataDir + fileName)) {
        CmxRasterizationOptions cmxRasterizationOptions = new CmxRasterizationOptions();
        cmxRasterizationOptions.setPositioning(PositioningTypes.DefinedByDocument);
        cmxRasterizationOptions.setSmoothingMode(SmoothingMode.AntiAlias);
        PngOptions options = new PngOptions();
        options.setVectorRasterizationOptions(cmxRasterizationOptions);
        image.save("Your Document Directory" + fileName + ".docpage.png", options);
    }
}
```

अपनी सूची में प्रत्येक CMX फ़ाइल के लिए इस चरण को दोहराएँ। परिवर्तित पीएनजी छवियां निर्दिष्ट निर्देशिका में सहेजी जाएंगी।

बधाई हो! आपने Java के लिए Aspose.Imaging का उपयोग करके CMX फ़ाइलों को सफलतापूर्वक PNG छवियों में परिवर्तित कर लिया है। अब आप इन पीएनजी छवियों का उपयोग विभिन्न उद्देश्यों के लिए कर सकते हैं, जैसे उन्हें किसी वेबसाइट पर प्रदर्शित करना या उन्हें अपने दस्तावेज़ों में शामिल करना।

## निष्कर्ष

इस व्यापक गाइड में, हमने पता लगाया है कि सीएमएक्स फ़ाइलों को पीएनजी छवियों में परिवर्तित करने के लिए जावा के लिए Aspose.Imaging का उपयोग कैसे करें। सही पूर्वापेक्षाओं के साथ और चरण-दर-चरण निर्देशों का पालन करके, आप इस रूपांतरण को कुशलतापूर्वक कर सकते हैं और अपने जावा अनुप्रयोगों में अपनी छवि प्रसंस्करण क्षमताओं को बढ़ा सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: जावा के लिए Aspose.Imaging क्या है?

A1: जावा के लिए Aspose.Imaging एक जावा लाइब्रेरी है जो डेवलपर्स को विभिन्न छवि प्रारूपों के साथ काम करने, छवि संपादन और रूपांतरण कार्य करने की अनुमति देती है।

### Q2: मैं जावा के लिए Aspose.Imaging के लिए दस्तावेज़ कहां पा सकता हूं?

 ए2: आप जावा के लिए Aspose.Imaging के लिए दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/imaging/java/). यह पुस्तकालय की विशेषताओं और कार्यों पर गहन जानकारी प्रदान करता है।

### Q3: क्या जावा के लिए Aspose.Imaging का कोई निःशुल्क परीक्षण उपलब्ध है?

 उ3: हां, आप जावा के लिए Aspose.Imaging का निःशुल्क परीक्षण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/). यह आपको खरीदारी करने से पहले लाइब्रेरी की क्षमताओं का पता लगाने की अनुमति देता है।

### Q4: मैं जावा के लिए Aspose.Imaging के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

A4: आप जावा के लिए Aspose.Imaging पर जाकर एक अस्थायी लाइसेंस प्राप्त कर सकते हैं[इस लिंक](https://purchase.aspose.com/temporary-license/). यह अल्पकालिक उपयोग के लिए एक सुविधाजनक विकल्प है।

### Q5: CMX को PNG छवियों में परिवर्तित करने के लिए कुछ सामान्य उपयोग के मामले क्या हैं?

A5: सामान्य उपयोग के मामलों में वेब ग्राफिक्स बनाना, मुद्रण के लिए छवियां तैयार करना और विभिन्न अनुप्रयोगों में उपयोग के लिए वेक्टर ग्राफिक्स को परिवर्तित करना शामिल है।
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
