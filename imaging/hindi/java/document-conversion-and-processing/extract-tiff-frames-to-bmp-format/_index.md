---
title: जावा के लिए Aspose.Imaging के साथ TIFF से BMP रूपांतरण
linktitle: TIFF फ्रेम्स को BMP फॉर्मेट में निकालें
second_title: Aspose.Imaging जावा इमेज प्रोसेसिंग एपीआई
description: जावा के लिए Aspose.Imaging का उपयोग करके जावा में TIFF फ्रेम को BMP प्रारूप में निकालने का तरीका जानें। हमारे चरण-दर-चरण मार्गदर्शिका का पालन करें.
type: docs
weight: 13
url: /hi/java/document-conversion-and-processing/extract-tiff-frames-to-bmp-format/
---
यदि आप जावा में छवि फ़ाइलों, विशेष रूप से टीआईएफएफ छवियों के साथ काम कर रहे हैं, और उनसे फ्रेम निकालने और उन्हें बीएमपी प्रारूप में सहेजने की आवश्यकता है, तो जावा के लिए Aspose.Imaging इसे प्राप्त करने के लिए एक शक्तिशाली और बहुमुखी उपकरण है। इस चरण-दर-चरण मार्गदर्शिका में, हम आपको जावा के लिए Aspose.Imaging का उपयोग करके TIFF फ़्रेम को BMP प्रारूप में निकालने की प्रक्रिया के बारे में बताएंगे।

## आवश्यक शर्तें

आरंभ करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

1. जावा विकास पर्यावरण: आपके सिस्टम पर एक कार्यशील जावा विकास वातावरण स्थापित होना चाहिए।

2.  जावा के लिए Aspose.Imaging: सुनिश्चित करें कि आपके पास Java लाइब्रेरी के लिए Aspose.Imaging स्थापित है। आप इसे वेबसाइट से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/imaging/java/).

3. नमूना TIFF छवि: एक नमूना TIFF छवि फ़ाइल रखें जिससे आप फ़्रेम निकालना चाहते हैं। सुनिश्चित करें कि यह छवि आपकी कार्यशील निर्देशिका में उपलब्ध हो।

## पैकेज आयात करें

प्रक्रिया शुरू करने के लिए, आपको अपने जावा एप्लिकेशन के लिए आवश्यक पैकेज आयात करने होंगे:

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
    // TiffImage में फ़्रेम का ट्रैक रखने के लिए int का एक उदाहरण बनाएं
    int frameCounter = 0;
```

## चरण 2: TIFF फ़्रेमों पर पुनरावृति करें

```java
    // TiffImage में TiffFrames पर पुनरावृति करें
    for (TiffFrame tiffFrame : multiImage.getFrames())
    {
        multiImage.setActiveFrame(tiffFrame);
```

## चरण 3: टिफ़फ़्रेम के पिक्सेल को रंगों की एक श्रृंखला में लोड करें

```java
        // टिफ़फ़्रेम के पिक्सेल को रंगों की एक श्रृंखला में लोड करें
        Color[] pixels = multiImage.loadPixels(tiffFrame.getBounds());
```

## चरण 4: बीएमपी विकल्प बनाएं और प्रति पिक्सेल बिट्स सेट करें

```java
        // BmpCreateOptions का एक उदाहरण बनाएं
        try (BmpOptions bmpCreateOptions = new BmpOptions())
        {
            bmpCreateOptions.setBitsPerPixel(24);
```

## चरण 5: बीएमपी छवि सहेजें

```java
            // उस स्थान को निर्दिष्ट करके जहां आउटपुट सहेजा जाएगा, bmpCreateOptions के स्रोत को FileCreateSource के रूप में सेट करें
            bmpCreateOptions.setSource(new FileCreateSource(String.format("%sConcatExtractTIFFFramesToBMP_out%d.bmp", "Your Document Directory", frameCounter), false));
            // एक नया bmpImage बनाएं
            try (BmpImage bmpImage = (BmpImage) Image.create(bmpCreateOptions, tiffFrame.getWidth(), tiffFrame.getHeight()))
            {
                // BmpImage को TiffFrame से पिक्सेल के साथ सहेजें
                bmpImage.savePixels(tiffFrame.getBounds(), pixels);
                bmpImage.save();
            }
        }
        frameCounter++;
    }
}
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने जावा के लिए Aspose.Imaging का उपयोग करके TIFF फ़्रेमों को निकालने और उन्हें BMP छवियों के रूप में सहेजने का तरीका बताया है। सही पूर्वापेक्षाओं के साथ और चरण-दर-चरण मार्गदर्शिका का पालन करते हुए, आप अपने जावा एप्लिकेशन में इस छवि रूपांतरण कार्य को आसानी से कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: जावा के लिए Aspose.Imaging क्या है?

A1: जावा के लिए Aspose.Imaging एक जावा लाइब्रेरी है जो व्यापक छवि प्रसंस्करण क्षमताएं प्रदान करती है, जो आपको विभिन्न छवि प्रारूपों के साथ काम करने और रूपांतरण, संपादन और हेरफेर जैसे कार्य करने की अनुमति देती है।

### Q2: क्या मैं जावा के लिए विभिन्न छवि प्रारूपों के साथ Aspose.Imaging का उपयोग कर सकता हूँ?

A2: हां, जावा के लिए Aspose.Imaging TIFF, BMP, JPEG, PNG और कई अन्य सहित छवि प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है, जो इसे छवि-संबंधित कार्यों के लिए एक बहुमुखी उपकरण बनाता है।

### Q3: मैं जावा के लिए Aspose.Imaging के लिए दस्तावेज़ कहां पा सकता हूं?

 A3: आप Java के लिए Aspose.Imaging के लिए विस्तृत दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/imaging/java/).

### Q4: क्या जावा के लिए Aspose.Imaging का कोई निःशुल्क परीक्षण उपलब्ध है?

A4: हां, आप निःशुल्क परीक्षण के साथ जावा के लिए Aspose.Imaging का पता लगा सकते हैं[यहाँ](https://releases.aspose.com/).

### Q5: मैं जावा के लिए Aspose.Imaging के लिए समर्थन कैसे प्राप्त करूं?

 A5: जावा के लिए Aspose.Imaging से संबंधित किसी भी प्रश्न, समस्या या समर्थन के लिए, आप सहायता फ़ोरम पर जा सकते हैं[यहाँ](https://forum.aspose.com/).