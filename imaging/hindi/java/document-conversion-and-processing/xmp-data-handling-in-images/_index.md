---
"description": "Java के लिए Aspose.Imaging का उपयोग करके छवियों में XMP मेटाडेटा को प्रबंधित करना सीखें। अपनी छवि फ़ाइलों को बेहतर बनाने के लिए मेटाडेटा एम्बेड करें और पुनर्प्राप्त करें।"
"linktitle": "छवियों में XMP डेटा प्रबंधन"
"second_title": "Aspose.Imaging जावा इमेज प्रोसेसिंग API"
"title": "Aspose.Imaging for Java के साथ छवियों में XMP डेटा हैंडलिंग"
"url": "/hi/java/document-conversion-and-processing/xmp-data-handling-in-images/"
"weight": 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java के साथ छवियों में XMP डेटा हैंडलिंग

Aspose.Imaging for Java विभिन्न प्रारूपों में छवियों के साथ काम करने के लिए एक बहुमुखी और शक्तिशाली लाइब्रेरी है। यह ट्यूटोरियल आपको Aspose.Imaging for Java का उपयोग करके छवियों में XMP (एक्सटेंसिबल मेटाडेटा प्लेटफ़ॉर्म) डेटा को संभालने की प्रक्रिया के माध्यम से मार्गदर्शन करेगा। XMP छवि फ़ाइलों में मेटाडेटा एम्बेड करने के लिए एक मानक है, जिससे आप लेखक, विवरण और अधिक जैसी मूल्यवान जानकारी संग्रहीत कर सकते हैं।

## आवश्यक शर्तें

आरंभ करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- आपके कंप्यूटर पर स्थापित जावा विकास वातावरण.
- Aspose.Imaging for Java लाइब्रेरी स्थापित है। आप इसे यहाँ से डाउनलोड कर सकते हैं [Aspose.Imaging for Java वेबसाइट](https://releases.aspose.com/imaging/java/).
- जावा प्रोग्रामिंग की बुनियादी समझ.

## पैकेज आयात करना

अपने जावा प्रोजेक्ट में आवश्यक पैकेज आयात करके शुरू करें। आप अपने कोड की शुरुआत में निम्नलिखित आयात कथन जोड़ सकते हैं:

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

अब, आइए इस उदाहरण को चरण-दर-चरण मार्गदर्शिका में विभाजित करें:

## चरण 1: छवि का आकार और Tiff विकल्प निर्दिष्ट करें

सबसे पहले, वह निर्देशिका निर्धारित करें जहाँ आपकी छवि संग्रहीत की जाएगी और छवि का आकार निर्दिष्ट करने के लिए एक आयत बनाएँ। इस उदाहरण में, हम कुछ विकल्पों के साथ एक Tiff छवि का उपयोग करते हैं।

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

## चरण 2: एक नई छवि बनाएँ

अब, निर्दिष्ट विकल्पों के साथ एक नई छवि बनाएँ। इस छवि का उपयोग XMP मेटाडेटा को संग्रहीत करने के लिए किया जाएगा।

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

## चरण 3: XMP हेडर और ट्रेलर बनाएँ

अपने XMP मेटाडेटा के लिए XMP-Header और XMP-Trailer के इंस्टेंस बनाएँ। ये हेडर और ट्रेलर मेटाडेटा संरचना को परिभाषित करने में मदद करते हैं।

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

## चरण 4: XMP मेटा जानकारी बनाएँ

अब, अलग-अलग विशेषताएँ सेट करने के लिए XMP मेटा का एक इंस्टेंस बनाएँ। आप लेखक और विवरण जैसी जानकारी जोड़ सकते हैं।

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

## चरण 5: XMP पैकेट रैपर बनाएं

XmpPacketWrapper का एक उदाहरण बनाएं जिसमें XMP हेडर, ट्रेलर और मेटा जानकारी शामिल हो।

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

## चरण 6: फ़ोटोशॉप पैकेज जोड़ें

फ़ोटोशॉप-विशिष्ट जानकारी संग्रहीत करने के लिए, फ़ोटोशॉप पैकेज बनाएँ और इसकी विशेषताएँ, जैसे शहर, देश और रंग मोड सेट करें। फिर, इस पैकेज को XMP मेटाडेटा में जोड़ें।

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

## चरण 7: डबलिन कोर पैकेज जोड़ें

लेखक, शीर्षक और अतिरिक्त मान जैसी अधिक सामान्य जानकारी के लिए, एक डबलिनकोर पैकेज बनाएं और इसकी विशेषताएँ सेट करें। इस पैकेज को XMP मेटाडेटा में भी जोड़ें।

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

## चरण 8: छवि में XMP मेटाडेटा अपडेट करें

XMP मेटाडेटा को छवि में अपडेट करें `setXmpData` तरीका।

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

## चरण 9: छवि सहेजें

अब आप डिस्क पर या मेमोरी स्ट्रीम में एम्बेडेड XMP मेटाडेटा के साथ छवि को सहेज सकते हैं।

```java
    image.save(ms);
```

## चरण 10: छवि लोड करें और XMP मेटाडेटा प्राप्त करें

छवि से XMP मेटाडेटा प्राप्त करने के लिए, छवि को मेमोरी स्ट्रीम या डिस्क से लोड करें और XMP डेटा तक पहुँचें।

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // पैकेज डेटा का उपयोग करें...
        }
    }
}
```

बधाई हो! आपने Aspose.Imaging for Java का उपयोग करके छवियों में XMP डेटा को संभालना सफलतापूर्वक सीख लिया है। यह आपको अपनी छवि फ़ाइलों में मूल्यवान मेटाडेटा संग्रहीत करने और पुनर्प्राप्त करने की अनुमति देता है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने Aspose.Imaging for Java का उपयोग करके छवियों में XMP मेटाडेटा के साथ काम करने का तरीका खोजा। चरण-दर-चरण मार्गदर्शिका का पालन करके, आप आसानी से अपनी छवि फ़ाइलों में मेटाडेटा एम्बेड और पुनर्प्राप्त कर सकते हैं, जिससे उनकी जानकारी और उपयोगिता बढ़ जाती है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: XMP मेटाडेटा क्या है?

A1: XMP (एक्सटेंसिबल मेटाडेटा प्लेटफ़ॉर्म) छवियों सहित विभिन्न प्रकार की फ़ाइलों में मेटाडेटा एम्बेड करने के लिए एक मानक है। यह आपको फ़ाइल के भीतर ही लेखक, शीर्षक, विवरण और बहुत कुछ जैसी जानकारी संग्रहीत करने की अनुमति देता है।

### प्रश्न 2: XMP मेटाडेटा महत्वपूर्ण क्यों है?

A2: XMP मेटाडेटा डिजिटल संपत्तियों को व्यवस्थित और वर्गीकृत करने के लिए आवश्यक है। यह स्वामित्व को निर्दिष्ट करने, सामग्री का वर्णन करने और छवियों जैसी फ़ाइलों में संदर्भ जोड़ने में मदद करता है, जिससे उन्हें अधिक सुलभ और सार्थक बनाया जा सके।

### प्रश्न 3: क्या मैं XMP मेटाडेटा को छवि में एम्बेड करने के बाद संपादित कर सकता हूँ?

A3: हाँ, आप XMP मेटाडेटा को इमेज में एम्बेड करने के बाद उसे संपादित कर सकते हैं। Aspose.Imaging for Java आवश्यकतानुसार मेटाडेटा विशेषताओं को संशोधित और अपडेट करने के लिए उपकरण प्रदान करता है।

### प्रश्न 4: क्या Aspose.Imaging for Java एक निःशुल्क टूल है?

A4: Aspose.Imaging for Java एक निःशुल्क परीक्षण संस्करण प्रदान करता है, लेकिन पूर्ण कार्यक्षमता और विस्तारित उपयोग के लिए, एक सशुल्क लाइसेंस की आवश्यकता होती है। आप विकल्पों का पता लगा सकते हैं [Aspose.Imaging for Java वेबसाइट](https://purchase.aspose.com/buy).

### प्रश्न 5: मैं Aspose.Imaging for Java के लिए सहायता और समर्थन कहां से प्राप्त कर सकता हूं?

A5: यदि आपको Aspose.Imaging for Java से संबंधित कोई समस्या आती है या आपके कोई प्रश्न हैं, तो आप यहां जा सकते हैं [Aspose.Imaging फ़ोरम](https://forum.aspose.com/) सामुदायिक सहायता और मार्गदर्शन के लिए।



## संपूर्ण स्रोत कोड
```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// आयत को परिभाषित करके छवि का आकार निर्दिष्ट करें
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// केवल नमूना प्रयोजनों के लिए एकदम नई छवि बनाएं
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// XMP-Header का एक उदाहरण बनाएँ
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// Xmp-TrailerPi का एक उदाहरण बनाएं
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// विभिन्न विशेषताओं को सेट करने के लिए XMP मेटा क्लास का एक उदाहरण बनाएं
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	// XmpPacketWrapper का एक उदाहरण बनाएं जिसमें सभी मेटाडेटा शामिल हों
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// फ़ोटोशॉप पैकेज का एक उदाहरण बनाएं और फ़ोटोशॉप विशेषताएँ सेट करें
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// XMP मेटाडेटा में फ़ोटोशॉप पैकेज जोड़ें
	xmpData.addPackage(photoshopPackage);
	// DublinCore पैकेज का एक उदाहरण बनाएं और dublinCore विशेषताएँ सेट करें
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// XMP मेटाडेटा में dublinCore पैकेज जोड़ें
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// XMP मेटाडेटा को छवि में अपडेट करें
	image.setXmpData(xmpData);
	// छवि को डिस्क या मेमोरी स्ट्रीम में सहेजें
	image.save(ms);
	// मेटाडेटा पढ़ने/प्राप्त करने के लिए मेमोरी स्ट्रीम या डिस्क से छवि लोड करें
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// XMP मेटाडेटा प्राप्त करना
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