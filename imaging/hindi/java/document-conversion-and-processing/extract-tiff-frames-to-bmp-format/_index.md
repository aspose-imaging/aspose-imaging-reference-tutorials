---
"description": "Aspose.Imaging for Java का उपयोग करके Java में TIFF फ़्रेम को BMP फ़ॉर्मेट में निकालने का तरीका जानें। हमारे चरण-दर-चरण मार्गदर्शिका का पालन करें।"
"linktitle": "TIFF फ़्रेम को BMP प्रारूप में निकालें"
"second_title": "Aspose.Imaging जावा इमेज प्रोसेसिंग API"
"title": "Java के लिए Aspose.Imaging के साथ TIFF से BMP रूपांतरण"
"url": "/hi/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/"
"weight": 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Java के लिए Aspose.Imaging के साथ TIFF से BMP रूपांतरण

यदि आप जावा में इमेज फ़ाइलों, विशेष रूप से TIFF इमेज के साथ काम कर रहे हैं, और उनसे फ़्रेम निकालने और उन्हें BMP फ़ॉर्मेट में सहेजने की आवश्यकता है, तो Aspose.Imaging for Java ऐसा करने के लिए एक शक्तिशाली और बहुमुखी उपकरण है। इस चरण-दर-चरण मार्गदर्शिका में, हम आपको Aspose.Imaging for Java का उपयोग करके TIFF फ़्रेम को BMP फ़ॉर्मेट में निकालने की प्रक्रिया से परिचित कराएँगे।

## आवश्यक शर्तें

आरंभ करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

1. जावा विकास वातावरण: आपके सिस्टम पर एक कार्यशील जावा विकास वातावरण स्थापित होना चाहिए।

2. Aspose.Imaging for Java: सुनिश्चित करें कि आपके पास Aspose.Imaging for Java लाइब्रेरी स्थापित है। आप इसे वेबसाइट से डाउनलोड कर सकते हैं [यहाँ](https://releases.aspose.com/imaging/java/).

3. नमूना TIFF छवि: एक नमूना TIFF छवि फ़ाइल रखें जिससे आप फ़्रेम निकालना चाहते हैं। सुनिश्चित करें कि यह छवि आपकी कार्यशील निर्देशिका में उपलब्ध है।

## पैकेज आयात करें

प्रक्रिया शुरू करने के लिए, आपको अपने जावा अनुप्रयोग के लिए आवश्यक पैकेज आयात करने होंगे:

```java
import com.aspose.imaging.Color;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.sources.FileCreateSource;
```

## चरण 1: TIFF छवि लोड करें और फ़्रेम काउंटर प्रारंभ करें

```java
// दस्तावेज़ निर्देशिका का पथ.
String dataDir = "Your Document Directory" + "ConvertingImages/";

try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "sample.tiff"))
{
    // TiffImage में फ़्रेम का ट्रैक रखने के लिए int का एक उदाहरण बनाएँ
    int frameCounter = 0;
```

## चरण 2: TIFF फ़्रेम पर पुनरावृति करें

```java
    // TiffImage में TiffFrames पर पुनरावृति करें
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

## चरण 3: TiffFrame के पिक्सेल को रंगों की एक सरणी में लोड करें

```java
        // TiffFrame के पिक्सेल को रंगों की एक सरणी में लोड करें
        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
```

## चरण 4: BMP विकल्प बनाएं और प्रति पिक्सेल बिट्स सेट करें

```java
        // bmpCreateOptions का एक उदाहरण बनाएँ
        try (BmpOptions bmpCreateOptions = new BmpOptions())
        {
            bmpCreateOptions.setBitsPerPixel(24);
```

## चरण 5: BMP छवि सहेजें

```java
            // आउटपुट को सहेजने के लिए स्थान निर्दिष्ट करके bmpCreateOptions के स्रोत को FileCreateSource के रूप में सेट करें
            bmpCreateOptions.setSource(new FileCreateSource(String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "Your Document Directory", frameCounter), false));
            // एक नया bmpImage बनाएं
            try (BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight()))
            {
                // TiffFrame से पिक्सेल के साथ bmpImage को सहेजें
                bmpImage.savePixels(tiffFrame.getBounds(), pixels);
                bmpImage.save();
            }
        }
        frameCounter++;
    }
}
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने बताया है कि Aspose.Imaging for Java का उपयोग करके TIFF फ़्रेम कैसे निकालें और उन्हें BMP इमेज के रूप में कैसे सेव करें। सही पूर्वापेक्षाओं और चरण-दर-चरण मार्गदर्शिका का पालन करके, आप अपने Java एप्लिकेशन में इस इमेज रूपांतरण कार्य को आसानी से कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: Java के लिए Aspose.Imaging क्या है?

A1: Aspose.Imaging for Java एक जावा लाइब्रेरी है जो व्यापक छवि प्रसंस्करण क्षमताएं प्रदान करती है, जिससे आप विभिन्न छवि प्रारूपों के साथ काम कर सकते हैं और रूपांतरण, संपादन और हेरफेर जैसे कार्य कर सकते हैं।

### प्रश्न 2: क्या मैं विभिन्न छवि प्रारूपों के साथ Java के लिए Aspose.Imaging का उपयोग कर सकता हूं?

A2: हां, Aspose.Imaging for Java TIFF, BMP, JPEG, PNG और कई अन्य सहित छवि प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है, जो इसे छवि-संबंधित कार्यों के लिए एक बहुमुखी उपकरण बनाता है।

### प्रश्न 3: मैं Aspose.Imaging for Java के लिए दस्तावेज़ कहां पा सकता हूं?

A3: आप Java के लिए Aspose.Imaging के लिए विस्तृत दस्तावेज़ पा सकते हैं [यहाँ](https://reference.aspose.com/imaging/java/).

### प्रश्न 4: क्या Aspose.Imaging for Java के लिए कोई निःशुल्क परीक्षण उपलब्ध है?

A4: हाँ, आप Aspose.Imaging for Java का निःशुल्क परीक्षण कर सकते हैं [यहाँ](https://releases.aspose.com/).

### प्रश्न 5: मैं Java के लिए Aspose.Imaging का समर्थन कैसे प्राप्त करूं?

A5: Aspose.Imaging for Java से संबंधित किसी भी प्रश्न, समस्या या सहायता के लिए, आप सहायता फ़ोरम पर जा सकते हैं [यहाँ](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}