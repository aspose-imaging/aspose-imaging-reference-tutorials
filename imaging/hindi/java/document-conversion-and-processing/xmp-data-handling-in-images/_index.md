---
date: 2026-05-18
description: जानें कैसे जावा इमेज प्रोसेसिंग लाइब्रेरी Aspose.Imaging का उपयोग करके
  इमेज में XMP मेटाडेटा एम्बेड और रिट्रीव करें, स्टेप‑बाय‑स्टेप कोड के साथ।
keywords:
- java image processing library
- XMP metadata Java
- Aspose.Imaging Java
linktitle: इमेज में XMP डेटा हैंडलिंग
schemas:
- author: Aspose
  dateModified: '2026-05-18'
  description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  headline: 'Java Image Processing Library: XMP with Aspose.Imaging'
  type: TechArticle
- description: Learn how to use the Java image processing library Aspose.Imaging to
    embed and retrieve XMP metadata in images, with step‑by‑step code.
  name: 'Java Image Processing Library: XMP with Aspose.Imaging'
  steps:
  - name: Specify Image Size and Tiff Options
    text: First, define the directory where your image will be stored and create a
      `Rectangle` to specify the size of the image. In this example, we use a TIFF
      image with certain options. `TiffOptions` configures format‑specific settings
      for the TIFF image.
  - name: Create a New Image
    text: Now, create a new image with the specified options. This image will be used
      to store the XMP metadata. `TiffImage` represents a TIFF image object, and `TiffFrame`
      defines an individual frame within it.
  - name: Create XMP Header and Trailer
    text: Create instances of XMP‑Header and XMP‑Trailer for your XMP metadata. These
      headers and trailers help define the metadata structure. `XmpHeaderPi` and `XmpTrailerPi`
      represent the XMP packet’s opening and closing sections.
  - name: Create XMP Meta Information
    text: Now, create an instance of XMP meta to set different attributes. You can
      add information like the author and description. `XmpMeta` holds the core metadata
      fields such as author and description.
  - name: Create XMP Packet Wrapper
    text: '`XmpPacketWrapper` is the container that holds the XMP header, trailer,
      and meta information in a single packet. It ensures the packet conforms to the
      XMP specification. `XmpPacketWrapper` packages the header, meta, and trailer
      into a single XMP packet.'
  - name: Add Photoshop Package
    text: To store Photoshop‑specific information, create a Photoshop package and
      set its attributes, such as city, country, and color mode. Then, add this package
      to the XMP metadata. `PhotoshopPackage` stores Photoshop‑specific metadata like
      city, country, and color mode.
  - name: Add Dublin Core Package
    text: For more general information, like author, title, and additional values,
      create a DublinCore package and set its attributes. Add this package to the
      XMP metadata as well. `DublinCorePackage` contains standard Dublin Core fields
      such as title, creator, and keywords.
  - name: Update XMP Metadata in the Image
    text: Update the XMP metadata into the image using the `setXmpData` method. This
      call writes the XMP packet into the image’s metadata section. `setXmpData` writes
      the XMP packet into the image’s metadata section.
  - name: Save the Image
    text: You can now save the image with the embedded XMP metadata on the disk or
      in a memory stream.
  - name: Load the Image and Retrieve XMP Metadata
    text: To retrieve the XMP metadata from the image, load the image from the memory
      stream or disk and access the XMP data via the `getXmpData` method. `getXmpData`
      reads the embedded XMP packet from the image. Congratulations! You've successfully
      learned how to handle XMP data in images using Aspose.Imagin
  type: HowTo
- questions:
  - answer: XMP is an XML‑based standard for embedding descriptive information directly
      inside files, enabling consistent metadata across applications.
    question: What is XMP metadata?
  - answer: It lets you tag images with author, copyright, keywords, and custom data,
      improving searchability and asset management without external databases.
    question: Why is XMP metadata important?
  - answer: Yes, Aspose.Imaging for Java provides methods to modify existing XMP packets
      and write them back to the file.
    question: Can I edit XMP metadata after embedding it in an image?
  - answer: A free trial is available for evaluation, but a paid license is required
      for production use. You can explore options on the [Aspose.Imaging for Java
      website](https://purchase.aspose.com/buy).
    question: Is Aspose.Imaging for Java a free tool?
  - answer: Visit the [Aspose.Imaging forums](https://forum.aspose.com/) for community
      assistance, or contact Aspose support directly for paid‑license customers.
    question: Where can I get help and support for Aspose.Imaging for Java?
  type: FAQPage
second_title: Aspose.Imaging Java Image Processing API
title: 'जावा इमेज प्रोसेसिंग लाइब्रेरी: XMP with Aspose.Imaging'
url: /hi/java/document-conversion-and-processing/xmp-data-handling-in-images/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.Imaging for Java के साथ छवियों में XMP डेटा हैंडलिंग

Aspose.Imaging एक **java image processing library** है जो आपको दर्जनों रास्टर और वेक्टर फ़ॉर्मेट के साथ काम करने देता है। इस ट्यूटोरियल में आप सीखेंगे कि कैसे Aspose.Imaging for Java का उपयोग करके छवियों में XMP (Extensible Metadata Platform) डेटा को एम्बेड और रिट्रीव किया जाता है। अंत तक, आप लेखक, विवरण, और कस्टम मेटाडेटा को सीधे अपनी छवि फ़ाइलों में स्टोर कर सकेंगे, जिससे वे खोज योग्य और स्वयं‑वर्णनात्मक बन जाएँगी।

## त्वरित उत्तर
- **What is XMP?** XMP एक मानकीकृत XML‑आधारित फ़ॉर्मेट है जो छवियों, PDFs, और वीडियो जैसी फ़ाइलों में मेटाडेटा एम्बेड करने के लिए उपयोग होता है।  
- **Which library handles XMP in Java?** Aspose.Imaging for Java XMP पैकेट पढ़ने और लिखने के लिए पूर्ण API प्रदान करता है।  
- **Do I need a license?** विकास के लिए एक फ्री ट्रायल काम करता है; उत्पादन के लिए एक व्यावसायिक लाइसेंस आवश्यक है।  
- **How many image formats are supported?** 150 से अधिक फ़ॉर्मेट समर्थित हैं, जिसमें TIFF, JPEG, PNG, PSD, और RAW शामिल हैं।  
- **Can I process large images?** हाँ – लाइब्रेरी 2 GB तक की फ़ाइलों को पूरी छवि को मेमोरी में लोड किए बिना संभाल सकती है।

## XMP मेटाडेटा क्या है?
XMP मेटाडेटा एक XML‑आधारित मानक है जो वर्णनात्मक जानकारी को सीधे डिजिटल फ़ाइलों में एम्बेड करता है। यह लेखक, कॉपीराइट, कीवर्ड, और कस्टम डेटा को विभिन्न अनुप्रयोगों में सुसंगत रूप से संग्रहीत करने में सक्षम बनाता है। चूँकि यह XML है, XMP को कस्टम नेमस्पेस के साथ विस्तारित किया जा सकता है, जिससे डेवलपर्स प्रोपाइटरी फ़ील्ड जोड़ सकते हैं जबकि कोर स्कीमा को समझने वाले टूल्स के साथ संगतता बनी रहती है। यह XMP को दीर्घकालिक एसेट मैनेजमेंट और क्रॉस‑एप्लिकेशन इंटरऑपरेबिलिटी के लिए आदर्श बनाता है।

## XMP के लिए Java इमेज प्रोसेसिंग लाइब्रेरी क्यों उपयोग करें?
Aspose.Imaging for Java **150+ इमेज फ़ॉर्मेट** का समर्थन करता है और मल्टी‑गिगाबाइट फ़ाइलों को स्ट्रीमिंग मोड में प्रोसेस कर सकता है, जिससे साधारण लोडिंग की तुलना में मेमोरी उपयोग 80 % तक घट जाता है। API यह भी सुनिश्चित करती है कि XMP पैकेट मानकों के अनुरूप रहें, जिससे Adobe Photoshop, Lightroom, और अन्य टूल्स के साथ संगतता बनी रहती है।

## आवश्यकताएँ

- आपके कंप्यूटर पर Java विकास वातावरण स्थापित हो।  
- Aspose.Imaging for Java लाइब्रेरी स्थापित हो। आप इसे [Aspose.Imaging for Java website](https://releases.aspose.com/imaging/java/) से डाउनलोड कर सकते हैं।  
- Java प्रोग्रामिंग की बुनियादी समझ।

## पैकेज इम्पोर्ट करना

अपने Java प्रोजेक्ट में आवश्यक पैकेज इम्पोर्ट करके शुरू करें। आप कोड की शुरुआत में निम्नलिखित इम्पोर्ट स्टेटमेंट जोड़ सकते हैं:

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

अब, चलिए उदाहरण को चरण‑दर‑चरण गाइड में विभाजित करते हैं:

## Java इमेज प्रोसेसिंग लाइब्रेरी का उपयोग करके XMP मेटाडेटा कैसे एम्बेड करें?

अपनी छवि लोड करें, एक XMP पैकेट बनाएं, पैकेट को छवि से संलग्न करें, और सहेजें – सभी कुछ कुछ ही संक्षिप्त लाइनों में। Aspose.Imaging की `setXmpData` मेथड पैकेट को सीधे फ़ाइल में लिखती है बिना किसी अलग मेटाडेटा फ़ाइल की आवश्यकता के। यह प्रक्रिया फ़ाइल‑आधारित और स्ट्रीम‑आधारित दोनों छवियों के साथ काम करती है, जिससे यह वेब सेवाओं और बैच जॉब्स के लिए उपयुक्त बनती है।

### चरण 1: छवि आकार और Tiff विकल्प निर्दिष्ट करें

पहले, वह डायरेक्टरी निर्धारित करें जहाँ आपकी छवि संग्रहीत होगी और एक `Rectangle` बनाकर छवि का आकार निर्दिष्ट करें। इस उदाहरण में, हम कुछ विकल्पों के साथ एक TIFF छवि का उपयोग करते हैं। `TiffOptions` TIFF छवि के लिए फ़ॉर्मेट‑विशिष्ट सेटिंग्स को कॉन्फ़िगर करता है।

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
```

### चरण 2: नई छवि बनाएं

अब, निर्दिष्ट विकल्पों के साथ एक नई छवि बनाएं। यह छवि XMP मेटाडेटा संग्रहीत करने के लिए उपयोग होगी। `TiffImage` एक TIFF छवि ऑब्जेक्ट को दर्शाता है, और `TiffFrame` उसके भीतर एक व्यक्तिगत फ्रेम को परिभाषित करता है।

```java
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight()))) {
```

### चरण 3: XMP हेडर और ट्रेलर बनाएं

अपने XMP मेटाडेटा के लिए XMP‑Header और XMP‑Trailer के इंस्टेंस बनाएं। ये हेडर और ट्रेलर मेटाडेटा संरचना को परिभाषित करने में मदद करते हैं। `XmpHeaderPi` और `XmpTrailerPi` क्रमशः XMP पैकेट के ओपनिंग और क्लोज़िंग सेक्शन को दर्शाते हैं।

```java
    XmpHeaderPi xmpHeader = new XmpHeaderPi();
    xmpHeader.setGuid(dataDir);
    
    XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
```

### चरण 4: XMP मेटा जानकारी बनाएं

अब, विभिन्न एट्रीब्यूट सेट करने के लिए XMP मेटा का एक इंस्टेंस बनाएं। आप लेखक और विवरण जैसी जानकारी जोड़ सकते हैं। `XmpMeta` कोर मेटाडेटा फ़ील्ड जैसे लेखक और विवरण को रखता है।

```java
    XmpMeta xmpMeta = new XmpMeta();
    xmpMeta.addAttribute("Author", "Mr Smith");
    xmpMeta.addAttribute("Description", "The fake metadata value");
```

### चरण 5: XMP पैकेट रैपर बनाएं

`XmpPacketWrapper` वह कंटेनर है जो XMP हेडर, ट्रेलर, और मेटा जानकारी को एक ही पैकेट में रखता है। यह सुनिश्चित करता है कि पैकेट XMP स्पेसिफिकेशन के अनुरूप हो। `XmpPacketWrapper` हेडर, मेटा, और ट्रेलर को एकल XMP पैकेट में पैकेज करता है।

```java
    XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
```

### चरण 6: Photoshop पैकेज जोड़ें

Photoshop‑विशिष्ट जानकारी संग्रहीत करने के लिए एक Photoshop पैकेज बनाएं और उसके एट्रीब्यूट सेट करें, जैसे शहर, देश, और कलर मोड। फिर इस पैकेज को XMP मेटाडेटा में जोड़ें। `PhotoshopPackage` Photoshop‑विशिष्ट मेटाडेटा जैसे शहर, देश, और कलर मोड को संग्रहीत करता है।

```java
    PhotoshopPackage photoshopPackage = new PhotoshopPackage();
    photoshopPackage.setCity("London");
    photoshopPackage.setCountry("England");
    photoshopPackage.setColorMode(ColorMode.Rgb);
    xmpData.addPackage(photoshopPackage);
```

### चरण 7: Dublin Core पैकेज जोड़ें

अधिक सामान्य जानकारी जैसे लेखक, शीर्षक, और अतिरिक्त मानों के लिए एक DublinCore पैकेज बनाएं और उसके एट्रीब्यूट सेट करें। इस पैकेज को भी XMP मेटाडेटा में जोड़ें। `DublinCorePackage` मानक Dublin Core फ़ील्ड जैसे शीर्षक, निर्माता, और कीवर्ड को शामिल करता है।

```java
    DublinCorePackage dublinCorePackage = new DublinCorePackage();
    dublinCorePackage.setAuthor("Charles Bukowski");
    dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
    dublinCorePackage.addValue("dc:movie", "Barfly");
    xmpData.addPackage(dublinCorePackage);
```

### चरण 8: छवि में XMP मेटाडेटा अपडेट करें

`setXmpData` मेथड का उपयोग करके छवि में XMP मेटाडेटा अपडेट करें। यह कॉल XMP पैकेट को छवि के मेटाडेटा सेक्शन में लिखती है। `setXmpData` XMP पैकेट को छवि के मेटाडेटा सेक्शन में लिखती है।

```java
    ByteArrayOutputStream ms = new ByteArrayOutputStream();
    image.setXmpData(xmpData);
```

### चरण 9: छवि सहेजें

अब आप एम्बेडेड XMP मेटाडेटा के साथ छवि को डिस्क पर या मेमोरी स्ट्रीम में सहेज सकते हैं।

```java
    image.save(ms);
```

### चरण 10: छवि लोड करें और XMP मेटाडेटा प्राप्त करें

छवि से XMP मेटाडेटा प्राप्त करने के लिए, छवि को मेमोरी स्ट्रीम या डिस्क से लोड करें और `getXmpData` मेथड के माध्यम से XMP डेटा एक्सेस करें। `getXmpData` एम्बेडेड XMP पैकेट को छवि से पढ़ता है।

```java
    try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray()))) {
        XmpPacketWrapper imgXmpData = img.getXmpData();
        for (XmpPackage pack : imgXmpData.getPackages()) {
            // Use package data ...
        }
    }
}
```

बधाई हो! आपने सफलतापूर्वक Aspose.Imaging for Java का उपयोग करके छवियों में XMP डेटा को हैंडल करना सीख लिया है। यह आपको अपनी छवि फ़ाइलों के भीतर मूल्यवान मेटाडेटा को स्टोर और पुनः प्राप्त करने की अनुमति देता है।

## सामान्य समस्याएँ और समाधान

- **Metadata not appearing in Photoshop:** सुनिश्चित करें कि XMP पैकेट उचित XML स्कीमा का पालन करता है; Aspose.Imaging इसे स्वचालित रूप से वैलिडेट करता है, लेकिन कस्टम नेमस्पेस को रजिस्टर करने की आवश्यकता हो सकती है।  
- **Large TIFF files cause OutOfMemoryError:** `TiffOptions` को `Compression` `LZW` पर सेट करें और स्ट्रीमिंग सक्षम करें (`loadOptions.setBufferSize`) ताकि मेमोरी उपयोग कम रहे।  
- **Unexpected character encoding:** XMP को UTF‑8 की अपेक्षा होती है; हमेशा स्ट्रिंग्स को `StandardCharsets.UTF_8` के साथ पास करें ताकि डेटा गड़बड़ न हो।

## अक्सर पूछे जाने वाले प्रश्न

**Q: XMP मेटाडेटा क्या है?**  
A: XMP एक XML‑आधारित मानक है जो फ़ाइलों के भीतर सीधे वर्णनात्मक जानकारी एम्बेड करता है, जिससे अनुप्रयोगों में सुसंगत मेटाडेटा सक्षम होता है।

**Q: XMP मेटाडेटा क्यों महत्वपूर्ण है?**  
A: यह आपको छवियों को लेखक, कॉपीराइट, कीवर्ड, और कस्टम डेटा के साथ टैग करने देता है, जिससे खोज योग्यता और एसेट मैनेजमेंट बाहरी डेटाबेस के बिना सुधरता है।

**Q: क्या मैं छवि में एम्बेड करने के बाद XMP मेटाडेटा को संपादित कर सकता हूँ?**  
A: हाँ, Aspose.Imaging for Java मौजूदा XMP पैकेट को संशोधित करने और फ़ाइल में वापस लिखने के लिए मेथड प्रदान करता है।

**Q: क्या Aspose.Imaging for Java एक मुफ्त टूल है?**  
A: मूल्यांकन के लिए एक फ्री ट्रायल उपलब्ध है, लेकिन उत्पादन उपयोग के लिए एक पेड लाइसेंस आवश्यक है। आप विकल्पों को [Aspose.Imaging for Java website](https://purchase.aspose.com/buy) पर देख सकते हैं।

**Q: Aspose.Imaging for Java के लिए सहायता और समर्थन कहाँ प्राप्त कर सकते हैं?**  
A: समुदाय सहायता के लिए [Aspose.Imaging forums](https://forum.aspose.com/) पर जाएँ, या पेड‑लाइसेंस ग्राहकों के लिए सीधे Aspose सपोर्ट से संपर्क करें।

## निष्कर्ष

इस ट्यूटोरियल में, हमने Aspose.Imaging for Java, एक प्रमुख **java image processing library**, का उपयोग करके छवियों में XMP मेटाडेटा के साथ काम करने का तरीका खोजा। चरण‑दर‑चरण गाइड का पालन करके, आप आसानी से XMP डेटा एम्बेड, अपडेट, और रिट्रीव कर सकते हैं, जिससे आपके डिजिटल एसेट्स में खोज योग्य, मानक‑अनुपालन मेटाडेटा जुड़ जाता है।

---

**Last Updated:** 2026-05-18  
**Tested With:** Aspose.Imaging for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## संबंधित ट्यूटोरियल

- [Java इमेज प्रोसेसिंग में महारत: Aspose.Imaging के साथ EXIF डेटा संशोधित करें](/imaging/java/metadata-exif-operations/java-image-processing-copy-modify-exif-aspose-imaging/)
- [Aspose.Imaging के साथ Java इमेज प्रोसेसिंग: लोडिंग, एन्हांसिंग और इमेज सेविंग](/imaging/java/image-loading-saving/java-image-processing-aspose-imaging-load-adjust-save/)
- [Aspose.Imaging लाइब्रेरी के साथ उन्नत Java इमेज प्रोसेसिंग](/imaging/java/advanced-drawing-graphics/mastering-image-processing-java-aspose-imaging/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
        
String dataDir = "Your Document Directory" + "ConvertingImages/";
// Specify the size of image by defining a Rectangle
Rectangle rect = new Rectangle(0, 0, 100, 200);
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffJpegRgb);
tiffOptions.setPhotometric(TiffPhotometrics.MinIsBlack);
tiffOptions.setBitsPerSample(new int[] { 8 });
// create the brand new image just for sample purposes
try (TiffImage image = new TiffImage(new TiffFrame(tiffOptions, rect.getWidth(), rect.getHeight())))
{
	// create an instance of XMP-Header
	XmpHeaderPi xmpHeader = new XmpHeaderPi();
	xmpHeader.setGuid(dataDir);
	// create an instance of Xmp-TrailerPi
	XmpTrailerPi xmpTrailer = new XmpTrailerPi(true);
	// create an instance of XMP meta class to set different attributes
	XmpMeta xmpMeta = new XmpMeta();
	xmpMeta.addAttribute("Author", "Mr Smith");
	xmpMeta.addAttribute("Description", "The fake metadata value");
	// create an instance of XmpPacketWrapper that contains all metadata
	XmpPacketWrapper xmpData = new XmpPacketWrapper(xmpHeader, xmpTrailer, xmpMeta);
	// create an instance of Photoshop package and set photoshop attributes
	PhotoshopPackage photoshopPackage = new PhotoshopPackage();
	photoshopPackage.setCity("London");
	photoshopPackage.setCountry("England");
	photoshopPackage.setColorMode(ColorMode.Rgb);
	// add photoshop package into XMP metadata
	xmpData.addPackage(photoshopPackage);
	// create an instance of DublinCore package and set dublinCore attributes
	DublinCorePackage dublinCorePackage = new DublinCorePackage();
	dublinCorePackage.setAuthor("Charles Bukowski");
	dublinCorePackage.setTitle("Confessions of a Man Insane Enough to Live With the Beasts");
	dublinCorePackage.addValue("dc:movie", "Barfly");
	// add dublinCore Package into XMP metadata
	xmpData.addPackage(dublinCorePackage);
	ByteArrayOutputStream ms = new ByteArrayOutputStream();
	// update XMP metadata into image
	image.setXmpData(xmpData);
	// Save image on the disk or in memory stream
	image.save(ms);
	// Load the image from memory stream or from disk to read/get the metadata
	try (TiffImage img = (TiffImage) Image.load(new ByteArrayInputStream(ms.toByteArray())))
	{
		// Getting the XMP metadata
		XmpPacketWrapper imgXmpData = img.getXmpData();
		for (XmpPackage pack : imgXmpData.getPackages())
		{
			// Use package data ...
		}
	}
}
        
```