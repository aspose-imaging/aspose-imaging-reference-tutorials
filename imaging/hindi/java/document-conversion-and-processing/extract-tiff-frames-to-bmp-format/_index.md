---
date: 2025-12-19
description: Aspose.Imaging के साथ जावा में TIFF को BMP में कैसे बदलें सीखें। यह चरण‑दर‑चरण
  जावा इमेज प्रोसेसिंग ट्यूटोरियल मल्टी‑पेज TIFF फ़ाइलों के लिए इमेज कन्वर्ज़न दिखाता
  है।
linktitle: Extract TIFF Frames to BMP Format
second_title: Aspose.Imaging Java Image Processing API
title: Aspose.Imaging for Java का उपयोग करके TIFF को BMP में कैसे परिवर्तित करें
url: /hi/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java के साथ TIFF को BMP में बदलें

यदि आपको Java एप्लिकेशन के भीतर **convert tiff to bmp** करने की आवश्यकता है, तो आप सही जगह पर हैं। चाहे आप एकल‑पृष्ठ TIFF या बहु‑पृष्ठ दस्तावेज़ को संभाल रहे हों, Aspose.Imaging for Java प्रक्रिया को सरल और विश्वसनीय बनाता है। इस ट्यूटोरियल में हम एक TIFF फ़ाइल से प्रत्येक फ्रेम निकालने और उसे व्यक्तिगत BMP इमेज के रूप में सहेजने की प्रक्रिया दिखाएंगे—इमेज कन्वर्ज़न java परिदृश्यों के लिए आदर्श।

## त्वरित उत्तर
- **कौन सा लाइब्रेरी रूपांतरण संभालती है?** Aspose.Imaging for Java  
- **क्या यह मल्टी‑पेज TIFFs को प्रोसेस कर सकता है?** हाँ – प्रत्येक फ्रेम को अलग BMP के रूप में सहेजा जाता है  
- **क्या उत्पादन के लिए लाइसेंस चाहिए?** व्यावसायिक उपयोग के लिए एक वैध Aspose लाइसेंस आवश्यक है  
- **कौन सा Java संस्करण समर्थित है?** Java 8 या उससे ऊपर  
- **कोड चलने में कितना समय लगता है?** सामान्य‑आकार की इमेज के लिए आमतौर पर कुछ सेकंड  

## पूर्वापेक्षाएँ

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

1. **Java Development Environment** – एक कार्यशील JDK (8 या नया) और आपका पसंदीदा IDE या बिल्ड टूल।  
2. **Aspose.Imaging for Java** – वेबसाइट से नवीनतम JAR डाउनलोड करें [here](https://releases.aspose.com/imaging/java/).  
3. **Sample TIFF Image** – एक TIFF फ़ाइल (सिंगल‑ या मल्टी‑पेज) जिसे आपके प्रोजेक्ट की कार्य निर्देशिका में रखें।  

## पैकेज आयात करें

प्रक्रिया शुरू करने के लिए, आपको अपने Java एप्लिकेशन के लिए आवश्यक पैकेज आयात करने होंगे:

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## convert tiff to bmp के लिए चरण‑दर‑चरण गाइड

### चरण 1: TIFF इमेज लोड करें और फ्रेम काउंटर प्रारंभ करें

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

### चरण 5: BMP इमेज सहेजें

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

## Aspose.Imaging for Java का उपयोग क्यों करें?

- **Robust multi‑page support** – अतिरिक्त कोड के बिना किसी भी संख्या में TIFF फ्रेम्स को संभालता है।  
- **Pure Java implementation** – कोई नेटिव डिपेंडेंसी नहीं, जिससे यह क्रॉस‑प्लेटफ़ॉर्म डिप्लॉयमेंट के लिए आदर्श है।  
- **High‑quality BMP output** – आप बिट्स‑पर‑पिक्सेल, कंप्रेशन और कलर डेप्थ को नियंत्रित कर सकते हैं।  
- **Comprehensive image conversion java toolkit** – JPEG, PNG, GIF और कई अन्य फ़ॉर्मैट्स के साथ काम करता है।  

## सामान्य समस्याएँ और ट्रबलशूटिंग

| लक्षण | संभावित कारण | समाधान |
|---------|--------------|-----|
| `OutOfMemoryError` बड़े TIFF लोड करते समय | पूरा इमेज मेमोरी में लोड हो रहा है | फ़्रेम्स को एक‑एक करके प्रोसेस करें जैसा दिखाया गया है, या JVM हीप साइज (`-Xmx`) बढ़ाएँ |
| BMP फ़ाइल भ्रष्ट है | गलत `BitsPerPixel` मान | सही‑रंग BMPs के लिए 24 या 32 का उपयोग करें |
| कोई आउटपुट फ़ाइलें नहीं बनीं | गलत आउटपुट डायरेक्टरी पाथ | `Your Document Directory` किसी मौजूदा फ़ोल्डर की ओर इशारा करता है, इसे सत्यापित करें |

## अक्सर पूछे जाने वाले प्रश्न

### Q1: Aspose.Imaging for Java क्या है?

A1: Aspose.Imaging for Java एक Java लाइब्रेरी है जो व्यापक इमेज प्रोसेसिंग क्षमताएँ प्रदान करती है, जिससे आप विभिन्न इमेज फ़ॉर्मैट्स के साथ काम कर सकते हैं और रूपांतरण, संपादन, तथा हेरफेर जैसे कार्य कर सकते हैं।

### Q2: क्या मैं Aspose.Imaging for Java को विभिन्न इमेज फ़ॉर्मैट्स के साथ उपयोग कर सकता हूँ?

A2: हाँ, Aspose.Imaging for Java कई इमेज फ़ॉर्मैट्स को सपोर्ट करता है, जिसमें TIFF, BMP, JPEG, PNG और कई अन्य शामिल हैं, जिससे यह इमेज‑संबंधित कार्यों के लिए एक बहुमुखी टूल बनता है।

### Q3: मैं Aspose.Imaging for Java की डॉक्यूमेंटेशन कहाँ पा सकता हूँ?

A3: आप Aspose.Imaging for Java की विस्तृत डॉक्यूमेंटेशन [here](https://reference.aspose.com/imaging/java/) पर पा सकते हैं।

### Q4: क्या Aspose.Imaging for Java के लिए कोई फ्री ट्रायल उपलब्ध है?

A4: हाँ, आप Aspose.Imaging for Java को फ्री ट्रायल के साथ [here](https://releases.aspose.com/) पर एक्सप्लोर कर सकते हैं।

### Q5: मैं Aspose.Imaging for Java के लिए सपोर्ट कैसे प्राप्त करूँ?

A5: Aspose.Imaging for Java से संबंधित किसी भी प्रश्न, समस्या या सपोर्ट के लिए आप सपोर्ट फ़ोरम [here](https://forum.aspose.com/) पर जा सकते हैं।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**अंतिम अपडेट:** 2025-12-19  
**परीक्षण किया गया संस्करण:** Aspose.Imaging for Java 24.12 (latest)  
**लेखक:** Aspose