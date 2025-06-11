---
"description": "Aspose.Imaging for Java का उपयोग करके अपनी छवियों को विकर्ण वॉटरमार्क के साथ बेहतर बनाएँ। इस चरण-दर-चरण मार्गदर्शिका का पालन करें और आसानी से आश्चर्यजनक वॉटरमार्क वाली छवियाँ बनाएँ।"
"linktitle": "विकर्ण छवि वॉटरमार्किंग"
"second_title": "Aspose.Imaging जावा इमेज प्रोसेसिंग API"
"title": "Java के लिए Aspose.Imaging के साथ विकर्ण छवि वॉटरमार्किंग"
"url": "/hi/java/image-processing-and-enhancement/diagonal-image-watermarking/"
"weight": 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Java के लिए Aspose.Imaging के साथ विकर्ण छवि वॉटरमार्किंग


अगर आप अपनी छवियों को स्टाइलिश विकर्ण वॉटरमार्क के साथ बेहतर बनाना चाहते हैं, तो Aspose.Imaging for Java आपकी मदद के लिए मौजूद है। इस चरण-दर-चरण मार्गदर्शिका में, हम आपको मौजूदा JPG छवि में 45-डिग्री घुमाए गए टेक्स्ट वॉटरमार्क को जोड़ने की प्रक्रिया से अवगत कराएँगे। आपको इसे करने के लिए Java या इमेज प्रोसेसिंग में विशेषज्ञ होने की आवश्यकता नहीं है - हम प्रत्येक उदाहरण को कई चरणों में विभाजित करेंगे ताकि यह सुनिश्चित हो सके कि आप आसानी से पेशेवर परिणाम प्राप्त कर सकें।

## आवश्यक शर्तें

इससे पहले कि हम छवि वॉटरमार्किंग की रोमांचक दुनिया में उतरें, आपको कुछ चीजों की आवश्यकता होगी:

1. Aspose.Imaging for Java: सुनिश्चित करें कि आपके पास Aspose.Imaging for Java इंस्टॉल है। आप डाउनलोड लिंक पा सकते हैं [यहाँ](https://releases.aspose.com/imaging/java/).

2. जावा विकास वातावरण: आपके कंप्यूटर पर एक कार्यशील जावा विकास वातावरण स्थापित होना चाहिए।

3. वॉटरमार्क के लिए एक छवि: वह छवि तैयार करें जिस पर आप वॉटरमार्क लगाना चाहते हैं और उसे एक निर्देशिका में संग्रहीत करें। आप इस ट्यूटोरियल के लिए एक नमूना छवि का उपयोग कर सकते हैं।

## पैकेज आयात करें

सबसे पहले, अपने जावा प्रोजेक्ट को इमेज वॉटरमार्किंग के लिए तैयार करने के लिए आवश्यक पैकेज आयात करें। नीचे वे आवश्यक पैकेज दिए गए हैं जिन्हें आपको शामिल करना होगा:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## चरण 1: मौजूदा छवि लोड करें

वह इमेज लोड करें जिस पर आप वॉटरमार्क लगाना चाहते हैं। इस उदाहरण में, हम मानते हैं कि आपके पास "ModifyingImages" निर्देशिका में "SampleTiff1.tiff" नाम की एक JPG इमेज है।

```java
// दस्तावेज़ निर्देशिका का पथ.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// मौजूदा JPG छवि लोड करें
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // शेष कोड यहां है
}
```

## चरण 2: वॉटरमार्क टेक्स्ट और ग्राफ़िक्स तैयार करें

अब, आइए अपना वॉटरमार्क टेक्स्ट घोषित करें और वॉटरमार्क के लिए ग्राफिक्स सेट करें।

```java
// वॉटरमार्क टेक्स्ट के साथ स्ट्रिंग ऑब्जेक्ट घोषित करें
String theString = "45 Degree Rotated Text";

// ग्राफ़िक्स क्लास का एक उदाहरण बनाएँ और आरंभ करें
Graphics graphics = new Graphics(image);

// छवि आकार संग्रहीत करने के लिए SizeF की एक ऑब्जेक्ट आरंभ करें
Size sz = graphics.getImage().getSize();
```

## चरण 3: फ़ॉन्ट और ब्रश परिभाषित करें

अपने वॉटरमार्क के लिए फ़ॉन्ट और ब्रश सेट करें। आप अपनी पसंद के अनुसार फ़ॉन्ट, आकार और शैली को अनुकूलित कर सकते हैं।

```java
// फ़ॉन्ट का एक उदाहरण बनाएं, इसे फ़ॉन्ट फेस, आकार और शैली के साथ आरंभ करें
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// SolidBrush का एक उदाहरण बनाएं और इसके विभिन्न गुण सेट करें
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## चरण 4: अपना पाठ प्रारूपित करें

संरेखण और प्रारूप ध्वज सहित अपने वॉटरमार्क पाठ के लिए प्रारूप निर्धारित करें।

```java
// StringFormat वर्ग के ऑब्जेक्ट को आरंभीकृत करें और इसके विभिन्न गुणधर्म सेट करें
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## चरण 5: परिवर्तन लागू करें

वॉटरमार्क टेक्स्ट को स्थान देने और घुमाने के लिए एक परिवर्तन मैट्रिक्स बनाएँ। इस उदाहरण में, हम टेक्स्ट को 45 डिग्री घुमाएँगे।

```java
// रूपांतरण के लिए मैट्रिक्स वर्ग का एक ऑब्जेक्ट बनाएँ
Matrix matrix = new Matrix();
// पहले अनुवाद फिर घूर्णन
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// मैट्रिक्स के माध्यम से परिवर्तन सेट करें
graphics.setTransform(matrix);
```

## चरण 6: ड्रा करें और सेव करें

अब, छवि में पाठ जोड़ने और वॉटरमार्क वाली छवि को अपने इच्छित स्थान पर सहेजने का समय आ गया है।

```java
// छवि पर स्ट्रिंग बनाएं
graphics.drawString(theString, font, brush, 0, 0, format);

// आउटपुट को डिस्क पर सहेजें
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

बधाई हो! आपने Aspose.Imaging for Java का उपयोग करके अपनी छवि में सफलतापूर्वक विकर्ण वॉटरमार्क जोड़ लिया है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा है कि Aspose.Imaging for Java का उपयोग करके विकर्ण वॉटरमार्क के साथ अपनी छवियों को कैसे बेहतर बनाया जाए। यह आपकी छवियों में एक पेशेवर स्पर्श जोड़ने के लिए एक शक्तिशाली उपकरण है। बस कुछ सरल चरणों के साथ, आप आश्चर्यजनक वॉटरमार्क वाली छवियां बना सकते हैं जो बाकी से अलग दिखती हैं।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: क्या Aspose.Imaging for Java शुरुआती लोगों के लिए उपयुक्त है?

A1: बिल्कुल! Aspose.Imaging for Java एक उपयोगकर्ता-अनुकूल इंटरफ़ेस और व्यापक दस्तावेज़ीकरण प्रदान करता है। यहां तक कि शुरुआती लोग भी इमेज प्रोसेसिंग के साथ जल्दी से शुरुआत कर सकते हैं।

### प्रश्न 2: क्या मैं वॉटरमार्क पाठ और शैली को अनुकूलित कर सकता हूं?

A2: हां, आप अपनी प्राथमिकताओं और ब्रांडिंग से मेल खाने के लिए वॉटरमार्क टेक्स्ट, फ़ॉन्ट, आकार, रंग और रोटेशन कोण को आसानी से अनुकूलित कर सकते हैं।

### प्रश्न 3: क्या Aspose.Imaging for Java JPG के अलावा अन्य छवि प्रारूपों का समर्थन करता है?

A3: हां, Aspose.Imaging for Java BMP, PNG, GIF, आदि सहित छवि प्रारूपों की एक विस्तृत श्रृंखला का समर्थन करता है।

### प्रश्न 4: क्या Aspose.Imaging for Java के लिए कोई निःशुल्क परीक्षण उपलब्ध है?

A4: हाँ, आप Java के लिए Aspose.Imaging को निःशुल्क परीक्षण के साथ आज़मा सकते हैं। इसे प्राप्त करें [यहाँ](https://releases.aspose.com/).

### प्रश्न 5: मैं Aspose.Imaging for Java के लिए सहायता या समर्थन कहां पा सकता हूं?

A5: यदि आपके पास कोई प्रश्न है या सहायता की आवश्यकता है, तो Aspose.Imaging for Java सहायता फ़ोरम पर जाएँ [यहाँ](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}