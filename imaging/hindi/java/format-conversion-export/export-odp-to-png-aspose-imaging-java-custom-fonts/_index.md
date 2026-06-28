---
date: '2026-06-28'
description: Aspose.Imaging for Java का उपयोग करके ODP को PNG में कैसे बदलें, कस्टम
  फ़ॉन्ट्स सेट करें, और सटीक रेंडरिंग के लिए सिस्टम फ़ॉन्ट्स को निष्क्रिय करें, यह
  जानें।
keywords:
- how to convert odp
- maven aspose imaging
- aspose imaging license
- disable system fonts
- java convert presentation image
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  headline: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts
    & Export Guide
  type: TechArticle
- description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  name: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts & Export
    Guide
  steps:
  - name: '**Free Trial** – No license required, limited features.'
    text: '**Free Trial** – No license required, limited features.'
  - name: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
    text: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
  - name: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
    text: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
  - name: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
    text: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
  type: HowTo
- questions:
  - answer: Aspose.Imaging for Java works with JDK 8 and newer; JDK 11 is recommended
      for long‑term support.
    question: What is the minimum Java version required?
  - answer: Yes, set `rasterizationOptions.setPageNumber(specificSlideIndex)` before
      calling `save`.
    question: Can I convert only selected slides?
  - answer: Load the file with `LoadOptions` that includes the password, then proceed
      with the same font settings.
    question: How do I handle password‑protected ODP files?
  - answer: It marginally improves speed because the engine skips the lookup of system
      fonts, especially noticeable on machines with large font collections.
    question: Does disabling system fonts affect performance?
  - answer: Explore the official [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      for additional scenarios such as batch conversion and image transformations.
    question: Where can I find more code samples?
  type: FAQPage
title: Aspose.Imaging for Java के साथ ODP को PNG में कैसे बदलें – कस्टम फ़ॉन्ट्स &
  एक्सपोर्ट गाइड
url: /hi/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Aspose.Imaging for Java के साथ ODP को PNG में कैसे बदलें – कस्टम फ़ॉन्ट्स और एक्सपोर्ट गाइड

आधुनिक Java अनुप्रयोगों में, OpenDocument Presentation (ODP) फ़ाइलों को उच्च‑गुणवत्ता वाले PNG चित्रों में बदलना एक सामान्य आवश्यकता है—विशेष रूप से जब आपको कस्टम फ़ॉन्ट्स के माध्यम से ब्रांडिंग बनाए रखना हो। यह ट्यूटोरियल Aspose.Imaging for Java का उपयोग करके **ODP को PNG में कैसे बदलें** दिखाता है, कस्टम फ़ॉन्ट फ़ोल्डर सेट करने, सिस्टम‑फ़ॉलबैक फ़ॉन्ट्स को निष्क्रिय करने, और इष्टतम प्रदर्शन के लिए रास्टराइज़ेशन विकल्पों को फाइन‑ट्यून करने की प्रक्रिया बताता है।

**आप क्या सीखेंगे**
- ODP रूपांतरण के लिए कस्टम फ़ॉन्ट डायरेक्टरी कैसे सेट करें।  
- सिस्टम वैकल्पिक फ़ॉन्ट्स को कैसे निष्क्रिय करें ताकि केवल आपके चयनित टाइपफ़ेस उपयोग हों।  
- सटीक आयाम और फ़ॉन्ट सेटिंग्स के साथ ODP फ़ाइल को PNG में कैसे एक्सपोर्ट करें।  
- बड़े प्रस्तुतियों को प्रोसेस करते समय गति और मेमोरी उपयोग में सुधार के टिप्स।

## त्वरित उत्तर
- **क्या मैं Maven का उपयोग करके Aspose.Imaging जोड़ सकता हूँ?** हाँ, Maven निर्भरता जोड़ें और `mvn install` चलाएँ।  
- **क्या मुझे प्रोडक्शन के लिए लाइसेंस चाहिए?** असीमित उपयोग के लिए एक वैध Aspose.Imaging लाइसेंस आवश्यक है।  
- **क्या मेरे कस्टम फ़ॉन्ट्स का सम्मान होगा?** फ़ॉन्ट फ़ोल्डर सेट करें और सिस्टम वैकल्पिक फ़ॉन्ट्स को निष्क्रिय करें ताकि वे लागू हों।  
- **कौन से इमेज फ़ॉर्मेट समर्थित हैं?** Aspose.Imaging 120+ रास्टर और वेक्टर फ़ॉर्मेट्स को सपोर्ट करता है, जिसमें PNG, JPEG, TIFF, और WebP शामिल हैं।  
- **क्या API थ्रेड‑सेफ़ है?** हाँ, अधिकांश Aspose.Imaging क्लासेज़ थ्रेड‑सेफ़ हैं जब आप प्रत्येक थ्रेड के लिए अलग-अलग इंस्टेंस बनाते हैं।

## “how to convert odp” क्या है?
*“How to convert odp”* उस प्रक्रिया को दर्शाता है जिसमें OpenDocument Presentation फ़ाइल को किसी अन्य फ़ॉर्मेट—आमतौर पर PNG—में बदलते हैं, जबकि लेआउट, फ़ॉन्ट्स और दृश्य सटीकता को बनाए रखा जाता है। Aspose.Imaging for Java एक सिंगल‑मेथड वर्कफ़्लो प्रदान करता है जो इस रूपांतरण को बाहरी टूल्स की आवश्यकता के बिना संभालता है, जिससे डेवलपर्स न्यूनतम कोड के साथ सीधे अपने अनुप्रयोगों में रूपांतरण को एकीकृत कर सकते हैं।

## Java के लिए Aspose.Imaging क्यों उपयोग करें?
Aspose.Imaging **120+ आउटपुट फ़ॉर्मेट्स** को सपोर्ट करता है और पूरे दस्तावेज़ को मेमोरी में लोड किए बिना मल्टी‑पेज ODP फ़ाइलों को रास्टराइज़ कर सकता है, जिससे बड़े प्रस्तुतियों पर अधिकतम RAM उपयोग में 70 % तक कमी आती है। लाइब्रेरी बिल्ट‑इन फ़ॉन्ट मैनेजमेंट भी प्रदान करती है, जिससे थर्ड‑पार्टी रेंडरिंग इंजन की आवश्यकता समाप्त हो जाती है।

## पूर्वापेक्षाएँ
- **लाइब्रेरीज़**: Aspose.Imaging for Java ≥ 25.5.  
- **JDK**: संस्करण 8 या नया।  
- **IDE**: IntelliJ IDEA, Eclipse, या कोई भी Java‑संगत एडिटर।  
- **बेसिक नॉलेज**: Java I/O, object‑oriented programming, और image concepts।

## इंस्टॉलेशन निर्देश

### Maven
`pom.xml` में निम्नलिखित निर्भरता जोड़ें और `mvn clean install` चलाएँ:

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
`build.gradle` फ़ाइल में लाइब्रेरी शामिल करें और प्रोजेक्ट को रिफ्रेश करें:

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### डायरेक्ट डाउनलोड
नवीनतम JAR को [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/) से डाउनलोड करें।

## लाइसेंस प्राप्ति चरण
पूर्ण कार्यक्षमता अनलॉक करने के लिए, एक अस्थायी या स्थायी लाइसेंस लागू करें:

1. **फ़्री ट्रायल** – कोई लाइसेंस आवश्यक नहीं, सीमित फीचर्स।  
2. **अस्थायी लाइसेंस** – इसे [Aspose वेबसाइट](https://purchase.aspose.com/temporary-license/) पर अनुरोध करें।  
3. **खरीदें** – [Aspose purchase page](https://purchase.aspose.com/buy) से सब्सक्रिप्शन या परपेचुअल लाइसेंस खरीदें।

अपने लाइसेंस फ़ाइल के साथ लाइब्रेरी को इनिशियलाइज़ करें:

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## ODP रूपांतरण के लिए कस्टम फ़ॉन्ट डायरेक्टरी कैसे सेट करें?
`FontSettings` एक क्लास है जो Aspose.Imaging के लिए फ़ॉन्ट रिसोर्सेज़ को मैनेज करती है। किसी भी इमेज प्रोसेसिंग से पहले अपने कस्टम फ़ॉन्ट लोड करें। यह सुनिश्चित करता है कि प्रत्येक स्लाइड आपके द्वारा प्रदान किए गए सटीक टाइपफ़ेस का उपयोग करे।

Aspose.Imaging के `FontSettings` का उपयोग करके फ़ॉन्ट फ़ोल्डर पाथ सेट करें:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*परिभाषा एंकर*: `FontSettings.setFontsFolder` Aspose.Imaging को बताता है कि फ़ाइल सिस्टम पर TrueType और OpenType फ़ॉन्ट्स कहां खोजे।

## ODP रूपांतरण के दौरान सिस्टम वैकल्पिक फ़ॉन्ट्स को कैसे निष्क्रिय करें?
सिस्टम वैकल्पिक फ़ॉन्ट्स को निष्क्रिय करने से रेंडरिंग इंजन ऑपरेटिंग सिस्टम पर इंस्टॉल किए गए फ़ॉन्ट्स को अनदेखा करता है, जिससे केवल आपके द्वारा प्रदान किए गए फ़ॉन्ट्स का उपयोग सुनिश्चित होता है। यह अप्रत्याशित फ़ॉन्ट प्रतिस्थापन को समाप्त करता है जो आपके स्लाइड्स की दृश्य उपस्थिति को बदल सकता है।

निम्नलिखित कॉल के साथ सिस्टम वैकल्पिक फ़ॉन्ट्स को निष्क्रिय करें:

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*परिभाषा एंकर*: `FontSettings.setGetSystemAlternativeFont(false)` इंजन को केवल आपके द्वारा परिभाषित फ़ोल्डर में स्थित फ़ॉन्ट्स का उपयोग करने के लिए मजबूर करता है, जिससे अप्रत्याशित प्रतिस्थापन समाप्त हो जाते हैं।

## निर्दिष्ट फ़ॉन्ट के साथ ODP फ़ाइल को PNG में कैसे एक्सपोर्ट करें?
`RasterizationOptions` यह निर्धारित करता है कि वेक्टर पेज़ को बिटमैप इमेजेज़ में कैसे रास्टराइज़ किया जाता है। फ़ॉन्ट कॉन्फ़िगरेशन को रास्टराइज़ेशन सेटिंग्स के साथ मिलाकर, आप प्रत्येक एक्सपोर्ट किए गए PNG के लिए DPI, बैकग्राउंड कलर, और पेज साइज को नियंत्रित कर सकते हैं।

नीचे दिखाए गए अनुसार एक्सपोर्ट मेथड को लागू करें:

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.Image;
  import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
  import com.aspose.imaging.imageoptions.PngOptions;

  private static void exportToPng(String filePath, String defaultFontName, String outfileName) {
      FontSettings.setDefaultFontName(defaultFontName);
      try (Image document = Image.load(filePath)) {
          PngOptions saveOptions = new PngOptions();
          
          OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
          rasterizationOptions.setPageWidth(1000); // Set the page width for rendering
          rasterizationOptions.setPageHeight(1000);  // Set the page height for rendering

          saveOptions.setVectorRasterizationOptions(rasterizationOptions);
          document.save(outfileName, saveOptions);
      }
  }

  ```

*परिभाषा एंकर*: `RasterizationOptions` क्लास उत्पन्न PNG फ़ाइलों के लिए DPI, पेज साइज, और बैकग्राउंड कलर को नियंत्रित करती है।

### सामान्य समस्याएँ और समाधान
- **फ़ॉन्ट फ़ाइलें गायब** – सुनिश्चित करें कि ODP में संदर्भित प्रत्येक `.ttf` या `.otf` फ़ाइल आपके सेट किए हुए फ़ोल्डर में मौजूद है।  
- **गलत फ़ाइल पाथ** – `System.getProperty("user.dir")` के विरुद्ध एब्सोल्यूट पाथ या रिलेटिव पाथ रेज़ॉल्व करें।  
- **पर्याप्त अनुमतियाँ नहीं** – सुनिश्चित करें कि Java प्रोसेस फ़ॉन्ट डायरेक्टरी को पढ़ सकता है और आउटपुट फ़ोल्डर में लिख सकता है।

## व्यावहारिक अनुप्रयोग
1. **ब्रांड‑संगत स्लाइड डेक्स** – वेब पब्लिशिंग के लिए प्रस्तुतियों को PNG के रूप में एक्सपोर्ट करें जबकि कॉर्पोरेट फ़ॉन्ट्स को बनाए रखें।  
2. **ऑटोमेटेड रिपोर्ट जेनरेशन** – प्रत्येक स्लाइड को इमेज में बदलें ताकि PDF रिपोर्ट या ईमेल न्यूज़लेटर्स में शामिल किया जा सके।  
3. **लेगेसी आर्काइव निर्माण** – ODP कंटेंट को PNG के रूप में स्टोर करें ताकि भविष्य में एक्सेसिबिलिटी सुनिश्चित हो और ODP व्यूअर्स की आवश्यकता न पड़े।

## प्रदर्शन संबंधी विचार
- नवीनतम Aspose.Imaging संस्करण का उपयोग करें ताकि मल्टी‑थ्रेडेड रास्टराइज़ेशन सुधारों (8‑कोर CPUs पर 2× तेज) का लाभ मिल सके।  
- इमेज प्रोसेसिंग को try‑with‑resources ब्लॉक में रैप करें ताकि नेटिव रिसोर्सेज़ का समय पर डिस्पोज़ल सुनिश्चित हो।  
- हजारों स्लाइड्स प्रोसेस करते समय `RasterizationOptions` (जैसे, कम DPI) को समायोजित करें ताकि क्वालिटी और मेमोरी उपयोग के बीच संतुलन बना रहे।

## अक्सर पूछे जाने वाले प्रश्न

**प्रश्न: न्यूनतम Java संस्करण क्या आवश्यक है?**  
उत्तर: Aspose.Imaging for Java JDK 8 और नए संस्करणों के साथ काम करता है; दीर्घकालिक समर्थन के लिए JDK 11 की सिफारिश की जाती है।

**प्रश्न: क्या मैं केवल चयनित स्लाइड्स को बदल सकता हूँ?**  
उत्तर: हाँ, `save` कॉल करने से पहले `rasterizationOptions.setPageNumber(specificSlideIndex)` सेट करें।

**प्रश्न: पासवर्ड‑सुरक्षित ODP फ़ाइलों को कैसे हैंडल करें?**  
उत्तर: फ़ाइल को `LoadOptions` के साथ लोड करें जिसमें पासवर्ड शामिल हो, फिर वही फ़ॉन्ट सेटिंग्स के साथ आगे बढ़ें।

**प्रश्न: सिस्टम फ़ॉन्ट्स को निष्क्रिय करने से प्रदर्शन पर असर पड़ता है?**  
उत्तर: यह गति को थोड़ा बढ़ाता है क्योंकि इंजन सिस्टम फ़ॉन्ट्स की लुकअप को स्किप करता है, विशेषकर बड़े फ़ॉन्ट कलेक्शन वाले मशीनों पर यह स्पष्ट दिखता है।

**प्रश्न: अधिक कोड सैंपल्स कहाँ मिल सकते हैं?**  
उत्तर: बैच कन्वर्ज़न और इमेज ट्रांसफ़ॉर्मेशन जैसे अतिरिक्त परिदृश्यों के लिए आधिकारिक [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/) देखें।

## अतिरिक्त संसाधन
- [Aspose.Imaging for Java रिलीज़](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging रिलीज़](https://releases.aspose.com/imaging/java/)  
- [अपना फ्री ट्रायल शुरू करें](https://releases.aspose.com/imaging/java/)  
- [Aspose.Imaging दस्तावेज़ीकरण](https://reference.aspose.com/imaging/java/)  
- [Aspose.Imaging फ़ोरम](https://forum.aspose.com/c/imaging/14)  
- [Aspose लाइसेंसिंग खरीदें](https://purchase.aspose.com/buy)  
- [अस्थायी लाइसेंस के लिए आवेदन करें](https://purchase.aspose.com/temporary-license/)  

---

**अंतिम अपडेट:** 2026-06-28  
**परीक्षित संस्करण:** Aspose.Imaging for Java 25.5  
**लेखक:** Aspose

## संबंधित ट्यूटोरियल
- [Aspose.Imaging for Java के साथ ODG को PNG में बदलें: एक पूर्ण गाइड](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)  
- [Aspose.Imaging के साथ Java में कुशल इमेज कन्वर्ज़न: एक पूर्ण गाइड](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}