---
title: Aspose.Imaging के साथ जावा में रैस्टर इमेज को TIFF में बदलें
linktitle: रेखापुंज छवि TIFF रूपांतरण
second_title: Aspose.Imaging जावा इमेज प्रोसेसिंग एपीआई
description: जावा के लिए Aspose.Imaging का उपयोग करके जावा में रेखापुंज छवियों को TIFF प्रारूप में परिवर्तित करना सीखें। छवि हेरफेर के लिए एक व्यापक मार्गदर्शिका।
type: docs
weight: 20
url: /hi/java/image-conversion-and-optimization/raster-image-tiff-conversion/
---
यदि आप अपने जावा एप्लिकेशन में रैस्टर छवियों में हेरफेर करना और परिवर्तित करना चाहते हैं, तो जावा के लिए Aspose.Imaging एक आदर्श उपकरण है। यह चरण-दर-चरण ट्यूटोरियल जावा के लिए Aspose.Imaging का उपयोग करके एक रेखापुंज छवि को TIFF प्रारूप में परिवर्तित करने की प्रक्रिया में आपका मार्गदर्शन करेगा। इससे पहले कि हम विवरण में उतरें, आइए देखें कि आरंभ करने के लिए आपको क्या चाहिए।

## आवश्यक शर्तें

इससे पहले कि आप रेखापुंज छवियों को टीआईएफएफ में परिवर्तित करना शुरू करें, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ हैं:

### 1. जावा विकास पर्यावरण

सुनिश्चित करें कि आपके सिस्टम पर जावा डेवलपमेंट किट (जेडीके) स्थापित है। आप इसे Oracle वेबसाइट से डाउनलोड कर सकते हैं।

### 2. जावा के लिए Aspose.Imaging

 आपको जावा के लिए Aspose.Imaging प्राप्त करने की आवश्यकता होगी, जो विभिन्न छवि प्रारूपों के साथ काम करने के लिए आवश्यक एपीआई प्रदान करता है। आप इसे यहां से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/imaging/java/).

### 3. बुनियादी जावा ज्ञान

यह ट्यूटोरियल मानता है कि आपको जावा प्रोग्रामिंग की बुनियादी समझ है। आपको कक्षाओं, वस्तुओं और विधि कॉल जैसी अवधारणाओं से परिचित होना चाहिए।

## पैकेज आयात करें

आरंभ करने के लिए, आपको जावा पैकेज के लिए आवश्यक Aspose.Imaging को अपने जावा प्रोग्राम में आयात करना होगा। यहां बताया गया है कि आप ऐसा कैसे कर सकते हैं:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.TiffOptions;
import com.aspose.imaging.imageoptions.TiffExpectedFormat;
import com.aspose.imaging.imageoptions.TiffPhotometrics;
import com.aspose.imaging.imageoptions.TiffRational;
import com.aspose.imaging.imageoptions.TiffResolutionUnits;
import com.aspose.imaging.imageoptions.TiffPlanarConfigs;
import com.aspose.imaging.imageoptions.TiffCompressions;
import com.aspose.imaging.RasterImage;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
```

## चरण 1: पर्यावरण स्थापित करें

 पहला कदम पर्यावरण स्थापित करना है। अपने प्रोजेक्ट के लिए एक निर्देशिका बनाएं और उसमें वह रैस्टर छवि रखें जिसे आप TIFF में कनवर्ट करना चाहते हैं। आप प्रतिस्थापित कर सकते हैं`"Your Document Directory"` आपकी प्रोजेक्ट निर्देशिका के वास्तविक पथ के साथ।

```java
String dataDir = "Your Document Directory" + "ModifyingImages/";
```

## चरण 2: टिफऑप्शंस बनाएं

अब, का एक उदाहरण बनाएं`TiffOptions` और TIFF प्रारूप के लिए इसके विभिन्न गुण सेट करें। आप इन विकल्पों को अपनी आवश्यकताओं के अनुसार अनुकूलित कर सकते हैं।

```java
TiffOptions options = new TiffOptions(TiffExpectedFormat.Default);
options.setBitsPerSample(new int[] { 8, 8, 8 });
options.setPhotometric(TiffPhotometrics.Rgb);
options.setXresolution(new TiffRational(72));
options.setYresolution(new TiffRational(72));
options.setResolutionUnit(TiffResolutionUnits.Inch);
options.setPlanarConfiguration(TiffPlanarConfigs.Contiguous);
options.setCompression(TiffCompressions.AdobeDeflate);
```

## चरण 3: छवि लोड करें

 उस मौजूदा छवि को लोड करें जिसे आप एक उदाहरण में बदलना चाहते हैं`RasterImage`. अपनी छवि फ़ाइल का पथ निर्दिष्ट करना सुनिश्चित करें।

```java
try (RasterImage image = (RasterImage) Image.load(dataDir + "SampleTiff1.tiff")) {
```

## चरण 4: टिफ़इमेज बनाएं और सहेजें

 कोई नया बनाएं`TiffImage` से`RasterImage` और उदाहरण पास करते समय परिणामी छवि को सहेजें`TiffOptions`. आप वह पथ भी निर्दिष्ट कर सकते हैं जहां आप परिवर्तित TIFF छवि को सहेजना चाहते हैं।

```java
    try (TiffImage tiffImage = new TiffImage(new TiffFrame(image))) {
        tiffImage.save("Your Document Directory" + "SavingRasterImage_out.tiff", options);
    }
}
```

इतना ही! आपने जावा के लिए Aspose.Imaging का उपयोग करके एक रैस्टर छवि को TIFF प्रारूप में सफलतापूर्वक परिवर्तित कर लिया है।

## निष्कर्ष

इस ट्यूटोरियल में, आपने सीखा कि जावा के लिए Aspose.Imaging का उपयोग करके एक रैस्टर छवि को TIFF प्रारूप में कैसे परिवर्तित किया जाए। यह शक्तिशाली लाइब्रेरी आपको आसानी से छवियों में हेरफेर करने और बदलने की अनुमति देती है। चाहे आप छवि प्रसंस्करण, दस्तावेज़ रूपांतरण, या किसी अन्य एप्लिकेशन पर काम कर रहे हों जिसमें छवियां शामिल हों, जावा के लिए Aspose.Imaging आपके टूलकिट में एक मूल्यवान उपकरण है।

 अब आप अपने जावा अनुप्रयोगों में छवियों के साथ काम करने के लिए जावा के लिए Aspose.Imaging का पूरा लाभ उठा सकते हैं। अधिक सुविधाओं और संभावनाओं के लिए दस्तावेज़ देखें[जावा दस्तावेज़ीकरण के लिए Aspose.Imaging](https://reference.aspose.com/imaging/java/).

## अक्सर पूछे जाने वाले प्रश्न

### Q1: जावा के लिए Aspose.Imaging किस छवि प्रारूप का समर्थन करता है?
जावा के लिए Aspose.Imaging JPEG, PNG, TIFF, BMP, GIF और कई अन्य सहित छवि प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है। समर्थित प्रारूपों की पूरी सूची के लिए दस्तावेज़ की जाँच करें।

### Q2: क्या मैं जावा के लिए Aspose.Imaging के साथ छवि संपादन कार्य कर सकता हूँ?

उ2: हां, आप जावा के लिए Aspose.Imaging का उपयोग करके विभिन्न छवि संपादन कार्य कर सकते हैं जैसे आकार बदलना, काटना, घुमाना और बहुत कुछ।

### Q3: मैं जावा के लिए Aspose.Imaging के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

 A3:आप विजिट करके अस्थायी लाइसेंस प्राप्त कर सकते हैं[अस्थायी लाइसेंस प्रदान करें](https://purchase.aspose.com/temporary-license/).

### Q4: क्या जावा के लिए Aspose.Imaging का कोई निःशुल्क परीक्षण उपलब्ध है?

 उ4: हां, आप जावा के लिए Aspose.Imaging के निःशुल्क परीक्षण तक पहुंच सकते हैं[Aspose.इमेजिंग नि:शुल्क परीक्षण](https://releases.aspose.com/).

### Q5: मैं जावा के लिए Aspose.Imaging के बारे में समर्थन कहां से प्राप्त कर सकता हूं या प्रश्न पूछ सकता हूं?

 A5: आप Aspose.Imaging समुदाय में शामिल हो सकते हैं और समर्थन प्राप्त कर सकते हैं[Aspose.इमेजिंग फोरम](https://forum.aspose.com/).