---
date: 2025-12-20
description: Aspose.Imaging for Java का उपयोग करके TIFF को PNG में कैसे बदलें और छवि
  को PNG, BMP या GIF के रूप में सहेजें, सीखें। छवि संशोधन के लिए चरण‑दर‑चरण मार्गदर्शिका।
linktitle: Frame Saving in Different Raster Formats
second_title: Aspose.Imaging Java Image Processing API
title: TIFF को PNG में कैसे बदलें और विभिन्न रास्टर फ़ॉर्मैट में फ्रेम सहेजें
url: /hi/java/document-conversion-and-processing/frame-saving-in-different-raster-formats/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# TIFF को PNG में बदलें और विभिन्न रास्टर फ़ॉर्मैट्स में फ्रेम्स सहेजें

बहु‑पृष्ठीय TIFF फ़ाइलों के साथ काम करना दस्तावेज‑भारी अनुप्रयोगों में एक सामान्य परिदृश्य है। यदि आपको **convert tiff to png** करना है—या व्यक्तिगत फ्रेम निकालकर उन्हें अन्य रास्टर फ़ॉर्मैट्स में संग्रहीत करना है—तो Aspose.Imaging for Java प्रक्रिया को सरल और तेज़ बनाता है। इस ट्यूटोरियल में हम TIFF को लोड करने, उसके फ्रेम्स पर इटररेट करने, और प्रत्येक को PNG के रूप में सहेजने के सटीक चरणों को देखेंगे (आप बाद में आसानी से BMP या GIF में बदल सकते हैं)।

## त्वरित उत्तर

- **What does “convert tiff to png” mean?** यह एक TIFF फ़ाइल के प्रत्येक पृष्ठ को निकालकर उसे PNG रास्टर इमेज के रूप में लिखने का अर्थ है।  
- **Which library handles this?** Aspose.Imaging for Java TIFF फ्रेम एक्सट्रैक्शन और रास्टर फ़ॉर्मैट रूपांतरण के लिए पूर्ण समर्थन प्रदान करता है।  
- **Do I need a license?** एक फ्री ट्रायल विकास के लिए काम करता है; उत्पादन उपयोग के लिए पूर्ण लाइसेंस आवश्यक है।  
- **Can I save to BMP or GIF instead of PNG?** हाँ—सिर्फ `PngOptions` को `BmpOptions` या `GifOptions` से बदलें।  
- **What Java version is required?** Java 8 या उससे ऊपर की संस्करण की सिफ़ारिश की जाती है।

## “convert tiff to png” क्या है?

TIFF को PNG में बदलना बहु‑पृष्ठीय TIFF को डिकोड करने, प्रत्येक फ्रेम तक पहुँचने, और उस फ्रेम को PNG फ़ॉर्मैट में एन्कोड करने को शामिल करता है, जो लॉसलेस, वेब‑फ्रेंडली, और व्यापक रूप से समर्थित है।

## Aspose.Imaging for Java का उपयोग क्यों करें?

- **Broad format support** – TIFF, PNG, JPEG, BMP, GIF, और कई अन्य फ़ॉर्मैट्स को संभालता है।  
- **No native dependencies** – शुद्ध Java, किसी भी JVM प्रोजेक्ट में एकीकृत करना आसान।  
- **High performance** – बड़े इमेज और बहु‑पृष्ठीय दस्तावेज़ों के लिए अनुकूलित।  
- **Simple API** – जटिल रूपांतरण करने के लिए न्यूनतम कोड आवश्यक।

## पूर्वापेक्षाएँ

1. **Java Development Environment** – सुनिश्चित करें कि JDK स्थापित है। यदि अभी तक नहीं किया है तो इसे [Oracle website](https://www.oracle.com/java/technologies/javase-downloads) से डाउनलोड करें।  
2. **Aspose.Imaging for Java Library** – API रेफ़रेंस के लिए [documentation](https://reference.aspose.com/imaging/java/) देखें। लाइब्रेरी को [download page](https://releases.aspose.com/imaging/java/) से प्राप्त करें। एक फ्री ट्रायल [here](https://releases.aspose.com/) पर उपलब्ध है, और पूर्ण लाइसेंस [here](https://purchase.aspose.com/buy) से खरीदा जा सकता है।  
3. **Sample TIFF Image** – प्रोसेसिंग के लिए एक बहु‑पृष्ठीय TIFF तैयार रखें।

अब जब पूर्वापेक्षाएँ पूरी हो गई हैं, चलिए कोड में डुबकी लगाते हैं।

## Aspose.Imaging for Java का उपयोग करके TIFF को PNG में कैसे बदलें

### पैकेज इम्पोर्ट करें

सबसे पहले, आवश्यक Aspose.Imaging क्लासेस को इम्पोर्ट करें।

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

### चरण 2: विभिन्न रास्टर फ़ॉर्मैट्स में फ्रेम्स सहेजें

प्रत्येक फ्रेम पर इटररेट करें और **save image as png**। **convert tiff to bmp** करने या **tiff to gif conversion** करने के लिए, बस `PngOptions` को `BmpOptions` या `GifOptions` से बदलें।

```java
    int i = 0;
    for (TiffFrame tiffFrame : multiImage.getFrames()) {
        tiffFrame.save("Your Document Directory" + i + "_out.png", new PngOptions());
        i++;
    }
}
```

> **प्रो टिप:** दिखाए गए अनुसार `try‑with‑resources` ब्लॉक को रखें ताकि प्रोसेसिंग के बाद TIFF फ़ाइल सही ढंग से डिस्पोज़ हो सके।

## सामान्य उपयोग मामलों

- **Document archiving:** स्कैन किए गए TIFF दस्तावेज़ों को वेब प्रीव्यू के लिए PNG में बदलें।  
- **Thumbnail generation:** TIFF के पहले फ्रेम को निकालें और उसे छोटे PNG थंबनेल के रूप में सहेजें।  
- **Format migration:** लेगेसी TIFF एसेट्स को BMP या GIF जैसे आधुनिक फ़ॉर्मैट्स में माइग्रेट करें ताकि पुराने सिस्टम्स के साथ संगतता बनी रहे।

## समस्या निवारण और टिप्स

- **Missing frames:** सुनिश्चित करें कि स्रोत TIFF वास्तव में कई पृष्ठों को शामिल करता है; डिबग करने के लिए `multiImage.getFrames().size()` का उपयोग करें।  
- **Out‑of‑memory errors:** दिखाए अनुसार बड़े TIFF को पेज‑बाय‑पेज प्रोसेस करें, पूरे फ़ाइल को मेमोरी में लोड करने के बजाय।  
- **Quality control:** PNG लॉसलेस है; यदि आपको छोटे फ़ाइल चाहिए तो क्वालिटी सेटिंग्स के साथ JPEG विकल्पों पर विचार करें।

## अक्सर पूछे जाने वाले प्रश्न

**Q1: Aspose.Imaging for Java में फ्रेम सहेजने के लिए समर्थित रास्टर फ़ॉर्मैट्स कौन‑से हैं?**  
A1: Aspose.Imaging for Java PNG, JPEG, BMP, GIF और अन्य सहित रास्टर फ़ॉर्मैट्स की विस्तृत श्रृंखला को सपोर्ट करता है। आप अपने एप्लिकेशन की आवश्यकताओं के अनुसार सबसे उपयुक्त फ़ॉर्मैट चुन सकते हैं।

**Q2: क्या मैं Aspose.Imaging for Java का उपयोग करके अन्य इमेज ऑपरेशन्स कर सकता हूँ?**  
A2: हाँ, Aspose.Imaging for Java इमेज मैनिपुलेशन के लिए रिसाइज़िंग, क्रॉपिंग, और विभिन्न फ़िल्टर व इफ़ेक्ट्स लागू करने सहित सुविधाओं का व्यापक सेट प्रदान करता है। यह आपके सभी इमेज प्रोसेसिंग आवश्यकताओं के लिए एक बहुमुखी टूल है।

**Q3: Aspose.Imaging for Java के लिए पूर्ण लाइसेंस कैसे प्राप्त करूँ?**  
A3: Aspose.Imaging for Java के लिए पूर्ण लाइसेंस खरीदने के लिए, [purchase page](https://purchase.aspose.com/buy) पर जाएँ। आपको अपने प्रोजेक्ट के अनुसार विभिन्न लाइसेंसिंग विकल्प मिलेंगे।

**Q4: क्या Aspose.Imaging for Java के लिए फ्री ट्रायल उपलब्ध है?**  
A4: हाँ, आप [releases page](https://releases.aspose.com/) से Aspose.Imaging for Java का फ्री ट्रायल एक्सेस कर सकते हैं। यह ट्रायल आपको लाइब्रेरी की क्षमताओं को खरीदारी से पहले जांचने की अनुमति देता है।

**Q5: Aspose.Imaging for Java के लिए समर्थन या सहायता कहाँ प्राप्त कर सकता हूँ?**  
A5: Aspose.Imaging for Java से संबंधित किसी भी प्रश्न, समस्या या सहायता के लिए आप [Aspose Imaging forum](https://forum.aspose.com/) पर जा सकते हैं। समुदाय और सपोर्ट टीम आपकी मदद के लिए उपलब्ध हैं।

**अंतिम अपडेट:** 2025-12-20  
**परीक्षित संस्करण:** Aspose.Imaging for Java 24.11  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}