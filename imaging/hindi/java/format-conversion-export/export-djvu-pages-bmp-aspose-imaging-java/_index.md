---
date: '2026-06-18'
description: Aspose Imaging Maven dependency का उपयोग करके Java में DJVU फ़ाइलों को
  BMP छवियों में बदलना सीखें। सेटअप, विकल्प, और पेज‑रेंज एक्सपोर्ट के साथ चरण‑बद्ध
  गाइड।
keywords:
- aspose imaging maven dependency
- how to convert djvu
- convert djvu to bmp java
- aspose imaging java setup
- djvu page export bmp
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how to use the Aspose Imaging Maven dependency to convert DJVU
    files to BMP images in Java. Step‑by‑step guide with setup, options, and page‑range
    export.
  headline: Aspose Imaging Maven Dependency – Convert DJVU to BMP in Java
  type: TechArticle
- description: Learn how to use the Aspose Imaging Maven dependency to convert DJVU
    files to BMP images in Java. Step‑by‑step guide with setup, options, and page‑range
    export.
  name: Aspose Imaging Maven Dependency – Convert DJVU to BMP in Java
  steps:
  - name: '**Archiving:** Convert DJVU files to BMP for easier archival and retrieval.'
    text: '**Archiving:** Convert DJVU files to BMP for easier archival and retrieval.'
  - name: '**Document Sharing:** Share individual images from DJVU documents without
      requiring specialized viewers.'
    text: '**Document Sharing:** Share individual images from DJVU documents without
      requiring specialized viewers.'
  - name: '**Web Development:** Use BMP images for web projects that need lossless
      graphics.'
    text: '**Web Development:** Use BMP images for web projects that need lossless
      graphics.'
  - name: '**Education:** Provide students with accessible image formats for study
      materials.'
    text: '**Education:** Provide students with accessible image formats for study
      materials.'
  - name: '**Integration:** Embed this conversion process into larger Java applications
      for automated workflows.'
    text: '**Integration:** Embed this conversion process into larger Java applications
      for automated workflows.'
  type: HowTo
- questions:
  - answer: DJVU is a highly compressed file format designed for storing scanned documents,
      images, and multi‑page publications while maintaining visual fidelity.
    question: What is a DJVU file?
  - answer: Yes, modify the `IntRange` parameters to target any start and end indices
      you require.
    question: Can I convert other page ranges besides the first two pages?
  - answer: Increase the bits‑per‑pixel setting in `BmpOptions` to 32 and ensure the
      source DJVU pages are not downscaled during loading.
    question: My BMP files look blurry—how can I improve quality?
  - answer: Process the file in chunks, dispose of each `DjvuImage` after saving,
      and consider streaming pages rather than loading the entire document at once.
    question: How do I handle very large DJVU files efficiently?
  - answer: Visit the [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      or the [Aspose.Imaging Java Documentation](https://reference.aspose.com/imaging/java/)
      for comprehensive guides, API references, and sample projects. For community
      help, see [Aspose.Imaging Support](https://forum.aspose.com/c/imaging/14).
    question: Where can I find more Aspose.Imaging resources?
  type: FAQPage
title: Aspose Imaging Maven Dependency – Java में DJVU को BMP में बदलें
url: /hi/java/format-conversion-export/export-djvu-pages-bmp-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# व्यापक गाइड: Aspose.Imaging Java का उपयोग करके DJVU पृष्ठों को BMP फ़ाइलों के रूप में निर्यात करना

## परिचय

डिजिटल युग में, दस्तावेज़ फ़ॉर्मेट को कुशलतापूर्वक प्रबंधित और परिवर्तित करना सहज सामग्री साझा करने और अभिलेखीयकरण के लिए अत्यंत महत्वपूर्ण है। **The Aspose Imaging Maven dependency** DJVU फ़ाइलों को अधिक सुलभ BMP छवियों में बदलना आसान बनाता है, बिना लो‑लेवल पार्सिंग कोड लिखे। यह ट्यूटोरियल आपको DJVU दस्तावेज़ लोड करने, BMP निर्यात विकल्प कॉन्फ़िगर करने, विशिष्ट पृष्ठ चुनने, और प्रत्येक पृष्ठ को व्यक्तिगत BMP फ़ाइल के रूप में सहेजने की प्रक्रिया दिखाता है—सिर्फ कुछ ही Java लाइनों के साथ।

**आप क्या सीखेंगे**

- कैसे अपने प्रोजेक्ट में Aspose Imaging Maven dependency जोड़ें।  
- कैसे Aspose.Imaging for Java का उपयोग करके DJVU फ़ाइलों को लोड और प्रोसेस करें।  
- कैसे BMP निर्यात विकल्प जैसे रंग गहराई को कॉन्फ़िगर करें।  
- कैसे एक कस्टम पेज रेंज निर्धारित करें और उन पृष्ठों को अलग-अलग BMP फ़ाइलों के रूप में निर्यात करें।  

इस गाइड के अंत तक, आप किसी भी Java एप्लिकेशन में DJVU‑to‑BMP रूपांतरण को एकीकृत कर सकेंगे, जिससे आपके दस्तावेज़ वर्कफ़्लो में सुधार होगा और थर्ड‑पार्टी व्यूअर्स पर निर्भरता कम होगी।

## त्वरित उत्तर
- **कौन सा Maven आर्टिफैक्ट Aspose.Imaging जोड़ता है?** `com.aspose:aspose-imaging`
- **क्या मैं केवल चयनित पृष्ठों को निर्यात कर सकता हूँ?** हाँ, पेज इंडेक्स निर्दिष्ट करने के लिए `IntRange` का उपयोग करें।
- **कौन सी BMP रंग गहराई अनुशंसित है?** लॉसलेस गुणवत्ता के लिए प्रति पिक्सेल 32 बिट।
- **क्या उत्पादन के लिए लाइसेंस आवश्यक है?** हाँ, खरीदा गया लाइसेंस मूल्यांकन सीमाओं को हटा देता है।
- **कौन सा Java संस्करण समर्थित है?** Java 8 और बाद के संस्करण।

## Aspose Imaging Maven Dependency क्या है?
**Aspose Imaging Maven dependency** एक Maven‑संगत पैकेज है जो Java कोड से सीधे 100 से अधिक इमेज और दस्तावेज़ फ़ॉर्मेट को पढ़ने, प्रोसेस करने और परिवर्तित करने के लिए व्यापक API प्रदान करता है। इस निर्भरता को अपने `pom.xml` में जोड़ने से आपको `Image`, `DjvuImage`, और `IntRange` जैसी क्लासेस तुरंत उपलब्ध हो जाती हैं, बिना मैन्युअल JAR प्रबंधन के।

## DJVU से BMP रूपांतरण के लिए Aspose.Imaging क्यों उपयोग करें?
Aspose.Imaging **100+ इनपुट और आउटपुट फ़ॉर्मेट** का समर्थन करता है और कई‑सौ पृष्ठों वाले DJVU फ़ाइलों को पूरी दस्तावेज़ को मेमोरी में लोड किए बिना प्रोसेस कर सकता है, जिससे RAM उपयोग में 70 % तक कमी आती है। इसका नेटिव BMP एन्कोडर पूर्ण रंग सटीकता बनाए रखता है, जिससे यह अभिलेखीय‑ग्रेड इमेज एक्सट्रैक्शन के लिए आदर्श है।

## पूर्वापेक्षाएँ
- **Aspose.Imaging for Java** संस्करण 25.5 (या नया)।  
- **Java Development Kit** 8 या बाद का स्थापित हो।  
- Maven या Gradle बिल्ड टूल्स का परिचय।  
- वैध Aspose.Imaging लाइसेंस (मूल्यांकन के लिए ट्रायल काम करता है)।

## Aspose.Imaging for Java सेट अप करना

### इंस्टॉलेशन जानकारी

**Maven:**  
अपने `pom.xml` में निम्नलिखित निर्भरता जोड़ें:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

**Gradle:**  
Gradle उपयोगकर्ताओं के लिए, इस पंक्ति को अपने `build.gradle` में शामिल करें:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

**Direct Download:**  
वैकल्पिक रूप से, आप नवीनतम रिलीज़ को [Aspose.Imaging for Java रिलीज़](https://releases.aspose.com/imaging/java/) से डाउनलोड कर सकते हैं। संस्करण इतिहास के लिए आप [Aspose.Imaging रिलीज़](https://releases.aspose.com/imaging/java/) पृष्ठ देख सकते हैं।

### लाइसेंस प्राप्त करना

Aspose.Imaging को पूरी तरह उपयोग करने के लिए:

- **मुफ़्त ट्रायल:** इसकी क्षमताओं को खोजने के लिए मुफ्त ट्रायल शुरू करें। ([अपना मुफ्त ट्रायल शुरू करें](https://releases.aspose.com/imaging/java/))  
- **टेम्पररी लाइसेंस:** यदि आपको लाइब्रेरी का मूल्यांकन करने के लिए अधिक समय चाहिए तो टेम्पररी लाइसेंस प्राप्त करें। ([टेम्पररी लाइसेंस प्राप्त करें](https://purchase.aspose.com/temporary-license/))  
- **खरीद:** दीर्घकालिक उपयोग के लिए लाइसेंस खरीदने पर विचार करें। ([Aspose.Imaging खरीदें](https://purchase.aspose.com/buy))

**बेसिक इनिशियलाइज़ेशन:**  
पर्यावरण सेट अप करने और लाइसेंस (यदि आवश्यक हो) प्राप्त करने के बाद, Aspose.Imaging को इस प्रकार इनिशियलाइज़ करें:

```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("path/to/your/license/file.lic");
```

## Java में DJVU को BMP में कैसे बदलें?

`Image.load("source.djvu")` के साथ अपना DJVU फ़ाइल लोड करें, BMP निर्यात विकल्प कॉन्फ़िगर करें, वांछित पेज रेंज निर्दिष्ट करें, और प्रत्येक पेज पर `save` कॉल करें – पूरी रूपांतरण दस लाइनों से कम कोड में पूरी की जा सकती है। यह तरीका रंग गहराई, पेज इंडेक्सिंग, और फ़ाइल I/O को स्वचालित रूप से संभालता है, जिससे आप इमेज पार्सिंग के बजाय बिज़नेस लॉजिक पर ध्यान केंद्रित कर सकते हैं।

### Load and Process DJVU File

**समीक्षा:**  
DJVU फ़ाइल लोड करना हमारे वर्कफ़्लो का पहला कदम है। Aspose.Imaging for Java इस प्रक्रिया को सरल बनाता है, जिससे आप DJVU दस्तावेज़ों को आसानी से संभाल सकते हैं।

`Image.load` मेथड DJVU फ़ाइल को `DjvuImage` ऑब्जेक्ट में पढ़ता है, जो मेमोरी में मल्टी‑पेज दस्तावेज़ का प्रतिनिधित्व करता है।

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.djvu.DjvuImage;

String dataDir = "YOUR_DOCUMENT_DIRECTORY" + "Sample.djvu";
try (DjvuImage image = (DjvuImage) Image.load(dataDir)) {
    // The DjVuImage object now holds the loaded DJVU file and can be processed further.
}
```

**व्याख्या:**  
- **`Image.load`:** आपका DJVU फ़ाइल लोड करता है और आगे की प्रोसेसिंग के लिए `DjvuImage` इंस्टेंस लौटाता है।

### Set Export Options for BMP Format

**समीक्षा:**  
निर्यात विकल्प कॉन्फ़िगर करने से सुनिश्चित होता है कि आउटपुट BMP फ़ाइलें आपकी गुणवत्ता आवश्यकताओं को पूरा करें।

`BmpOptions` आपको सहेजने से पहले बिट‑पर‑पिक्सेल, कम्प्रेशन, और रिज़ॉल्यूशन जैसी प्रॉपर्टीज़ निर्धारित करने की अनुमति देता है।

```java
import com.aspose.imaging.imageoptions.BmpOptions;

BmpOptions exportOptions = new BmpOptions();
exportOptions.setBitsPerPixel(32);
```

**व्याख्या:**  
- **`setBitsPerPixel`:** निर्यात छवियों की रंग गहराई सेट करता है। 32 बिट प्रति पिक्सेल का उपयोग करने से लॉसलेस, उच्च‑गुणवत्ता वाले BMP फ़ाइलें मिलती हैं, जो अभिलेखीय उद्देश्यों के लिए उपयुक्त हैं।

### Define Page Range to Export

**समीक्षा:**  
कौन से पृष्ठ निर्यात करने हैं, यह निर्दिष्ट करने से आप केवल आवश्यक सामग्री पर ध्यान केंद्रित कर सकते हैं।

`IntRange` शून्य‑आधारित पेज इंडेक्स की रेंज बनाता है; इस उदाहरण में हम पहले दो पृष्ठ चुनते हैं।

```java
import com.aspose.imaging.IntRange;

IntRange range = new IntRange(0, 2);
```

**व्याख्या:**  
- **`IntRange`:** पेज नंबरों की निरंतर रेंज का प्रतिनिधित्व करता है। आप आवश्यकतानुसार शुरू और अंत मान बदलकर किसी भी पृष्ठ उपसमुच्चय को निर्यात कर सकते हैं।

### Export Specified Pages as Separate BMP Files

**समीक्षा:**  
अंतिम चरण में चयनित पृष्ठों को व्यक्तिगत BMP फ़ाइलों के रूप में निर्यात किया जाता है।

`DjvuMultiPageOptions` प्रत्येक पृष्ठ के निर्यात को कॉन्फ़िगर करता है, और `image.save` BMP फ़ाइलों को लक्ष्य डायरेक्टरी में लिखता है।

```java
import com.aspose.imaging.imageoptions.DjvuMultiPageOptions;

int counter = 0;
for (int i : range.getRange()) {
    exportOptions.setMultiPageOptions(new DjvuMultiPageOptions(range.getArrayOneItemFromIndex(counter)));
    image.save("YOUR_OUTPUT_DIRECTORY" + (counter++) + ".bmp", exportOptions);
}
```

**व्याख्या:**  
- **`DjvuMultiPageOptions`:** मल्टी‑पेज निर्यात के लिए पेज‑रेंज जानकारी और BMP विकल्प रखता है।  
- **`image.save`:** प्रत्येक चयनित पृष्ठ को डिस्क पर अलग BMP फ़ाइल के रूप में सहेजता है।

## व्यावहारिक अनुप्रयोग

1. **अभिलेखीयकरण:** DJVU फ़ाइलों को BMP में बदलें ताकि अभिलेखीयकरण और पुनः प्राप्ति आसान हो।  
2. **दस्तावेज़ साझा करना:** DJVU दस्तावेज़ों से व्यक्तिगत छवियों को साझा करें बिना विशेष व्यूअर्स की आवश्यकता के।  
3. **वेब विकास:** वेब प्रोजेक्ट्स में लॉसलेस ग्राफ़िक्स की आवश्यकता होने पर BMP छवियों का उपयोग करें।  
4. **शिक्षा:** छात्रों को अध्ययन सामग्री के लिए सुलभ इमेज फ़ॉर्मेट प्रदान करें।  
5. **एकीकरण:** इस रूपांतरण प्रक्रिया को बड़े Java एप्लिकेशन में एम्बेड करें ताकि स्वचालित वर्कफ़्लो बन सके।

## प्रदर्शन विचार

- **मेमोरी उपयोग अनुकूलित करें:** `DjvuImage` ऑब्जेक्ट को `close()` के साथ तुरंत डिस्पोज़ करें ताकि नेटिव संसाधन मुक्त हो सकें।  
- **बैच प्रोसेसिंग:** कई DJVU फ़ाइलों को लूप में प्रोसेस करें ताकि I/O ओवरहेड कम हो।  
- **समांतर प्रोसेसिंग:** मल्टी‑कोर सर्वरों पर पृष्ठों को एक साथ बदलने के लिए Java के `ExecutorService` का उपयोग करें।

## सामान्य समस्याएँ और समाधान

- **बड़ी DJVU फ़ाइलों पर OutOfMemoryError:** प्रत्येक पृष्ठ सहेजने के बाद `image.dispose()` का उपयोग करें और आवश्यकतानुसार JVM हीप आकार बढ़ाएँ।  
- **कम‑गुणवत्ता वाला BMP आउटपुट:** सुनिश्चित करें कि `BmpOptions.setBitsPerPixel(32)` सेट है; कम मान रंग सटीकता घटाते हैं।  
- **आउटपुट में पृष्ठ गायब:** यह सत्यापित करें कि `IntRange` इंडेक्स वास्तविक पेज काउंट (`djvuImage.getPages().size()`) से मेल खाते हैं।

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: DJVU फ़ाइल क्या है?**  
**उत्तर:** DJVU एक अत्यधिक संकुचित फ़ाइल फ़ॉर्मेट है, जिसे स्कैन किए गए दस्तावेज़, छवियों और मल्टी‑पेज प्रकाशनों को दृश्य सटीकता बनाए रखते हुए संग्रहीत करने के लिए डिज़ाइन किया गया है।

**प्रश्न: क्या मैं पहले दो पृष्ठों के अलावा अन्य रेंज भी बदल सकता हूँ?**  
**उत्तर:** हाँ, `IntRange` पैरामीटर को बदलकर आप किसी भी प्रारंभ और समाप्ति इंडेक्स को लक्षित कर सकते हैं।

**प्रश्न: मेरी BMP फ़ाइलें धुंधली दिख रही हैं—गुणवत्ता कैसे बढ़ाएँ?**  
**उत्तर:** `BmpOptions` में बिट‑पर‑पिक्सेल सेटिंग को 32 तक बढ़ाएँ और सुनिश्चित करें कि स्रोत DJVU पृष्ठ लोडिंग के दौरान डाउनस्केल नहीं हुए हैं।

**प्रश्न: बहुत बड़ी DJVU फ़ाइलों को कुशलतापूर्वक कैसे संभालें?**  
**उत्तर:** फ़ाइल को भागों में प्रोसेस करें, सहेजने के बाद प्रत्येक `DjvuImage` को डिस्पोज़ करें, और पूरे दस्तावेज़ को लोड करने के बजाय पृष्ठों को स्ट्रीम करने पर विचार करें।

**प्रश्न: मैं और अधिक Aspose.Imaging संसाधन कहाँ पा सकता हूँ?**  
**उत्तर:** विस्तृत गाइड, API रेफ़रेंस, और सैंपल प्रोजेक्ट्स के लिए [Aspose.Imaging दस्तावेज़ीकरण](https://reference.aspose.com/imaging/java/) या [Aspose.Imaging Java दस्तावेज़ीकरण](https://reference.aspose.com/imaging/java/) देखें। समुदाय सहायता के लिए, देखें [Aspose.Imaging समर्थन](https://forum.aspose.com/c/imaging/14)।

---

**अंतिम अपडेट:** 2026-06-18  
**परीक्षित संस्करण:** Aspose.Imaging 25.5 for Java  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल

- [Aspose.Imaging for Java के साथ DjVu को ग्रेस्केल PNG में बदलें | फ़ॉर्मेट रूपांतरण ट्यूटोरियल](/imaging/java/format-conversion-export/export-djvu-grayscale-png-aspose-java/)
- [Aspose.Imaging के साथ Java में DjVu को TIFF में बदलें: चरण‑दर‑चरण गाइड](/imaging/java/format-conversion-export/load-export-djvu-tiff-aspose-imaging-java/)
- [Aspose.Imaging for Java का उपयोग करके DjVu को PDF में बदलें - चरण‑दर‑चरण गाइड](/imaging/java/image-loading-saving/convert-djvu-to-pdf-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}