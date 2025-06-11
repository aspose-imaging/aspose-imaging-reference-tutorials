---
"description": "Aspose.Imaging का उपयोग करके Java में WMF मेटाफ़ाइल छवियाँ बनाना सीखें। शक्तिशाली छवि निर्माण क्षमताओं के लिए इस चरण-दर-चरण मार्गदर्शिका का पालन करें।"
"linktitle": "WMF मेटाफ़ाइल छवियाँ उत्पन्न करें"
"second_title": "Aspose.Imaging जावा इमेज प्रोसेसिंग API"
"title": "Java के लिए Aspose.Imaging के साथ WMF छवियाँ बनाना"
"url": "/hi/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/"
"weight": 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Java के लिए Aspose.Imaging के साथ WMF छवियाँ बनाना

क्या आप अपने Java अनुप्रयोगों के साथ WMF (Windows मेटाफ़ाइल) छवियाँ बनाना चाहते हैं? Aspose.Imaging for Java एक शक्तिशाली उपकरण है जो आपको आसानी से WMF छवियाँ बनाने की अनुमति देता है। इस चरण-दर-चरण मार्गदर्शिका में, हम आपको WMF मेटाफ़ाइल छवियाँ बनाने के लिए Aspose.Imaging for Java का उपयोग करने की प्रक्रिया से अवगत कराएँगे। 

## आवश्यक शर्तें

आरंभ करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- आपके कंप्यूटर पर स्थापित जावा विकास वातावरण.
- Aspose.Imaging for Java लाइब्रेरी स्थापित है। आप इसे यहाँ से डाउनलोड कर सकते हैं [वेबसाइट](https://releases.aspose.com/imaging/java/).
- जावा प्रोग्रामिंग का बुनियादी ज्ञान.

## पैकेज आयात करें

सबसे पहले, Aspose.Imaging for Java का उपयोग करने के लिए अपने Java अनुप्रयोग के लिए आवश्यक पैकेज आयात करें:

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

## चरण 1: कैनवास बनाएं

अपनी WMF छवि बनाना शुरू करने के लिए, आपको एक कैनवास बनाना होगा जहाँ आप आकृतियाँ बना सकें। `WmfRecorderGraphics2D` क्लास आपको यह कैनवास प्रदान करता है। यहाँ बताया गया है कि आप इसका एक उदाहरण कैसे बना सकते हैं:

```java
// दस्तावेज़ निर्देशिका का पथ.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

उपरोक्त कोड में, हम कैनवास आयाम (100x100) और रिज़ॉल्यूशन (96 DPI) निर्दिष्ट करते हैं।

## चरण 2: पृष्ठभूमि रंग सेट करें

इसके बाद, अपने कैनवास के लिए पृष्ठभूमि का रंग निर्धारित करें। आप इसका उपयोग कर सकते हैं `setBackgroundColor` पृष्ठभूमि रंग सेट करने की विधि:

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

इस उदाहरण में, हमने पृष्ठभूमि का रंग सफेद धुआँ निर्धारित किया है।

## चरण 3: पेन और ब्रश को परिभाषित करें

कैनवास पर आकृतियाँ बनाने के लिए, आपको एक पेन और एक ब्रश की आवश्यकता होती है। पेन का उपयोग रूपरेखा बनाने के लिए किया जाता है, और ब्रश का उपयोग आकृतियों को भरने के लिए किया जाता है। यहाँ बताया गया है कि आप पेन और एक ठोस ब्रश कैसे बना सकते हैं:

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

इस कोड में, हम एक नीला पेन और एक पीला-हरा ठोस ब्रश बनाते हैं।

## चरण 4: आकृतियाँ भरें और बनाएँ

अब, आइए कैनवास पर कुछ बुनियादी आकृतियाँ भरें और बनाएँ। हम एक बहुभुज से शुरुआत करेंगे:

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

यहाँ, हम निर्दिष्ट पेन और ब्रश का उपयोग करके एक बहुभुज भरते हैं और बनाते हैं। आप आवश्यकतानुसार निर्देशांक और आकृतियों को समायोजित कर सकते हैं।

## चरण 5: हैचब्रश का उपयोग करें

अपनी आकृतियों में बनावट जोड़ने के लिए, आप इसका उपयोग कर सकते हैं `HatchBrush`। उदाहरण के लिए:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

इस कोड में, हम सफेद और सिल्वर रंगों से एक क्रॉस-हैच ब्रश बनाते हैं।

## चरण 6: दीर्घवृत्त भरें और बनाएं

आइये कैनवास पर एक दीर्घवृत्त भरें और बनाएं:

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

आप आवश्यकतानुसार दीर्घवृत्त की स्थिति और आकार को समायोजित कर सकते हैं।

## चरण 7: आर्क और क्यूबिक बेज़ियर बनाएं

अधिक जटिल आकृतियाँ बनाना भी संभव है। यहाँ बताया गया है कि चाप और क्यूबिक बेज़ियर वक्र कैसे बनाएं:

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

आप अपनी WMF मेटाफ़ाइल में छवियाँ भी जोड़ सकते हैं। इसे करने का तरीका इस प्रकार है:

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

इस चरण में, हम एक छवि लोड करते हैं और इसे निर्दिष्ट निर्देशांक (50, 50) पर कैनवास पर रखते हैं।

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

टेक्स्ट और पॉलीलाइन जोड़ना सरल है:

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

आप आवश्यकतानुसार फ़ॉन्ट, पाठ और पॉलीलाइन बिंदुओं को अनुकूलित कर सकते हैं।

## चरण 11: WMF छवि सहेजें

एक बार जब आप अपनी WMF छवि बना लेते हैं, तो उसे सहेजने का समय आ जाता है:

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

यह कोड WMF छवि को निर्दिष्ट निर्देशिका में सहेज देगा।

बस! आपने Aspose.Imaging for Java का उपयोग करके सफलतापूर्वक WMF मेटाफ़ाइल छवि तैयार कर ली है।

## निष्कर्ष

इस ट्यूटोरियल में, हमने जावा के लिए Aspose.Imaging का उपयोग करके WMF मेटाफ़ाइल छवियाँ बनाने का तरीका खोजा है। हमने आवश्यक पूर्वापेक्षाएँ, आयातित पैकेजों को कवर किया, और विभिन्न आकृतियों को बनाने, बनावट जोड़ने, छवियाँ सम्मिलित करने और अंतिम छवि को सहेजने के लिए चरण-दर-चरण निर्देश प्रदान किए। जावा के लिए Aspose.Imaging छवि हेरफेर और निर्माण के लिए उपकरणों का एक शक्तिशाली सेट प्रदान करता है, जो इसे आपके जावा अनुप्रयोगों के लिए एक मूल्यवान संसाधन बनाता है।

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: WMF छवि प्रारूप क्या है?

A1: WMF का मतलब है विंडोज मेटाफाइल, जो एक वेक्टर ग्राफिक्स प्रारूप है जिसका उपयोग छवियों, रेखाचित्रों और अन्य ग्राफिकल डेटा को संग्रहीत करने के लिए किया जाता है। इसका उपयोग आमतौर पर विंडोज अनुप्रयोगों में किया जाता है और गुणवत्ता में कमी के बिना इसे आसानी से बढ़ाया जा सकता है।

### प्रश्न 2: मैं Java के लिए Aspose.Imaging कहां से डाउनलोड कर सकता हूं?

A2: आप Aspose.Imaging for Java को यहाँ से डाउनलोड कर सकते हैं [वेबसाइट](https://releases.aspose.com/imaging/java/).

### प्रश्न 3: क्या मुझे Java के लिए Aspose.Imaging का उपयोग करने के लिए उन्नत प्रोग्रामिंग कौशल की आवश्यकता है?

A3: जबकि बुनियादी जावा प्रोग्रामिंग ज्ञान की आवश्यकता है, Aspose.Imaging for Java एक उपयोगकर्ता के अनुकूल API प्रदान करता है जो छवि हेरफेर और निर्माण कार्यों को सरल करता है।

### प्रश्न 4: क्या मैं व्यावसायिक उद्देश्यों के लिए Aspose.Imaging for Java का उपयोग कर सकता हूँ?

A4: हाँ, Aspose.Imaging for Java व्यवसायों और डेवलपर्स के लिए वाणिज्यिक लाइसेंस प्रदान करता है। आप यहाँ से लाइसेंस खरीद सकते हैं [यहाँ](https://purchase.aspose.com/buy).

### प्रश्न 5: मैं Aspose.Imaging for Java के बारे में सहायता कहां से प्राप्त कर सकता हूं या प्रश्न कहां पूछ सकता हूं?

A5: आप Aspose समुदाय से सहायता प्राप्त कर सकते हैं और उससे जुड़ सकते हैं [Aspose.Imaging फ़ोरम](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}