---
date: 2026-05-03
description: Aspose.Imaging का उपयोग करके जावा में मल्टी‑पेज TIFF को BMP फ़ॉर्मेट
  में कैसे बदलें, सीखें। TIFF को कुशलतापूर्वक बदलने के लिए इस चरण‑दर‑चरण गाइड का पालन
  करें।
keywords:
- convert multi page tiff
- how to convert tiff
- Aspose.Imaging Java
- TIFF to BMP conversion
- image processing Java
linktitle: TIFF फ्रेम्स को BMP फ़ॉर्मेट में निकालें
second_title: Aspose.Imaging Java Image Processing API
title: Aspose.Imaging for Java का उपयोग करके मल्टी पेज TIFF को BMP में बदलें
url: /hi/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java का उपयोग करके मल्टी पेज TIFF को BMP में बदलें

यदि आपको Java वातावरण में काम करते हुए **multi page tiff** फ़ाइलों को व्यक्तिगत BMP छवियों में बदलने की आवश्यकता है, तो आप सही जगह पर आए हैं। इस ट्यूटोरियल में हम प्रत्येक TIFF फ्रेम को निकालने और उसे Aspose.Imaging for Java लाइब्रेरी का उपयोग करके BMP फ़ाइल के रूप में सहेजने के सटीक चरणों को दिखाएंगे। अंत तक, आप न केवल प्रोग्रामेटिक रूप से *tiff फ़ाइलों को कैसे बदलें* समझेंगे, बल्कि यह भी जानेंगे कि यह तरीका बैच इमेज प्रोसेसिंग कार्यों के लिए क्यों विश्वसनीय है।

## त्वरित उत्तर
- **TIFF से BMP रूपांतरण के लिए सबसे अच्छा लाइब्रेरी कौन सा है?** Aspose.Imaging for Java  
- **कोड की कितनी पंक्तियों की आवश्यकता है?** लगभग 30 पंक्तियाँ पाँच तार्किक चरणों में  
- **क्या उत्पादन के लिए लाइसेंस चाहिए?** हाँ, एक व्यावसायिक लाइसेंस आवश्यक है (नि:शुल्क ट्रायल उपलब्ध)  
- **क्या यह बड़े मल्टी‑पेज TIFF को संभाल सकता है?** हाँ, API फ्रेम्स को कुशलता से स्ट्रीम करता है  
- **कौन सा Java संस्करण समर्थित है?** Java 8 और उसके बाद के संस्करण  

## “convert multi page tiff” क्या है?
मल्टी‑पेज TIFF को बदलना का अर्थ है एक ही TIFF कंटेनर में संग्रहीत प्रत्येक पेज (या फ्रेम) को निकालकर उसे एक स्वतंत्र छवि फ़ाइल—यहाँ BMP—के रूप में निर्यात करना। यह दस्तावेज़ अभिलेखन, मेडिकल इमेजिंग, या किसी भी कार्यप्रवाह के लिए उपयोगी है जिसमें आगे की प्रोसेसिंग के लिए रास्टर छवियों की आवश्यकता होती है।

## Aspose.Imaging for Java का उपयोग क्यों करें?
- **पूर्ण फ़ॉर्मेट समर्थन** – TIFF, BMP, JPEG, PNG, और कई अन्य को संभालता है।  
- **कोई बाहरी निर्भरताएँ नहीं** – शुद्ध Java, कोई नेटिव लाइब्रेरी नहीं।  
- **उच्च प्रदर्शन** – फ्रेम्स तक स्ट्रीम्ड एक्सेस मेमोरी उपयोग को कम करता है।  
- **समृद्ध API** – पिक्सेल डेटा, रंग गहराई, और मेटाडेटा पर सूक्ष्म नियंत्रण प्रदान करता है।

## पूर्वापेक्षाएँ

1. **Java विकास वातावरण** – JDK 8+ और आपका पसंदीदा IDE।  
2. **Aspose.Imaging for Java** – आधिकारिक साइट से नवीनतम JAR **[here](https://releases.aspose.com/imaging/java/)** डाउनलोड करें।  
3. **नमूना मल्टी‑पेज TIFF** – एक TIFF फ़ाइल (जैसे, `sample.tiff`) को ऐसी निर्देशिका में रखें जिसे आपका कोड पढ़ सके।

## पैकेज आयात करें

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## Aspose.Imaging के साथ मल्टी पेज TIFF को BMP में कैसे बदलें

### चरण 1: TIFF छवि लोड करें और फ्रेम काउंटर प्रारंभ करें

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // Create an instance of int to keep track of frames in TiffImage
    int frameCounter = 0;
```

### चरण 2: TIFF फ्रेम्स पर इटररेट करें

```java
    // Iterate over the TiffFrames in TiffImage
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

### चरण 3: TiffFrame के पिक्सेल को रंगों की एरे में लोड करें

```java
        // Load Pixels of TiffFrame into an array of Colors
        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
```

### चरण 4: BMP विकल्प बनाएं और बिट्स प्रति पिक्सेल सेट करें

```java
        // Create an instance of bmpCreateOptions
        try (BmpOptions bmpCreateOptions = new BmpOptions())
        {
            bmpCreateOptions.setBitsPerPixel(24);
```

### चरण 5: BMP छवि सहेजें

```java
            // Set the Source of bmpCreateOptions as FileCreateSource by specifying the location where output will be saved
            bmpCreateOptions.setSource(new FileCreateSource(String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "Your Document Directory", frameCounter), false));
            // Create a new bmpImage
            try (BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight()))
            {
                // Save the bmpImage with pixels from TiffFrame
                bmpImage.savePixels(tiffFrame.getBounds(), pixels);
                bmpImage.save();
            }
        }
        frameCounter++;
    }
}
```

## सामान्य समस्याएँ और सुझाव

- **मेमोरी उपयोग:** बहुत बड़े TIFF फ़ाइलों के साथ काम करते समय, पूरे चित्र को मेमोरी में लोड करने के बजाय (जैसा कि दिखाया गया है) एक बार में एक फ्रेम प्रोसेस करने पर विचार करें।  
- **फ़ाइल नामकरण:** `String.format` कॉल प्रत्येक फ्रेम के लिए एक अनूठा फ़ाइलनाम बनाता है (`...out0.bmp`, `...out1.bmp`, आदि)। यदि आपको अलग नामकरण नियम चाहिए तो पैटर्न को समायोजित करें।  
- **बिट गहराई:** BMP विभिन्न बिट गहराइयों को समर्थन देता है; अधिकांश परिदृश्यों के लिए 24‑bit (सच्चा रंग) उपयुक्त है। यदि आपको 8‑bit ग्रेस्केल आउटपुट चाहिए तो `setBitsPerPixel` बदलें।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: Aspose.Imaging for Java क्या है?

A1: Aspose.Imaging for Java एक Java लाइब्रेरी है जो व्यापक इमेज प्रोसेसिंग क्षमताएँ प्रदान करती है, जिससे आप विभिन्न इमेज फ़ॉर्मेट के साथ काम कर सकते हैं और रूपांतरण, संपादन, तथा हेरफेर जैसे कार्य कर सकते हैं।

### प्रश्न 2: क्या मैं Aspose.Imaging for Java को विभिन्न इमेज फ़ॉर्मेट के साथ उपयोग कर सकता हूँ?

A2: हाँ, Aspose.Imaging for Java कई इमेज फ़ॉर्मेट का समर्थन करता है, जिसमें TIFF, BMP, JPEG, PNG, और कई अन्य शामिल हैं, जिससे यह इमेज‑संबंधित कार्यों के लिए एक बहुमुखी टूल बनता है।

### प्रश्न 3: Aspose.Imaging for Java के लिए दस्तावेज़ीकरण कहाँ मिल सकता है?

A3: आप Aspose.Imaging for Java के विस्तृत दस्तावेज़ीकरण **[here](https://reference.aspose.com/imaging/java/)** पर पा सकते हैं।

### प्रश्न 4: क्या Aspose.Imaging for Java के लिए कोई नि:शुल्क ट्रायल उपलब्ध है?

A4: हाँ, आप Aspose.Imaging for Java को नि:शुल्क ट्रायल के साथ **[here](https://releases.aspose.com/)** एक्सप्लोर कर सकते हैं।

### प्रश्न 5: Aspose.Imaging for Java के लिए समर्थन कैसे प्राप्त करें?

A5: किसी भी प्रश्न, समस्या, या समर्थन के लिए आप सपोर्ट फ़ोरम **[here](https://forum.aspose.com/)** पर जा सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

**Q:** क्या मैं उसी दृष्टिकोण का उपयोग करके मल्टी‑पेज TIFF को अन्य फ़ॉर्मेट (जैसे PNG) में बदल सकता हूँ?  
**A:** बिल्कुल। `BmpOptions` को उपयुक्त विकल्प क्लास (जैसे `PngOptions`) से बदलें और `FileCreateSource` पाथ में फ़ाइल एक्सटेंशन को समायोजित करें।

**Q:** क्या Aspose.Imaging संकुचित TIFFs (LZW, CCITT) को संभालता है?  
**A:** हाँ, लाइब्रेरी फ्रेम एक्सट्रैक्शन के दौरान समर्थित TIFF संपीड़न योजनाओं को पारदर्शी रूप से डिकम्प्रेस करती है।

**Q:** क्या BMP में बदलते समय EXIF मेटाडेटा को संरक्षित किया जा सकता है?  
**A:** BMP EXIF मेटाडेटा को समर्थन नहीं देता। यदि आपको मेटाडेटा रखना है, तो PNG जैसे फ़ॉर्मेट में बदलने या रूपांतरण के बाद मेटाडेटा को मैन्युअली कॉपी करने पर विचार करें।

**Q:** फ़ोल्डर में कई TIFF फ़ाइलों को बैच‑प्रोसेस कैसे करें?  
**A:** ऊपर दिया गया कोड एक लूप में रखें जो किसी निर्देशिका के `File` ऑब्जेक्ट्स पर इटररेट करे, प्रत्येक फ़ाइल के लिए `dataDir` और स्रोत फ़ाइलनाम को अपडेट करे।

**Q:** व्यावसायिक तैनाती के लिए कौन सा लाइसेंस चाहिए?  
**A:** उत्पादन उपयोग के लिए एक भुगतान किया गया Aspose.Imaging for Java लाइसेंस आवश्यक है। विकास के दौरान एक अस्थायी ट्रायल लाइसेंस का उपयोग किया जा सकता है।

**Last Updated:** 2026-05-03  
**Tested With:** Aspose.Imaging for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}