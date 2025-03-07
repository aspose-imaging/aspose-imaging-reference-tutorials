---
title: जावा के लिए Aspose.Imaging के साथ छवियों में XMP डेटा हैंडलिंग
linktitle: छवियों में एक्सएमपी डेटा हैंडलिंग
second_title: Aspose.Imaging जावा इमेज प्रोसेसिंग एपीआई
description: जावा के लिए Aspose.Imaging का उपयोग करके छवियों में XMP मेटाडेटा को संभालना सीखें। अपनी छवि फ़ाइलों को बेहतर बनाने के लिए मेटाडेटा एम्बेड और पुनर्प्राप्त करें।
weight: 16
url: /hi/java/document-conversion-and-processing/xmp-data-handling-in-images/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# जावा के लिए Aspose.Imaging के साथ छवियों में XMP डेटा हैंडलिंग

जावा के लिए Aspose.Imaging विभिन्न प्रारूपों में छवियों के साथ काम करने के लिए एक बहुमुखी और शक्तिशाली लाइब्रेरी है। यह ट्यूटोरियल जावा के लिए Aspose.Imaging का उपयोग करके छवियों में XMP (एक्स्टेंसिबल मेटाडेटा प्लेटफ़ॉर्म) डेटा को संभालने की प्रक्रिया में आपका मार्गदर्शन करेगा। XMP छवि फ़ाइलों में मेटाडेटा एम्बेड करने के लिए एक मानक है, जो आपको लेखक, विवरण और बहुत कुछ जैसी मूल्यवान जानकारी संग्रहीत करने की अनुमति देता है।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

- आपके कंप्यूटर पर एक जावा विकास वातावरण स्थापित किया गया है।
-  जावा लाइब्रेरी के लिए Aspose.Imaging स्थापित किया गया। आप इसे यहां से डाउनलोड कर सकते हैं[जावा वेबसाइट के लिए Aspose.Imaging](https://releases.aspose.com/imaging/java/).
- जावा प्रोग्रामिंग की बुनियादी समझ।

## पैकेज आयात करना

अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करके प्रारंभ करें। आप अपने कोड की शुरुआत में निम्नलिखित आयात विवरण जोड़ सकते हैं:

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Rectangle;
import com.aspose.imaging.imageoptions.TiffOptions;
import com.aspose.imaging.xmp.XmpPackage;
import com.aspose.imaging.xmp.XmpPacketWrapper;
import com.aspose.imaging.xmp.XmpMeta;
import com.aspose.imaging.xmp.photoshop.ColorMode;
import com.aspose.imaging.xmp.photoshop.PhotoshopPackage;
import com.aspose.imaging.xmp.dc.DublinCorePackage;
import com.aspose.imaging.xmp.header.XmpHeaderPi;
import com.aspose.imaging.xmp.trailer.XmpTrailerPi;
import java.io.ByteArrayInputStream;
import java.io.ByteArrayOutputStream;
```

अब, आइए उदाहरण को चरण-दर-चरण मार्गदर्शिका में विभाजित करें:

## चरण 1: छवि का आकार और टिफ़ विकल्प निर्दिष्ट करें

सबसे पहले, उस निर्देशिका को परिभाषित करें जहां आपकी छवि संग्रहीत की जाएगी और छवि का आकार निर्दिष्ट करने के लिए एक आयत बनाएं। इस उदाहरण में, हम कुछ विकल्पों के साथ एक टिफ़ छवि का उपयोग करते हैं।

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

## चरण 2: एक नई छवि बनाएं

अब, निर्दिष्ट विकल्पों के साथ एक नई छवि बनाएं। इस छवि का उपयोग XMP मेटाडेटा को संग्रहीत करने के लिए किया जाएगा।

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

## चरण 3: एक्सएमपी हेडर और ट्रेलर बनाएं

अपने XMP मेटाडेटा के लिए XMP-हेडर और XMP-ट्रेलर के उदाहरण बनाएं। ये हेडर और ट्रेलर मेटाडेटा संरचना को परिभाषित करने में मदद करते हैं।

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## चरण 4: एक्सएमपी मेटा सूचना बनाएं

अब, विभिन्न विशेषताओं को सेट करने के लिए XMP मेटा का एक उदाहरण बनाएं। आप लेखक और विवरण जैसी जानकारी जोड़ सकते हैं।

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## चरण 5: एक्सएमपी पैकेट रैपर बनाएं

XmpPacketWrapper का एक उदाहरण बनाएं जिसमें XMP हेडर, ट्रेलर और मेटा जानकारी शामिल हो।

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## चरण 6: फ़ोटोशॉप पैकेज जोड़ें

फ़ोटोशॉप-विशिष्ट जानकारी संग्रहीत करने के लिए, एक फ़ोटोशॉप पैकेज बनाएं और इसकी विशेषताएँ, जैसे शहर, देश और रंग मोड सेट करें। फिर, इस पैकेज को XMP मेटाडेटा में जोड़ें।

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## चरण 7: डबलिन कोर पैकेज जोड़ें

अधिक सामान्य जानकारी, जैसे लेखक, शीर्षक और अतिरिक्त मानों के लिए, एक डबलिनकोर पैकेज बनाएं और उसकी विशेषताएँ सेट करें। इस पैकेज को XMP मेटाडेटा में भी जोड़ें।

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## चरण 8: छवि में XMP मेटाडेटा अपडेट करें

 का उपयोग करके छवि में XMP मेटाडेटा को अपडेट करें`setXmpData` तरीका।

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## चरण 9: छवि सहेजें

अब आप छवि को डिस्क पर या मेमोरी स्ट्रीम में एम्बेडेड XMP मेटाडेटा के साथ सहेज सकते हैं।

```java
    image.save(ms);
```

## चरण 10: छवि लोड करें और XMP मेटाडेटा पुनर्प्राप्त करें

छवि से XMP मेटाडेटा पुनर्प्राप्त करने के लिए, छवि को मेमोरी स्ट्रीम या डिस्क से लोड करें और XMP डेटा तक पहुंचें।

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // पैकेज डेटा का उपयोग करें...
        }
    }
}
```

बधाई हो! आपने Java के लिए Aspose.Imaging का उपयोग करके छवियों में XMP डेटा को प्रबंधित करना सफलतापूर्वक सीख लिया है। यह आपको अपनी छवि फ़ाइलों के भीतर मूल्यवान मेटाडेटा को संग्रहीत और पुनर्प्राप्त करने की अनुमति देता है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने पता लगाया कि जावा के लिए Aspose.Imaging का उपयोग करके छवियों में XMP मेटाडेटा के साथ कैसे काम किया जाए। चरण-दर-चरण मार्गदर्शिका का पालन करके, आप अपनी छवि फ़ाइलों में मेटाडेटा को आसानी से एम्बेड और पुनर्प्राप्त कर सकते हैं, जिससे उनकी जानकारी और उपयोगिता बढ़ सकती है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: XMP मेटाडेटा क्या है?

A1: XMP (एक्स्टेंसिबल मेटाडेटा प्लेटफ़ॉर्म) छवियों सहित विभिन्न प्रकार की फ़ाइलों में मेटाडेटा एम्बेड करने के लिए एक मानक है। यह आपको फ़ाइल के भीतर लेखक, शीर्षक, विवरण और बहुत कुछ जैसी जानकारी संग्रहीत करने की अनुमति देता है।

### Q2: XMP मेटाडेटा क्यों महत्वपूर्ण है?

A2: XMP मेटाडेटा डिजिटल संपत्तियों को व्यवस्थित और वर्गीकृत करने के लिए आवश्यक है। यह स्वामित्व को जिम्मेदार ठहराने, सामग्री का वर्णन करने और छवियों की तरह फाइलों में संदर्भ जोड़ने, उन्हें अधिक सुलभ और सार्थक बनाने में मदद करता है।

### Q3: क्या मैं XMP मेटाडेटा को किसी छवि में एम्बेड करने के बाद संपादित कर सकता हूँ?

A3: हाँ, आप XMP मेटाडेटा को किसी छवि में एम्बेड करने के बाद संपादित कर सकते हैं। जावा के लिए Aspose.Imaging आवश्यकतानुसार मेटाडेटा विशेषताओं को संशोधित और अद्यतन करने के लिए उपकरण प्रदान करता है।

### Q4: क्या जावा के लिए Aspose.Imaging एक मुफ़्त टूल है?

 A4: जावा के लिए Aspose.Imaging एक निःशुल्क परीक्षण संस्करण प्रदान करता है, लेकिन पूर्ण कार्यक्षमता और विस्तारित उपयोग के लिए, एक सशुल्क लाइसेंस की आवश्यकता होती है। आप पर विकल्प तलाश सकते हैं[जावा वेबसाइट के लिए Aspose.Imaging](https://purchase.aspose.com/buy).

### Q5: जावा के लिए Aspose.Imaging के लिए मुझे सहायता और समर्थन कहां से मिल सकता है?

 A5: यदि आपको जावा के लिए Aspose.Imaging से संबंधित कोई समस्या आती है या आपके कोई प्रश्न हैं, तो आप यहां जा सकते हैं[Aspose.इमेजिंग फ़ोरम](https://forum.aspose.com/) सामुदायिक समर्थन और मार्गदर्शन के लिए।



## संपूर्ण स्रोत कोड
```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// आयत को परिभाषित करके छवि का आकार निर्दिष्ट करें
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// केवल नमूना प्रयोजनों के लिए बिल्कुल नई छवि बनाएं
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// एक्सएमपी-हेडर का एक उदाहरण बनाएं
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// Xmp-TrailerPi का एक उदाहरण बनाएं
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// विभिन्न विशेषताओं को सेट करने के लिए XMP मेटा क्लास का एक उदाहरण बनाएं
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	//XmpPacketWrapper का एक उदाहरण बनाएं जिसमें सभी मेटाडेटा शामिल हों
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// फ़ोटोशॉप पैकेज का एक उदाहरण बनाएं और फ़ोटोशॉप विशेषताएँ सेट करें
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// XMP मेटाडेटा में फ़ोटोशॉप पैकेज जोड़ें
	xmpData.addPackage(photoshopPackage);
	// डबलिनकोर पैकेज का एक उदाहरण बनाएं और डबलिनकोर विशेषताएँ सेट करें
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// XMP मेटाडेटा में डबलिनकोर पैकेज जोड़ें
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// XMP मेटाडेटा को छवि में अद्यतन करें
	image.setXmpData(xmpData);
	// छवि को डिस्क पर या मेमोरी स्ट्रीम में सहेजें
	image.save(ms);
	// मेटाडेटा पढ़ने/प्राप्त करने के लिए छवि को मेमोरी स्ट्रीम या डिस्क से लोड करें
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// एक्सएमपी मेटाडेटा प्राप्त करना
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// पैकेज डेटा का उपयोग करें...
		}
	}
}
        
```
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
