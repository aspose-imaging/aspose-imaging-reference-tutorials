---
title: जावा के लिए Aspose.Imaging के साथ ODG को PNG और PDF में बदलें
linktitle: ओडीजी फ़ाइल प्रारूप समर्थन
second_title: Aspose.Imaging जावा इमेज प्रोसेसिंग एपीआई
description: जावा के लिए Aspose.Imaging के साथ ODG फ़ाइलों को PNG और PDF में परिवर्तित करना सीखें। कुशल रूपांतरण के लिए हमारी चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 12
url: /hi/java/metafile-and-vector-image-handling/odg-file-format-support/
---
दस्तावेज़ रूपांतरण की दुनिया में, जावा के लिए Aspose.Imaging एक शक्तिशाली उपकरण के रूप में सामने आता है जो आपको ODG (OpenDocument ग्राफ़िक्स) फ़ाइलों को PNG और PDF स्वरूपों में आसानी से परिवर्तित करने की अनुमति देता है। यह ट्यूटोरियल जावा के लिए Aspose.Imaging का उपयोग करते हुए, चरण दर चरण प्रक्रिया में आपका मार्गदर्शन करेगा। चाहे आप एक डेवलपर हों या केवल ODG फ़ाइलों को कनवर्ट करना चाह रहे हों, यह लेख आपको अपना लक्ष्य प्राप्त करने में मदद करेगा।

## आवश्यक शर्तें

इससे पहले कि हम रूपांतरण प्रक्रिया में उतरें, आपको यह सुनिश्चित करना होगा कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

### 1. जावा विकास पर्यावरण

 सुनिश्चित करें कि आपके सिस्टम पर जावा डेवलपमेंट वातावरण स्थापित है। आप नवीनतम जावा डेवलपमेंट किट (जेडीके) को डाउनलोड और इंस्टॉल कर सकते हैं[ओरेकल वेबसाइट](https://www.oracle.com/java/technologies/javase-downloads).

### 2. जावा के लिए Aspose.Imaging

 आपको जावा के लिए Aspose.Imaging को डाउनलोड और इंस्टॉल करना होगा। आप नवीनतम संस्करण यहां पा सकते हैं[जावा डाउनलोड पेज के लिए Aspose.Imaging](https://releases.aspose.com/imaging/java/).

### 3. ओडीजी फ़ाइलें

बेशक, आपको उन ODG फ़ाइलों की आवश्यकता होगी जिन्हें आप कनवर्ट करना चाहते हैं। सुनिश्चित करें कि ये फ़ाइलें आपके सिस्टम पर एक निर्देशिका में उपलब्ध हैं।

## पैकेज आयात करें

अब जब आपको आवश्यक शर्तें मिल गई हैं, तो आइए अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करना शुरू करें। ये पैकेज आपको जावा के लिए Aspose.Imaging के साथ प्रभावी ढंग से काम करने की अनुमति देंगे।

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.SizeF;
import com.aspose.imaging.imageoptions.PdfOptions;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
```

अब हम रूपांतरण प्रक्रिया को सरल चरणों में विभाजित करेंगे ताकि इसका पालन करना आसान हो सके। प्रत्येक चरण के लिए, हम एक शीर्षक और स्पष्टीकरण प्रदान करेंगे।

## चरण 1: अपनी डेटा निर्देशिका परिभाषित करें

 उस निर्देशिका को निर्दिष्ट करके प्रारंभ करें जहां आपकी ODG फ़ाइलें स्थित हैं। आपको प्रतिस्थापित करना होगा`"Your Document Directory"` आपकी निर्देशिका के वास्तविक पथ के साथ।

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

## चरण 2: ओडीजी फ़ाइलें निर्दिष्ट करें

ODG फ़ाइल नामों की एक सरणी बनाएं जिन्हें आप कनवर्ट करना चाहते हैं। उदाहरण फ़ाइल नामों को अपनी ODG फ़ाइलों के नामों से बदलें।

```java
String[] files = new String[] {"example.odg", "example1.odg"};
```

## चरण 3: रैस्टराइज़ेशन विकल्प कॉन्फ़िगर करें

ODG फ़ाइलों के लिए रैस्टराइज़ेशन विकल्प सेट करें। ये विकल्प पृष्ठ आकार और वेक्टर रैस्टराइज़ेशन सेटिंग्स निर्धारित करेंगे।

```java
final OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
```

## चरण 4: ODG फ़ाइलों के माध्यम से लूप करें

अब, प्रत्येक ODG फ़ाइल को पुनरावृत्त करें, इसे लोड करें, और इसे PNG और PDF दोनों स्वरूपों में परिवर्तित करें।

```java
for (String file : files) {
    String fileName = dataDir + file;
    try (Image image = Image.load(fileName)) {
        rasterizationOptions.setPageSize(new SizeF(image.getWidth(), image.getHeight()));

        // पीएनजी में कनवर्ट करें
        String outFileName = "Your Document Directory" + file.replace(".odg", ".png");
        image.save(outFileName, new PngOptions() {{
            setVectorRasterizationOptions(rasterizationOptions);
        }});

        // पीडीएफ में कनवर्ट करें
        outFileName = "Your Document Directory" + file.replace(".odg", ".pdf");
        image.save(outFileName, new PdfOptions() {{
            setVectorRasterizationOptions(rasterizationOptions);
        }});
    }
}
```

बधाई हो! आपने Java के लिए Aspose.Imaging का उपयोग करके अपनी ODG फ़ाइलों को PNG और PDF दोनों स्वरूपों में सफलतापूर्वक परिवर्तित कर लिया है।

## निष्कर्ष

जावा के लिए Aspose.Imaging ODG फ़ाइलों को PNG और PDF जैसे अधिक व्यापक रूप से समर्थित छवि प्रारूपों में परिवर्तित करने की प्रक्रिया को सरल बनाता है। इस ट्यूटोरियल में बताए गए चरणों का पालन करके, आप अपने जावा प्रोजेक्ट्स में इन रूपांतरणों को कुशलतापूर्वक कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: क्या जावा के लिए Aspose.Imaging एक मुफ़्त टूल है?

 A1: नहीं, जावा के लिए Aspose.Imaging एक व्यावसायिक लाइब्रेरी है, और आप मूल्य निर्धारण की जानकारी यहां पा सकते हैं[खरीद पृष्ठ](https://purchase.aspose.com/buy).

### Q2: क्या मैं खरीदने से पहले जावा के लिए Aspose.Imaging आज़मा सकता हूँ?

 उ2: हां, आप यहां से नि:शुल्क परीक्षण संस्करण डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/).

### Q3: मैं जावा के लिए Aspose.Imaging के लिए समर्थन कैसे प्राप्त कर सकता हूं?

 उ3: आप सहायता मांग सकते हैं और प्रश्न पूछ सकते हैं[Aspose.इमेजिंग फोरम](https://forum.aspose.com/).

### Q4: जावा के लिए Aspose.Imaging अन्य कौन से फ़ाइल प्रारूप संभाल सकता है?

 A4: जावा के लिए Aspose.Imaging BMP, JPEG, TIFF, PDF और अन्य सहित छवि और दस्तावेज़ प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है। को देखें[प्रलेखन](https://reference.aspose.com/imaging/java/) एक व्यापक सूची के लिए.

### Q5: क्या मैं अपनी व्यावसायिक परियोजनाओं में जावा के लिए Aspose.Imaging का उपयोग कर सकता हूँ?

A5: हां, आप उचित लाइसेंस खरीदने के बाद वाणिज्यिक परियोजनाओं में जावा के लिए Aspose.Imaging का उपयोग कर सकते हैं।