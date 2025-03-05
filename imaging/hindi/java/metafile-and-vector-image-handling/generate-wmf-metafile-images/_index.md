---
title: जावा के लिए Aspose.Imaging के साथ WMF छवियाँ बनाना
linktitle: WMF मेटाफ़ाइल छवियाँ उत्पन्न करें
second_title: Aspose.Imaging जावा इमेज प्रोसेसिंग एपीआई
description: Aspose.Imaging का उपयोग करके जावा में WMF मेटाफ़ाइल छवियां बनाना सीखें। शक्तिशाली छवि निर्माण क्षमताओं के लिए इस चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 10
url: /hi/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/
---
क्या आप अपने जावा अनुप्रयोगों के साथ WMF (विंडोज़ मेटाफ़ाइल) छवियां बनाना चाह रहे हैं? जावा के लिए Aspose.Imaging एक शक्तिशाली उपकरण है जो आपको आसानी से WMF छवियां उत्पन्न करने की अनुमति देता है। इस चरण-दर-चरण मार्गदर्शिका में, हम आपको WMF मेटाफ़ाइल छवियां बनाने के लिए जावा के लिए Aspose.Imaging का उपयोग करने की प्रक्रिया के बारे में बताएंगे। 

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित आवश्यक शर्तें हैं:

- आपके कंप्यूटर पर एक जावा विकास वातावरण स्थापित किया गया है।
-  जावा लाइब्रेरी के लिए Aspose.Imaging स्थापित किया गया। आप इसे यहां से डाउनलोड कर सकते हैं[वेबसाइट](https://releases.aspose.com/imaging/java/).
- जावा प्रोग्रामिंग का बुनियादी ज्ञान।

## पैकेज आयात करें

सबसे पहले, जावा के लिए Aspose.Imaging का उपयोग करने के लिए अपने जावा एप्लिकेशन के लिए आवश्यक पैकेज आयात करें:

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.color.*;
import com.aspose.imaging.coreexceptions.ImageLoadException;
import com.aspose.imaging.imageoptions.WmfOptions;
import com.aspose.imaging.internal.system.drawing.*;
import com.aspose.imaging.internal.system.drawing.imaging.*;
import com.aspose.imaging.pen.*;
import com.aspose.imaging.system.drawing.*;
```

## चरण 1: एक कैनवास बनाएं

 अपनी WMF छवि बनाना शुरू करने के लिए, आपको एक कैनवास बनाना होगा जहाँ आप आकृतियाँ बना सकें।`WmfRecorderGraphics2D` क्लास आपको यह कैनवास प्रदान करता है। यहां बताया गया है कि आप इसका उदाहरण कैसे बना सकते हैं:

```java
// दस्तावेज़ निर्देशिका का पथ.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

उपरोक्त कोड में, हम कैनवास आयाम (100x100) और रिज़ॉल्यूशन (96 डीपीआई) निर्दिष्ट करते हैं।

## चरण 2: पृष्ठभूमि का रंग सेट करें

 इसके बाद, अपने कैनवास के लिए पृष्ठभूमि का रंग परिभाषित करें। आप इसका उपयोग कर सकते हैं`setBackgroundColor` पृष्ठभूमि का रंग सेट करने की विधि:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

इस उदाहरण में, हमने पृष्ठभूमि का रंग सफ़ेद धुएँ पर सेट किया है।

## चरण 3: पेन और ब्रश को परिभाषित करें

कैनवास पर आकृतियाँ बनाने के लिए, आपको एक पेन और एक ब्रश को परिभाषित करने की आवश्यकता है। पेन का उपयोग रूपरेखा बनाने के लिए किया जाता है, और ब्रश का उपयोग आकृतियाँ भरने के लिए किया जाता है। यहां बताया गया है कि आप एक पेन और एक ठोस ब्रश कैसे बना सकते हैं:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

इस कोड में, हम एक नीला पेन और एक पीला-हरा ठोस ब्रश बनाते हैं।

## चरण 4: आकृतियाँ भरें और बनाएं

अब, आइए कैनवास पर कुछ बुनियादी आकृतियाँ भरें और बनाएं। हम बहुभुज से शुरुआत करेंगे:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

यहां, हम निर्दिष्ट पेन और ब्रश का उपयोग करके एक बहुभुज भरते हैं और बनाते हैं। आप आवश्यकतानुसार निर्देशांक और आकृतियों को समायोजित कर सकते हैं।

## चरण 5: हैचब्रश का उपयोग करें

 अपनी आकृतियों में बनावट जोड़ने के लिए, आप इसका उपयोग कर सकते हैं`HatchBrush`. उदाहरण के लिए:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

इस कोड में, हम सफेद और चांदी के रंगों के साथ एक क्रॉस-हैच ब्रश बनाते हैं।

## चरण 6: दीर्घवृत्त भरें और बनाएं

आइए कैनवास पर एक दीर्घवृत्त भरें और बनाएं:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

आप आवश्यकतानुसार दीर्घवृत्त की स्थिति और आकार को समायोजित कर सकते हैं।

## चरण 7: आर्क और क्यूबिक बेज़ियर बनाएं

अधिक जटिल आकृतियाँ बनाना भी संभव है। यहां एक चाप और एक घन बेज़ियर वक्र बनाने का तरीका बताया गया है:

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

उपरोक्त कोड में, हम पहले एक बिंदीदार रेखा शैली के साथ एक चाप बनाते हैं, और फिर हम एक ठोस लाल पेन के साथ एक घन बेजियर वक्र बनाते हैं।

## चरण 8: छवियाँ जोड़ें

आप अपने WMF मेटाफ़ाइल में छवियां भी जोड़ सकते हैं। इसे करने का तरीका यहां बताया गया है:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

इस चरण में, हम एक छवि लोड करते हैं और इसे कैनवास पर निर्दिष्ट निर्देशांक (50, 50) पर रखते हैं।

## चरण 9: रेखाएँ और पाई बनाएँ

रेखाएँ और पाई आकृतियाँ जोड़ने के लिए, आप इन उदाहरणों का अनुसरण कर सकते हैं:

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

यहां, हम एक रेखा खींचते हैं और निर्दिष्ट पेन और ब्रश का उपयोग करके एक पाई आकार भरते/खींचते हैं।

## चरण 10: पॉलीलाइन और टेक्स्ट बनाएं

टेक्स्ट और पॉलीलाइन जोड़ना सीधा है:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

आप आवश्यकतानुसार फ़ॉन्ट, टेक्स्ट और पॉलीलाइन बिंदुओं को अनुकूलित कर सकते हैं।

## चरण 11: WMF छवि सहेजें

एक बार जब आप अपनी WMF छवि बना लें, तो इसे सहेजने का समय आ गया है:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

यह कोड WMF छवि को निर्दिष्ट निर्देशिका में सहेजेगा।

इतना ही! आपने जावा के लिए Aspose.Imaging का उपयोग करके सफलतापूर्वक WMF मेटाफ़ाइल छवि तैयार की है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने पता लगाया है कि जावा के लिए Aspose.Imaging का उपयोग करके WMF मेटाफ़ाइल छवियां कैसे बनाई जाती हैं। हमने आवश्यक शर्तें शामिल कीं, पैकेज आयात किए, और विभिन्न आकृतियाँ बनाने, बनावट जोड़ने, चित्र सम्मिलित करने और अंतिम छवि को सहेजने के लिए चरण-दर-चरण निर्देश प्रदान किए। जावा के लिए Aspose.Imaging छवि हेरफेर और निर्माण के लिए उपकरणों का एक शक्तिशाली सेट प्रदान करता है, जो इसे आपके जावा अनुप्रयोगों के लिए एक मूल्यवान संसाधन बनाता है।

## अक्सर पूछे जाने वाले प्रश्न

### Q1: WMF छवि प्रारूप क्या है?

A1: WMF का मतलब विंडोज़ मेटाफ़ाइल है, जो एक वेक्टर ग्राफ़िक्स प्रारूप है जिसका उपयोग छवियों, रेखाचित्रों और अन्य ग्राफ़िकल डेटा को संग्रहीत करने के लिए किया जाता है। यह आमतौर पर विंडोज़ अनुप्रयोगों में उपयोग किया जाता है और गुणवत्ता की हानि के बिना इसे आसानी से बढ़ाया जा सकता है।

### Q2: मैं जावा के लिए Aspose.Imaging कहां से डाउनलोड कर सकता हूं?

 A2: आप जावा के लिए Aspose.Imaging को यहां से डाउनलोड कर सकते हैं[वेबसाइट](https://releases.aspose.com/imaging/java/).

### Q3: क्या मुझे जावा के लिए Aspose.Imaging का उपयोग करने के लिए उन्नत प्रोग्रामिंग कौशल की आवश्यकता है?

A3: जबकि बुनियादी जावा प्रोग्रामिंग ज्ञान आवश्यक है, जावा के लिए Aspose.Imaging एक उपयोगकर्ता के अनुकूल एपीआई प्रदान करता है जो छवि हेरफेर और निर्माण कार्यों को सरल बनाता है।

### Q4: क्या मैं व्यावसायिक उद्देश्यों के लिए जावा के लिए Aspose.Imaging का उपयोग कर सकता हूँ?

 A4: हां, जावा के लिए Aspose.Imaging व्यवसायों और डेवलपर्स के लिए वाणिज्यिक लाइसेंस प्रदान करता है। आप यहां से लाइसेंस खरीद सकते हैं[यहाँ](https://purchase.aspose.com/buy).

### Q5: मैं जावा के लिए Aspose.Imaging के बारे में समर्थन कहां से प्राप्त कर सकता हूं या प्रश्न पूछ सकता हूं?

 A5: आप Aspose समुदाय से समर्थन प्राप्त कर सकते हैं और उससे जुड़ सकते हैं[Aspose.इमेजिंग फ़ोरम](https://forum.aspose.com/).