---
date: 2026-04-28
description: Aspose.Imaging for Java का उपयोग करके TIFF को PNG में और अन्य रास्टर
  फ़ॉर्मैट्स में कैसे बदलें, सीखें। इमेज मैनिपुलेशन के लिए चरण‑दर‑चरण गाइड।
keywords:
- tiff to png java
- how to convert tiff
- Aspose.Imaging Java
linktitle: विभिन्न रास्टर फ़ॉर्मैट्स में फ्रेम सहेजना
second_title: Aspose.Imaging Java Image Processing API
title: tiff to png java – TIFF को PNG में बदलें और विभिन्न रास्टर फ़ॉर्मैट्स में फ्रेम
  सहेजें
url: /hi/java/document-conversion-and-processing/frame-saving-in-different-raster-formats/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# tiff to png java – TIFF को PNG में बदलें और विभिन्न रास्टर फ़ॉर्मेट्स में फ्रेम सहेजें

मल्टी‑पेज TIFF फ़ाइलों के साथ काम करना दस्तावेज‑भारी अनुप्रयोगों में एक सामान्य परिदृश्य है। यदि आपको **convert tiff to png** करना है—या व्यक्तिगत फ्रेम निकालकर उन्हें अन्य रास्टर फ़ॉर्मेट्स में संग्रहीत करना है—तो Aspose.Imaging for Java प्रक्रिया को सरल और तेज़ बनाता है। इस ट्यूटोरियल में हम TIFF को लोड करने, उसके फ्रेमों पर इटररेट करने, और प्रत्येक को PNG के रूप में सहेजने के सटीक चरणों से गुजरेंगे (बाद में आप आसानी से BMP या GIF में स्विच कर सकते हैं)। अंत तक आप देखेंगे कि कैसे **how to convert tiff** को समर्थित किसी भी रास्टर फ़ॉर्मेट में कुछ ही लाइनों के कोड से बदला जा सकता है।

## त्वरित उत्तर
- **“convert tiff to png” का क्या अर्थ है?** इसका मतलब है TIFF फ़ाइल के प्रत्येक पृष्ठ को निकालकर उसे PNG रास्टर इमेज के रूप में लिखना।  
- **कौन सी लाइब्रेरी यह संभालती है?** Aspose.Imaging for Java TIFF फ्रेम एक्सट्रैक्शन और रास्टर फ़ॉर्मेट कन्वर्ज़न के लिए पूर्ण समर्थन प्रदान करती है।  
- **क्या मुझे लाइसेंस चाहिए?** डेवलपमेंट के लिए फ्री ट्रायल काम करता है; प्रोडक्शन उपयोग के लिए पूर्ण लाइसेंस आवश्यक है।  
- **क्या मैं PNG के बजाय BMP या GIF में सहेज सकता हूँ?** हाँ—सिर्फ `PngOptions` को `BmpOptions` या `GifOptions` से बदल दें।  
- **कौन सा Java संस्करण आवश्यक है?** Java 8 या उससे ऊपर की सिफ़ारिश की जाती है।

## “convert tiff to png” क्या है?
TIFF को PNG में बदलना मल्टी‑पेज TIFF को डिकोड करने, प्रत्येक फ्रेम तक पहुँचने, और उस फ्रेम को PNG फ़ॉर्मेट में एन्कोड करने को शामिल करता है, जो लॉसलेस, वेब‑फ्रेंडली, और व्यापक रूप से समर्थित है।

## Aspose.Imaging for Java क्यों उपयोग करें?
- **व्यापक फ़ॉर्मेट समर्थन** – TIFF, PNG, JPEG, BMP, GIF, और कई अन्य को संभालता है।  
- **कोई नेटिव डिपेंडेंसी नहीं** – शुद्ध Java, किसी भी JVM प्रोजेक्ट में आसानी से इंटीग्रेट किया जा सकता है।  
- **उच्च प्रदर्शन** – बड़े इमेज और मल्टी‑पेज दस्तावेज़ों के लिए अनुकूलित।  
- **सरल API** – जटिल कन्वर्ज़न करने के लिए न्यूनतम कोड की आवश्यकता।

## यह क्यों महत्वपूर्ण है
कई लेगेसी सिस्टम स्कैन किए गए दस्तावेज़ों को मल्टी‑पेज TIFF के रूप में संग्रहीत करते हैं क्योंकि यह आर्काइव‑फ्रेंडली फ़ॉर्मेट है। आधुनिक वेब और मोबाइल एप्लिकेशन, हालांकि, तेज़ रेंडरिंग और थंबनेल जनरेशन के लिए PNG, BMP, या GIF को प्राथमिकता देते हैं। ऑन‑द‑फ़्लाई TIFF फ्रेम को बदलने से स्टोरेज लागत घटती है, लोड टाइम बेहतर होते हैं, और ब्राउज़र व डिवाइसों के बीच संगतता बढ़ती है।

## पूर्वापेक्षाएँ

1. **Java Development Environment** – सुनिश्चित करें कि JDK स्थापित है। यदि अभी तक नहीं किया है तो इसे [Oracle website](https://www.oracle.com/java/technologies/javase-downloads) से डाउनलोड करें।  
2. **Aspose.Imaging for Java Library** – API रेफ़रेंस के लिए [documentation](https://reference.aspose.com/imaging/java/) देखें। लाइब्रेरी को [download page](https://releases.aspose.com/imaging/java/) से प्राप्त करें। एक फ्री ट्रायल [here](https://releases.aspose.com/) उपलब्ध है, और पूर्ण लाइसेंस [here](https://purchase.aspose.com/buy) से खरीदा जा सकता है।  
3. **Sample TIFF Image** – प्रोसेसिंग के लिए एक मल्टी‑पेज TIFF तैयार रखें।

अब जब पूर्वापेक्षाएँ पूरी हो गई हैं, चलिए कोड में डुबकी लगाते हैं।

## Aspose.Imaging for Java का उपयोग करके TIFF को PNG में कैसे बदलें

### पैकेज इम्पोर्ट करें
पहले, आवश्यक Aspose.Imaging क्लासेज़ को इम्पोर्ट करें।

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
```

### चरण 1: TIFF इमेज लोड करें
डेटा डायरेक्टरी को इनिशियलाइज़ करें और स्रोत TIFF फ़ाइल को लोड करें।

```java
String dataDir = "Your Document Directory" + "ModifyingImages/";
try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "SampleTiff1.tiff")) {
```

### चरण 2: विभिन्न रास्टर फ़ॉर्मेट्स में फ्रेम सहेजें
प्रत्येक फ्रेम पर इटररेट करें और **save image as png** करें। **convert tiff to bmp** या **tiff to gif conversion** करने के लिए, बस `PngOptions` को `BmpOptions` या `GifOptions` से बदल दें।

```java
    int i = 0;
    for (TiffFrame tiffFrame : multiImage.getFrames()) {
        tiffFrame.save("Your Document Directory" + i + "_out.png", new PngOptions());
        i++;
    }
}
```

> **Pro tip:** जैसा दिखाया गया है, `try‑with‑resources` ब्लॉक को रखें ताकि प्रोसेसिंग के बाद TIFF फ़ाइल सही ढंग से डिस्पोज़ हो सके।

## सामान्य उपयोग केस
- **डॉक्यूमेंट आर्काइविंग:** स्कैन किए गए TIFF दस्तावेज़ों को वेब प्रीव्यू के लिए PNG में बदलें।  
- **थंबनेल जनरेशन:** TIFF के पहले फ्रेम को निकालें और उसे छोटा PNG थंबनेल के रूप में सहेजें।  
- **फ़ॉर्मेट माइग्रेशन:** लेगेसी TIFF एसेट्स को BMP या GIF जैसे आधुनिक फ़ॉर्मेट में माइग्रेट करें ताकि पुराने सिस्टमों के साथ संगतता बनी रहे।

## ट्रबलशूटिंग और टिप्स
- **Missing frames:** सुनिश्चित करें कि स्रोत TIFF वास्तव में कई पृष्ठों वाला है; डिबग करने के लिए `multiImage.getFrames().size()` का उपयोग करें।  
- **Out‑of‑memory errors:** जैसा दिखाया गया है, पूरे फ़ाइल को मेमोरी में लोड करने के बजाय पेज‑बाय‑पेज प्रोसेस करें।  
- **Quality control:** PNG लॉसलेस है; यदि आपको छोटे फ़ाइल चाहिए तो JPEG विकल्पों के साथ क्वालिटी सेटिंग्स का उपयोग करें।

## अक्सर पूछे जाने वाले प्रश्न

**Q1: Aspose.Imaging for Java में फ्रेम सहेजने के लिए कौन से रास्टर फ़ॉर्मेट समर्थित हैं?**  
A1: Aspose.Imaging for Java कई रास्टर फ़ॉर्मेट्स को सपोर्ट करता है, जिसमें PNG, JPEG, BMP, GIF, और अधिक शामिल हैं। आप अपनी एप्लिकेशन की जरूरतों के अनुसार फ़ॉर्मेट चुन सकते हैं।

**Q2: क्या मैं Aspose.Imaging for Java का उपयोग करके अन्य इमेज ऑपरेशन्स भी कर सकता हूँ?**  
A2: हाँ, Aspose.Imaging for Java इमेज मैनिपुलेशन के लिए व्यापक फीचर्स प्रदान करता है, जिसमें रिसाइज़िंग, क्रॉपिंग, और विभिन्न फ़िल्टर व इफ़ेक्ट्स लागू करना शामिल है। यह आपके सभी इमेज प्रोसेसिंग आवश्यकताओं के लिए एक बहुमुखी टूल है।

**Q3: मैं Aspose.Imaging for Java के लिए पूर्ण लाइसेंस कैसे प्राप्त करूँ?**  
A: Aspose.Imaging for Java के लिए पूर्ण लाइसेंस खरीदने हेतु [purchase page](https://purchase.aspose.com/buy) पर जाएँ। वहाँ आपके प्रोजेक्ट के अनुसार विभिन्न लाइसेंस विकल्प उपलब्ध हैं।

**Q4: क्या Aspose.Imaging for Java के लिए फ्री ट्रायल उपलब्ध है?**  
A: हाँ, आप [releases page](https://releases.aspose.com/) से Aspose.Imaging for Java का फ्री ट्रायल एक्सेस कर सकते हैं। यह ट्रायल आपको लाइब्रेरी की क्षमताओं को खरीदारी से पहले एक्सप्लोर करने की अनुमति देता है।

**Q5: मैं Aspose.Imaging for Java के लिए सपोर्ट या सहायता कहाँ प्राप्त कर सकता हूँ?**  
A: किसी भी प्रश्न, समस्या, या सहायता के लिए आप [Aspose Imaging forum](https://forum.aspose.com/) पर जा सकते हैं। कम्युनिटी और सपोर्ट टीम आपकी मदद के लिए उपलब्ध है।

---

**Last Updated:** 2026-04-28  
**Tested With:** Aspose.Imaging for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}