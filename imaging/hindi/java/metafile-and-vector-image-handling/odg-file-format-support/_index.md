---
"description": "जानें कि Aspose.Imaging for Java के साथ ODG फ़ाइलों को PNG और PDF में कैसे बदलें। कुशल रूपांतरण के लिए हमारे चरण-दर-चरण मार्गदर्शिका का पालन करें।"
"linktitle": "ODG फ़ाइल प्रारूप समर्थन"
"second_title": "Aspose.Imaging जावा इमेज प्रोसेसिंग API"
"title": "Java के लिए Aspose.Imaging के साथ ODG को PNG और PDF में बदलें"
"url": "/hi/java/metafile-and-vector-image-handling/odg-file-format-support/"
"weight": 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Java के लिए Aspose.Imaging के साथ ODG को PNG और PDF में बदलें

दस्तावेज़ रूपांतरण की दुनिया में, Aspose.Imaging for Java एक शक्तिशाली उपकरण के रूप में सामने आता है जो आपको ODG (OpenDocument Graphics) फ़ाइलों को PNG और PDF फ़ॉर्मेट में आसानी से बदलने की अनुमति देता है। यह ट्यूटोरियल आपको Aspose.Imaging for Java का उपयोग करके, चरण दर चरण प्रक्रिया के माध्यम से मार्गदर्शन करेगा। चाहे आप डेवलपर हों या सिर्फ़ ODG फ़ाइलों को परिवर्तित करने की तलाश में हों, यह लेख आपको अपना लक्ष्य प्राप्त करने में मदद करेगा।

## आवश्यक शर्तें

इससे पहले कि हम रूपांतरण प्रक्रिया में उतरें, आपको यह सुनिश्चित करना होगा कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

### 1. जावा विकास पर्यावरण

सुनिश्चित करें कि आपके सिस्टम पर जावा डेवलपमेंट एनवायरनमेंट सेट अप है। आप नवीनतम जावा डेवलपमेंट किट (JDK) को डाउनलोड करके इंस्टॉल कर सकते हैं। [ओरेकल वेबसाइट](https://www.oracle.com/java/technologies/javase-downloads).

### 2. जावा के लिए Aspose.Imaging

आपको Aspose.Imaging for Java डाउनलोड और इंस्टॉल करना होगा। आप नवीनतम संस्करण यहाँ पा सकते हैं [Aspose.Imaging for Java डाउनलोड पृष्ठ](https://releases.aspose.com/imaging/java/).

### 3. ओडीजी फ़ाइलें

बेशक, आपको उन ODG फ़ाइलों की ज़रूरत होगी जिन्हें आप कनवर्ट करना चाहते हैं। सुनिश्चित करें कि ये फ़ाइलें आपके सिस्टम पर किसी डायरेक्टरी में उपलब्ध हैं।

## पैकेज आयात करें

अब जब आपने सभी आवश्यक शर्तें पूरी कर ली हैं, तो चलिए अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करना शुरू करते हैं। ये पैकेज आपको Aspose.Imaging for Java के साथ प्रभावी ढंग से काम करने की अनुमति देंगे।

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.SizeF;
import com.aspose.imaging.imageoptions.PdfOptions;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
```

अब हम रूपांतरण प्रक्रिया को सरल चरणों में विभाजित करेंगे ताकि इसे समझना आसान हो जाए। प्रत्येक चरण के लिए, हम एक शीर्षक और स्पष्टीकरण प्रदान करेंगे।

## चरण 1: अपनी डेटा निर्देशिका निर्धारित करें

सबसे पहले उस डायरेक्टरी को निर्दिष्ट करें जहाँ आपकी ODG फ़ाइलें स्थित हैं। आपको प्रतिस्थापित करने की आवश्यकता होगी `"Your Document Directory"` आपकी निर्देशिका के वास्तविक पथ के साथ.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

## चरण 2: ODG फ़ाइलें निर्दिष्ट करें

उन ODG फ़ाइल नामों की एक सरणी बनाएँ जिन्हें आप कनवर्ट करना चाहते हैं। उदाहरण फ़ाइल नामों को अपनी ODG फ़ाइलों के नामों से बदलें।

```java
String[] files = new String[] {"example.odg", "example1.odg"};
```

## चरण 3: रास्टराइज़ेशन विकल्प कॉन्फ़िगर करें

ODG फ़ाइलों के लिए रास्टराइज़ेशन विकल्प सेट करें। ये विकल्प पृष्ठ आकार और वेक्टर रास्टराइज़ेशन सेटिंग निर्धारित करेंगे।

```java
final OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
```

## चरण 4: ODG फ़ाइलों के माध्यम से लूप करें

अब, प्रत्येक ODG फ़ाइल को पुनरावृत्त करें, उसे लोड करें, तथा उसे PNG और PDF दोनों प्रारूपों में परिवर्तित करें।

```java
for (String file : files) {
    String fileName = dataDir + file;
    try (Image image = Image.load(fileName)) {
        rasterizationOptions.setPageSize(new SizeF(image.getWidth(), image.getHeight()));

        // PNG में परिवर्तित करें
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

बधाई हो! आपने Aspose.Imaging for Java का उपयोग करके अपनी ODG फ़ाइलों को PNG और PDF दोनों स्वरूपों में सफलतापूर्वक परिवर्तित कर लिया है।

## निष्कर्ष

Aspose.Imaging for Java ODG फ़ाइलों को PNG और PDF जैसे अधिक व्यापक रूप से समर्थित छवि प्रारूपों में परिवर्तित करने की प्रक्रिया को सरल बनाता है। इस ट्यूटोरियल में बताए गए चरणों का पालन करके, आप अपने Java प्रोजेक्ट में इन रूपांतरणों को कुशलतापूर्वक निष्पादित कर सकते हैं।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या Aspose.Imaging for Java एक निःशुल्क टूल है?

A1: नहीं, Aspose.Imaging for Java एक वाणिज्यिक लाइब्रेरी है, और आप मूल्य निर्धारण जानकारी यहाँ पा सकते हैं [खरीद पृष्ठ](https://purchase.aspose.com/buy).

### प्रश्न 2: क्या मैं खरीदने से पहले Aspose.Imaging for Java आज़मा सकता हूँ?

A2: हाँ, आप यहाँ से निःशुल्क परीक्षण संस्करण डाउनलोड कर सकते हैं [यहाँ](https://releases.aspose.com/).

### प्रश्न 3: मैं Java के लिए Aspose.Imaging का समर्थन कैसे प्राप्त कर सकता हूं?

A3: आप सहायता मांग सकते हैं और प्रश्न पूछ सकते हैं [Aspose.Imaging फ़ोरम](https://forum.aspose.com/).

### प्रश्न 4: Aspose.Imaging for Java अन्य कौन से फ़ाइल स्वरूपों को संभाल सकता है?

A4: Aspose.Imaging for Java कई तरह के इमेज और दस्तावेज़ फ़ॉर्मेट को सपोर्ट करता है, जिसमें BMP, JPEG, TIFF, PDF और बहुत कुछ शामिल है। [प्रलेखन](https://reference.aspose.com/imaging/java/) विस्तृत सूची के लिए कृपया देखें.

### प्रश्न 5: क्या मैं अपनी व्यावसायिक परियोजनाओं में Java के लिए Aspose.Imaging का उपयोग कर सकता हूँ?

A5: हां, आप उचित लाइसेंस खरीदने के बाद व्यावसायिक परियोजनाओं में Aspose.Imaging for Java का उपयोग कर सकते हैं।

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}