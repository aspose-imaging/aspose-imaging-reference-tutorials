---
date: 2026-01-17
description: जानेँ कि Aspose.Imaging के साथ जावा में मीडियन फ़िल्टर का उपयोग करके
  इमेज़ शोर को कैसे हटाया जाए। यह चरण‑दर‑चरण ट्यूटोरियल इमेज़ डिनॉइज़िंग के लिए मीडियन
  और विंर फ़िल्टर लागू करने को कवर करता है।
linktitle: Median Filter Java – Apply Median and Wiener Filters
second_title: Aspose.Imaging Java Image Processing API
title: मीडियन फ़िल्टर जावा – मीडियन और विंर फ़िल्टर लागू करें
url: /hi/java/image-processing-and-enhancement/median-and-wiener-filter-application/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# मीडियन फ़िल्टर जावा – मीडियन और विंर फ़िल्टर लागू करें

## Quick Answers
- **मीडियन फ़िल्टर क्या करता है?** यह प्रत्येक पिक्सेल को उसके आसपास के पड़ोस के मीडियन मान से बदल देता है, इम्पल्स शोर को हटाते हुए किनारों को संरक्षित रखता है।  
- **कौन सी लाइब्रेरी मीडियन फ़िल्टर जावा को सपोर्ट करती है?** Aspose.Imaging for Java एक तैयार‑से‑उपयोग `MedianFilterOptions` क्लास प्रदान करती है।  
- **क्या कोड चलाने के लिए लाइसेंस चाहिए?** मूल्यांकन के लिए एक मुफ्त ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **क्या मैं मीडियन फ़िल्टर को अन्य फ़िल्टरों के साथ चेन कर सकता हूँ?** हाँ, आप मीडियन चरण के बाद विंर जैसे अतिरिक्त फ़िल्टर लागू कर सकते हैं।  
- **कौन से इमेज फ़ॉर्मेट समर्थित हैं?** अधिकांश रास्टर फ़ॉर्मेट (PNG, JPEG, BMP, TIFF, आदि) पूरी तरह से समर्थित हैं।

## मीडियन फ़िल्टर जावा क्या है?
मीडियन फ़िल्टर एक गैर‑रेखीय डिजिटल फ़िल्टरिंग तकनीक है जो आमतौर पर **इमेज शोर को हटाने** के लिए उपयोग की जाती है। जावा में, Aspose.Imaging इस फ़िल्टर को `MedianFilterOptions` क्लास के माध्यम से लागू करता है, जिससे आप कर्नेल आकार निर्दिष्ट कर सकते हैं जो निर्धारित करता है कि कितने पड़ोसी पिक्सेल विचार किए जाएँ।

## क्यों उपयोग करें मीडियन फ़िल्टर जावा इमेज डीनॉइज़िंग के लिए?
- **किनारों को संरक्षित करता है** साधारण औसत फ़िल्टरों की तुलना में बेहतर।  
- **सरल API** – कुछ ही कोड लाइनों से स्पेकल और साल्ट‑एंड‑पेपर शोर हट जाता है।  
- **Aspose.Imaging के साथ लोड की गई किसी भी रास्टर इमेज** पर काम करता है, जिससे यह सर्वर‑साइड प्रोसेसिंग के लिए आदर्श बनता है।

## Prerequisites
शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **जावा विकास पर्यावरण** – JDK 8 या बाद का स्थापित हो।  
2. **Aspose.Imaging for Java** – लाइब्रेरी को [here](https://releases.aspose.com/imaging/java/) से डाउनलोड और इंस्टॉल करें।  
3. **नॉइज़ी इमेज का नमूना** – कोई भी इमेज जिसे आप साफ़ करना चाहते हैं; इस गाइड के लिए हम `your‑noisy‑image.png` का उपयोग करेंगे।  

## Import Packages
अपने जावा प्रोजेक्ट में, आवश्यक Aspose.Imaging क्लासेज़ को आयात करके शुरू करें:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.RasterImage;
import com.aspose.imaging.imagefilters.filteroptions.MedianFilterOptions;
```

## How to Apply Median Filter Java
नीचे चरण‑बद्ध मार्गदर्शन दिया गया है। प्रत्येक चरण में एक संक्षिप्त व्याख्या और फिर वह सटीक कोड शामिल है जिसे आपको कॉपी करना है।

### Step 1: Load the Noisy Image
पहले, वह इमेज लोड करें जिसे आप डीनॉइज़ करना चाहते हैं। यह Aspose.Imaging के `Image.load` मेथड का उपयोग करके **load image java** को दर्शाता है।

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (Image image = Image.load(dataDir + "your-noisy-image.png"))
{
    // Cast the image into RasterImage
    RasterImage rasterImage = (RasterImage) image;
```

### Step 2: Create and Configure the Median Filter
`MedianFilterOptions` का एक इंस्टेंस बनाएं और कर्नेल आकार सेट करें। बड़ा आकार अधिक शोर हटाता है लेकिन विवरण धुंधला हो सकता है।

```java
    // Create an instance of MedianFilterOptions class and set the size.
    MedianFilterOptions options = new MedianFilterOptions(4);
```

### Step 3: Apply the Median Filter
फ़िल्टर को पूरी इमेज की सीमाओं पर लागू करें। यह मुख्य **apply median filter** ऑपरेशन है।

```java
    // Apply Median filter to RasterImage object.
    rasterImage.filter(image.getBounds(), options);
```

### Step 4: Save the Resultant Image
अंत में, डीनॉइज़्ड इमेज को डिस्क पर लिखें। अब आप मीडियन फ़िल्टर का प्रभाव देख सकते हैं।

```java
    // Save the resultant image
    image.save("Your Document Directory" + "denoised-image.png");
}
```

## Common Issues and Solutions
- **कर्नेल आकार बहुत बड़ा** – इमेज अत्यधिक धुंधली दिख सकती है। अधिकांश फ़ोटो के लिए 3‑5 के बीच मान आज़माएँ।  
- **असमर्थित इमेज फ़ॉर्मेट** – सुनिश्चित करें कि फ़ाइल Aspose.Imaging द्वारा समर्थित रास्टर फ़ॉर्मेट है।  
- **OutOfMemoryError** – फ़िल्टरिंग से पहले `RasterImage` के `crop` मेथड का उपयोग करके बड़े इमेज को छोटे टाइल्स में प्रोसेस करें।  

## निष्कर्ष
इस गाइड में हमने Aspose.Imaging द्वारा प्रदान किए गए **median filter java** दृष्टिकोण का उपयोग करके **इमेज को डीनॉइज़ कैसे करें** दिखाया। ऊपर दिए गए चरणों का पालन करके, आप किसी भी जावा‑आधारित इमेज‑प्रोसेसिंग पाइपलाइन में शोर‑हटाने को जल्दी से एकीकृत कर सकते हैं, और विंर फ़िल्टर या अन्य उन्नत तकनीकों को चेन करके परिणामों को और बेहतर बना सकते हैं।

## Frequently Asked Questions

**Q1: Aspose.Imaging for Java क्या है?**  
A1: Aspose.Imaging for Java एक जावा लाइब्रेरी है जो डेवलपर्स को इमेज के साथ काम करने और विभिन्न इमेज प्रोसेसिंग कार्यों को प्रोग्रामेटिकली करने की अनुमति देती है।

**Q2: क्या मैं Aspose.Imaging for Java को मुफ्त में उपयोग कर सकता हूँ?**  
A2: Aspose.Imaging for Java एक व्यावसायिक लाइब्रेरी है, लेकिन आप एक मुफ्त ट्रायल संस्करण [here](https://releases.aspose.com/) से प्राप्त कर सकते हैं। हालांकि, विस्तारित उपयोग के लिए आपको [here](https://purchase.aspose.com/buy) से लाइसेंस खरीदना होगा।

**Q3: मैं Aspose.Imaging for Java के लिए समर्थन कैसे प्राप्त कर सकता हूँ?**  
A3: आप Aspose.Imaging समुदाय और विशेषज्ञों से [Aspose.Imaging Forum](https://forum.aspose.com/) पर मदद और सहायता ले सकते हैं।

**Q4: कुछ अन्य इमेज एन्हांसमेंट तकनीकें क्या हैं?**  
A4: मीडियन फ़िल्टर के अलावा, इमेज एन्हांसमेंट तकनीकों में विंर फ़िल्टरिंग, गॉसियन ब्लरिंग, और कॉन्ट्रास्ट स्ट्रेचिंग आदि शामिल हैं।

**Q5: क्या मैं Aspose.Imaging for Java को अपनी वेब एप्लिकेशन में उपयोग कर सकता हूँ?**  
A5: हाँ, आप सर्वर‑साइड इमेज प्रोसेसिंग के लिए Aspose.Imaging for Java को अपनी वेब एप्लिकेशनों में एकीकृत कर सकते हैं।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-17  
**Tested With:** Aspose.Imaging for Java 24.11  
**Author:** Aspose