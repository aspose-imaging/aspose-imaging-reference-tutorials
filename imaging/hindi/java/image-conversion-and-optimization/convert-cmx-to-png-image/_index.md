---
"description": "Aspose.Imaging for Java का उपयोग करके CMX को PNG छवियों में परिवर्तित करना सीखें। सहज छवि रूपांतरण के लिए हमारे चरण-दर-चरण मार्गदर्शिका का पालन करें।"
"linktitle": "CMX को PNG छवि में बदलें"
"second_title": "Aspose.Imaging जावा इमेज प्रोसेसिंग API"
"title": "Java के लिए Aspose.Imaging के साथ CMX को PNG में बदलें"
"url": "/hi/java/image-conversion-and-optimization/convert-cmx-to-png-image/"
"weight": 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Java के लिए Aspose.Imaging के साथ CMX को PNG में बदलें

क्या आप Java का उपयोग करके CMX फ़ाइलों को PNG छवियों में बदलना चाहते हैं? Aspose.Imaging for Java एक शक्तिशाली और बहुमुखी उपकरण है जो आपको इसे आसानी से प्राप्त करने में मदद कर सकता है। इस चरण-दर-चरण मार्गदर्शिका में, हम आपको Aspose.Imaging for Java का उपयोग करके CMX फ़ाइलों को PNG छवियों में बदलने की प्रक्रिया से परिचित कराएँगे।

## आवश्यक शर्तें

आरंभ करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

1. जावा विकास पर्यावरण

आपके सिस्टम पर जावा डेवलपमेंट एनवायरनमेंट सेट अप होना चाहिए। सुनिश्चित करें कि आपके पास नवीनतम जावा डेवलपमेंट किट (JDK) स्थापित है।

2. जावा के लिए Aspose.Imaging

Aspose.Imaging for Java डाउनलोड करें और इंस्टॉल करें। आप आवश्यक पैकेज और इंस्टॉलेशन निर्देश यहाँ पा सकते हैं [यहाँ](https://releases.aspose.com/imaging/java/).

3. CMX फ़ाइलें

आपको CMX फ़ाइलों की आवश्यकता होगी जिन्हें आप PNG छवियों में बदलना चाहते हैं। सुनिश्चित करें कि आपने इन फ़ाइलों को किसी निर्देशिका में संग्रहीत किया है।

## पैकेज आयात करें

रूपांतरण शुरू करने के लिए, आपको Aspose.Imaging से आवश्यक पैकेज आयात करने होंगे। आप यह कैसे कर सकते हैं:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.CmxRasterizationOptions;
import com.aspose.imaging.system.drawing.SmoothingMode;
import com.aspose.imaging.positioning.PositioningTypes;
```

## चरण 1: अपनी डेटा निर्देशिका सेट करें

आपको अपनी डेटा निर्देशिका का पथ निर्दिष्ट करना होगा जहाँ आपकी CMX फ़ाइलें स्थित हैं। `"Your Document Directory" + "CMX/"` आपकी निर्देशिका के वास्तविक पथ के साथ.

```java
String dataDir = "Your Document Directory" + "CMX/";
```

## चरण 2: CMX फ़ाइलों की सूची तैयार करें

CMX फ़ाइल नामों की एक सरणी बनाएँ जिन्हें आप PNG छवियों में बदलना चाहते हैं। सुनिश्चित करें कि फ़ाइल नाम सटीक हैं और आपकी निर्देशिका में फ़ाइलों से मेल खाते हैं।

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

## चरण 3: CMX को PNG में बदलें

अब, आइए रूपांतरण प्रक्रिया में गोता लगाएँ। सूची में प्रत्येक CMX फ़ाइल के लिए, हम PNG प्रारूप में रूपांतरण करेंगे।

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

अपनी सूची में प्रत्येक CMX फ़ाइल के लिए इस चरण को दोहराएँ। परिवर्तित PNG छवियाँ निर्दिष्ट निर्देशिका में सहेजी जाएँगी।

बधाई हो! आपने Aspose.Imaging for Java का उपयोग करके CMX फ़ाइलों को PNG छवियों में सफलतापूर्वक परिवर्तित कर लिया है। अब आप इन PNG छवियों का उपयोग विभिन्न उद्देश्यों के लिए कर सकते हैं, जैसे कि उन्हें किसी वेबसाइट पर प्रदर्शित करना या उन्हें अपने दस्तावेज़ों में शामिल करना।

## निष्कर्ष

इस व्यापक गाइड में, हमने CMX फ़ाइलों को PNG छवियों में बदलने के लिए Aspose.Imaging for Java का उपयोग करने का तरीका खोजा है। सही पूर्वापेक्षाएँ रखने और चरण-दर-चरण निर्देशों का पालन करके, आप कुशलतापूर्वक यह रूपांतरण कर सकते हैं और अपने Java अनुप्रयोगों में अपनी छवि प्रसंस्करण क्षमताओं को बढ़ा सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: Java के लिए Aspose.Imaging क्या है?

A1: Aspose.Imaging for Java एक जावा लाइब्रेरी है जो डेवलपर्स को विभिन्न छवि प्रारूपों के साथ काम करने, छवि संपादन और रूपांतरण कार्य करने की अनुमति देती है।

### प्रश्न 2: मैं Aspose.Imaging for Java के लिए दस्तावेज़ कहां पा सकता हूं?

A2: आप Java के लिए Aspose.Imaging का दस्तावेज़ पा सकते हैं [यहाँ](https://reference.aspose.com/imaging/java/)यह पुस्तकालय की विशेषताओं और कार्यों पर गहन जानकारी प्रदान करता है।

### प्रश्न 3: क्या Aspose.Imaging for Java के लिए कोई निःशुल्क परीक्षण उपलब्ध है?

A3: हाँ, आप Java के लिए Aspose.Imaging का निःशुल्क परीक्षण प्राप्त कर सकते हैं [यहाँ](https://releases.aspose.com/)यह आपको खरीदारी करने से पहले पुस्तकालय की क्षमताओं का पता लगाने की अनुमति देता है।

### प्रश्न 4: मैं Aspose.Imaging for Java के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

A4: आप Aspose.Imaging for Java के लिए अस्थायी लाइसेंस प्राप्त करने के लिए यहाँ जाएँ [इस लिंक](https://purchase.aspose.com/temporary-license/)यह अल्पकालिक उपयोग के लिए एक सुविधाजनक विकल्प है।

### प्रश्न 5: CMX को PNG छवियों में परिवर्तित करने के कुछ सामान्य उपयोग क्या हैं?

A5: सामान्य उपयोग के मामलों में वेब ग्राफिक्स बनाना, मुद्रण के लिए चित्र तैयार करना, और विभिन्न अनुप्रयोगों में उपयोग के लिए वेक्टर ग्राफिक्स को परिवर्तित करना शामिल है।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}