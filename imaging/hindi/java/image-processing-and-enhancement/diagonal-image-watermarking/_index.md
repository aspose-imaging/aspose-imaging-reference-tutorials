---
date: 2026-01-09
description: Aspose.Imaging for Java के साथ छवियों में वॉटरमार्क कैसे जोड़ें, सीखें।
  यह जावा इमेज प्रोसेसिंग ट्यूटोरियल चरण‑बद्ध तरीके से दिखाता है कि कैसे जल्दी से
  एक तिरछा वॉटरमार्क बनाया जाए।
linktitle: Diagonal Image Watermarking
second_title: Aspose.Imaging Java Image Processing API
title: वॉटरमार्क कैसे जोड़ें – तिरछा इमेज वॉटरमार्किंग (जावा)
url: /hi/java/image-processing-and-enhancement/diagonal-image-watermarking/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# कैसे जोड़ें वॉटरमार्क – तिरछा इमेज वॉटरमार्किंग (Java)

यदि आप अपनी तस्वीरों में एक स्टाइलिश तिरछी दिशा में **वॉटरमार्क कैसे जोड़ें** चाहते हैं, तो Aspose.Imaging for Java इसे बेहद आसान बनाता है। इस चरण‑दर‑चरण ट्यूटोरियल में हम 45‑डिग्री घुमा हुआ टेक्स्ट वॉटरमार्क JPG (या किसी भी समर्थित) इमेज पर जोड़ेंगे। आपको जावा का जादूगर होने की जरूरत नहीं – प्रत्येक ब्लॉक को साधारण भाषा में समझाया गया है ताकि आप कुछ ही मिनटों में परिणाम दोहरा सकें।

## त्वरित उत्तर
- **कौन सी लाइब्रेरी उपयोग की गई है?** Aspose.Imaging for Java  
- **कौन सा मुख्य कीवर्ड कवर किया गया है?** how to add watermark  
- **समर्थित इमेज फॉर्मेट?** JPEG, PNG, BMP, TIFF, GIF और अधिक  
- **कोड की मात्रा?** केवल सात संक्षिप्त कोड ब्लॉक्स  
- **टेस्टिंग के लिए लाइसेंस चाहिए?** एक फ्री ट्रायल उपलब्ध है; प्रोडक्शन के लिए लाइसेंस आवश्यक है  

## इमेज प्रोसेसिंग में “how to add watermark” क्या है?
वॉटरमार्क जोड़ना मतलब इमेज पर अर्द्ध‑पारदर्शी टेक्स्ट या ग्राफ़िक्स को ओवरले करना, ताकि स्वामित्व की रक्षा हो या ब्रांडिंग दर्शाई जा सके। एक तिरछा वॉटरमार्क विशेष रूप से प्रभावी होता है क्योंकि यह पूरी तस्वीर को कवर करता है और इसे हटाना कठिन होता है।

## Aspose.Imaging for Java क्यों उपयोग करें?
Aspose.Imaging एक हाई‑लेवल API प्रदान करता है जो लो‑लेवल पिक्सेल मैनिपुलेशन को एब्स्ट्रैक्ट करता है, दर्जनों फॉर्मेट को सपोर्ट करता है, और किसी भी जावा रनटाइम पर काम करता है। यह आपको *क्या* करना है—जैसे तिरछा वॉटरमार्क जोड़ना—पर फोकस करने देता है, बिना इमेज‑फॉर्मेट की जटिलताओं की चिंता किए।

## पूर्वापेक्षाएँ

शुरू करने से पहले सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

1. **Aspose.Imaging for Java** – आधिकारिक साइट से नवीनतम संस्करण **[यहाँ](https://releases.aspose.com/imaging/java/)** डाउनलोड करें।  
2. **जावा डेवलपमेंट एनवायरनमेंट** – JDK 8+ और आपका पसंदीदा IDE (IntelliJ, Eclipse, VS Code, आदि)।  
3. **वॉटरमार्क करने के लिए एक इमेज** – कोड में जिस फ़ोल्डर का संदर्भ देंगे, वहाँ एक नमूना JPG/TIFF/PNG रखें।

## पैकेज इम्पोर्ट करें

सबसे पहले, उन क्लासेज़ को इम्पोर्ट करें जिनकी आपको आवश्यकता होगी। इम्पोर्ट को एक साथ रखने से कोड पढ़ने और मेंटेन करने में आसानी होती है।

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## चरण 1: मौजूदा इमेज लोड करें

हम स्रोत तस्वीर को लोड करके शुरू करते हैं। `Image.load` मेथड स्वचालित रूप से फॉर्मेट का पता लगा लेता है।

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Load an existing JPG image
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Rest of the code goes here
}
```

> **प्रो टिप:** `Image` ऑब्जेक्ट को `try‑with‑resources` ब्लॉक में रखें (जैसा दिखाया गया है) ताकि यह स्वतः डिस्पोज़ हो जाए और मेमोरी लीक न हो।

## चरण 2: वॉटरमार्क टेक्स्ट और ग्राफ़िक्स तैयार करें

लोड की गई इमेज से जुड़ा एक `Graphics` ऑब्जेक्ट बनाएं और बाद में गणनाओं के लिए इमेज का आकार स्टोर करें।

```java
// Declare a String object with Watermark Text
String theString = "45 Degree Rotated Text";

// Create and initialize an instance of Graphics class
Graphics graphics = new Graphics(image);

// Initialize an object of SizeF to store image Size
Size sz = graphics.getImage().getSize();
```

## चरण 3: फ़ॉन्ट और ब्रश निर्धारित करें

ऐसा फ़ॉन्ट चुनें जो स्पष्ट दिखे और एक ब्रश जो वॉटरमार्क का रंग और अपारदर्शिता निर्धारित करे। अपारदर्शिता को समायोजित करके वॉटरमार्क को अर्द्ध‑पारदर्शी बनाएं।

```java
// Create an instance of Font, initialize it with Font Face, Size, and Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Create an instance of SolidBrush and set its various properties
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## चरण 4: अपने टेक्स्ट को फॉर्मेट करें

ऐलाइनमेंट और फॉर्मेटिंग फ्लैग सेट करें ताकि टेक्स्ट ड्रॉ करते समय केंद्रित रहे।

```java
// Initialize an object of StringFormat class and set its various properties
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## चरण 5: ट्रांसफ़ॉर्मेशन लागू करें

एक ट्रांसफ़ॉर्मेशन मैट्रिक्स हमें इमेज के केंद्र पर ओरिजिन ले जाने और फिर टेक्स्ट को ‑45° (घड़ी की दिशा में) घुमाने की अनुमति देता है।

```java
// Create an object of Matrix class for transformation
Matrix matrix = new Matrix();
// First a translation then a rotation
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Set the Transformation through Matrix
graphics.setTransform(matrix);
```

## चरण 6: ड्रॉ करें और सेव करें

अंत में, स्ट्रिंग को इमेज पर रेंडर करें और परिणाम को डिस्क पर लिखें।

```java
// Draw the string on Image
graphics.drawString(theString, font, brush, 0, 0, format);

// Save output to disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

जब आप `AddDiagonalWatermarkToImage_out.jpg` खोलेंगे, तो आपको लाल, अर्द्ध‑पारदर्शी टेक्स्ट तस्वीर के केंद्र में तिरछा दिखेगा।

## सामान्य समस्याएँ और समाधान

| समस्या | कारण | समाधान |
|---------|--------|-----|
| वॉटरमार्क बहुत हल्का दिख रहा है | अपारदर्शिता 0 (पूरी तरह पारदर्शी) सेट है | अपारदर्शिता बढ़ाएँ, उदाहरण: `brush.setOpacity(0.5f);` |
| टेक्स्ट किनारों पर कट रहा है | गैर‑स्क्वायर इमेज के लिए ट्रांसलेशन केंद्रित नहीं है | जैसा दिखाया गया है `matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);` उपयोग करें, फिर आवश्यकता अनुसार रोटेशन एंगल समायोजित करें |
| असमर्थित इमेज फॉर्मेट त्रुटि | पुराना Aspose.Imaging संस्करण उपयोग किया गया | नवीनतम Aspose.Imaging रिलीज़ में अपडेट करें |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या Aspose.Imaging for Java शुरुआती लोगों के लिए उपयुक्त है?

**A:** बिल्कुल! API सहज है, और दस्तावेज़ीकरण स्पष्ट उदाहरण प्रदान करता है। इमेज प्रोसेसिंग में नए डेवलपर्स भी इस ट्यूटोरियल को फॉलो करके जल्दी ही प्रोफ़ेशनल परिणाम प्राप्त कर सकते हैं।

### Q2: क्या मैं वॉटरमार्क टेक्स्ट और स्टाइल को कस्टमाइज़ कर सकता हूँ?

**A:** हाँ। `theString` वेरिएबल बदलें, कोई अलग `Font` चुनें, `brush.setColor(...)` संशोधित करें, या मैट्रिक्स में रोटेशन एंगल बदलें ताकि आपका ब्रांडिंग फिट हो सके।

### Q3: क्या Aspose.Imaging for Java JPG के अलावा अन्य इमेज फॉर्मेट सपोर्ट करता है?

**A:** हाँ। लाइब्रेरी BMP, PNG, GIF, TIFF, PSD और कई अन्य फॉर्मेट के साथ काम करती है। बस `Image.load` मेथड को उचित फ़ाइल पर पॉइंट करें।

### Q4: क्या Aspose.Imaging for Java के लिए फ्री ट्रायल उपलब्ध है?

**A:** हाँ, आप Aspose.Imaging for Java को फ्री ट्रायल के साथ आज़मा सकते हैं। इसे **[यहाँ](https://releases.aspose.com/)** प्राप्त करें।

### Q5: Aspose.Imaging for Java के लिए सहायता या सपोर्ट कहाँ मिल सकता है?

**A:** प्रश्नों, बग रिपोर्ट या बेस्ट‑प्रैक्टिस सलाह के लिए Aspose.Imaging for Java सपोर्ट फ़ोरम **[यहाँ](https://forum.aspose.com/)** देखें।

---

**अंतिम अपडेट:** 2026-01-09  
**टेस्टेड संस्करण:** Aspose.Imaging for Java 24.11 (लेखन समय पर नवीनतम)  
**लेखक:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}