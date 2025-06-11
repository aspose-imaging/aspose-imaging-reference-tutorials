---
"description": "जानें कि .NET के लिए Aspose.Imaging का उपयोग करके DICOM छवियों में XMP मेटाडेटा कैसे जोड़ें। इस चरण-दर-चरण मार्गदर्शिका के साथ छवि प्रबंधन और संगठन को अनुकूलित करें।"
"linktitle": ".NET के लिए Aspose.Imaging में XMP टैग संग्रहीत करने का समर्थन करें"
"second_title": "Aspose.Imaging .NET इमेज प्रोसेसिंग API"
"title": ".NET के लिए Aspose.Imaging में XMP टैग संग्रहीत करने का समर्थन करें"
"url": "/hi/net/dicom-image-processing/support-storing-xmp-tags/"
"weight": 25
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# .NET के लिए Aspose.Imaging में XMP टैग संग्रहीत करने का समर्थन करें

Aspose.Imaging for .NET एक शक्तिशाली लाइब्रेरी है जो आपको .NET वातावरण में विभिन्न छवि प्रारूपों के साथ काम करने की अनुमति देती है। इस ट्यूटोरियल में, हम यह पता लगाएंगे कि Aspose.Imaging for .NET में XMP (एक्सटेंसिबल मेटाडेटा प्लेटफ़ॉर्म) टैग को संग्रहीत करने का समर्थन कैसे करें। छवियों में मेटाडेटा जानकारी जोड़ने के लिए XMP टैग आवश्यक हैं, जिससे आपकी डिजिटल संपत्तियों को व्यवस्थित और प्रबंधित करना आसान हो जाता है। हम इस प्रक्रिया को कई चरणों में विभाजित करेंगे ताकि आपको यह समझने में मदद मिल सके कि इसे कैसे प्राप्त किया जाए।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:

- Aspose.Imaging for .NET: आपके पास Aspose.Imaging for .NET इंस्टॉल होना चाहिए। आप इसे यहाँ से डाउनलोड कर सकते हैं [.NET वेबसाइट के लिए Aspose.Imaging](https://releases.aspose.com/imaging/net/).

## नामस्थान आयात करें

अपने .NET प्रोजेक्ट में, Aspose.Imaging के साथ काम करने के लिए आवश्यक नामस्थान आयात करें:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.Exif;
using Aspose.Imaging.FileFormats.Dicom;
```

अब, आइए .NET के लिए Aspose.Imaging का उपयोग करके XMP टैग संग्रहीत करने के लिए चरण-दर-चरण मार्गदर्शिका में गोता लगाएँ।

## चरण 1: DICOM छवि लोड करें

उस DICOM छवि को लोड करके शुरू करें जिसके साथ आप काम करना चाहते हैं। `"Your Document Directory"` वास्तविक निर्देशिका पथ के साथ जहां आपकी DICOM छवि स्थित है।

```csharp
string dataDir = "Your Document Directory";
using (DicomImage image = (DicomImage)Image.Load(dataDir + "file.dcm"))
{
    // आपका कोड यहां जाएगा
}
```

## चरण 2: एक XMP पैकेट और Dicom पैकेज बनाएँ

अपना मेटाडेटा संग्रहीत करने के लिए एक XmpPacketWrapper और DicomPackage बनाएँ। आप विभिन्न मेटाडेटा फ़ील्ड सेट कर सकते हैं, जैसे कि संस्थान, निर्माता, रोगी विवरण, श्रृंखला जानकारी और अध्ययन विवरण।

```csharp
XmpPacketWrapper xmpPacketWrapper = new XmpPacketWrapper();
DicomPackage dicomPackage = new DicomPackage();

dicomPackage.SetEquipmentInstitution("Test Institution");
dicomPackage.SetEquipmentManufacturer("Test Manufacturer");
dicomPackage.SetPatientBirthDate("19010101");
dicomPackage.SetPatientId("010101");
dicomPackage.SetPatientName("Test Name");
dicomPackage.SetPatientSex("M");
dicomPackage.SetSeriesDateTime("19020202");
dicomPackage.SetSeriesDescription("Test Series Description");
dicomPackage.SetSeriesModality("Test Modality");
dicomPackage.SetSeriesNumber("01");
dicomPackage.SetStudyDateTime("19030303");
dicomPackage.SetStudyDescription("Test Study Description");
dicomPackage.SetStudyId("02");
dicomPackage.SetStudyPhysician("Test Physician");

xmpPacketWrapper.AddPackage(dicomPackage);
```

## चरण 3: छवि को XMP मेटाडेटा के साथ सहेजें

अब, जोड़े गए XMP मेटाडेटा के साथ छवि को सहेजें `DicomOptions` कक्षा।

```csharp
string outputFile = dataDir + "output.dcm";
image.Save(outputFile, new DicomOptions() { XmpData = xmpPacketWrapper });
```

## चरण 4: XMP टैग सत्यापित करें

सहेजी गई छवि को लोड करें और XMP टैग जोड़ने से पहले और बाद में DICOM जानकारी की तुलना करें।

```csharp
using (DicomImage imageSaved = (DicomImage)Image.Load(outputFile))
{
    List<string> originalDicomInfo = image.FileInfo.DicomInfo;
    List<string> imageSavedDicomInfo = imageSaved.FileInfo.DicomInfo;
    int tagsCountDiff = Math.Abs(imageSavedDicomInfo.Count - originalDicomInfo.Count);
}
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा कि .NET के लिए Aspose.Imaging का उपयोग करके DICOM छवियों में XMP टैग संग्रहीत करने का समर्थन कैसे करें। अपनी छवियों में मेटाडेटा जोड़ना संगठन और प्रबंधन के लिए महत्वपूर्ण है। Aspose.Imaging इस प्रक्रिया को सरल बनाता है और आपको छवि मेटाडेटा के साथ कुशलतापूर्वक काम करने में सक्षम बनाता है।

अधिक जानकारी और उन्नत उपयोग के लिए, आप देख सकते हैं [Aspose.Imaging for .NET दस्तावेज़](https://reference.aspose.com/imaging/net/).

## अक्सर पूछे जाने वाले प्रश्न

### प्रश्न 1: XMP मेटाडेटा क्या है?

A1: XMP (एक्सटेंसिबल मेटाडेटा प्लेटफ़ॉर्म) डिजिटल संपत्तियों में मेटाडेटा जोड़ने के लिए एक मानक है, जिसमें इमेज भी शामिल हैं। यह फ़ाइल की विभिन्न विशेषताओं को व्यवस्थित करने और उनका वर्णन करने में मदद करता है।

### प्रश्न 2: क्या मैं .NET के लिए Aspose.Imaging का उपयोग करके मौजूदा XMP मेटाडेटा को संपादित कर सकता हूं?

A2: हाँ, आप Aspose.Imaging का उपयोग करके मौजूदा XMP मेटाडेटा को संपादित कर सकते हैं और छवियों में नया मेटाडेटा जोड़ सकते हैं।

### प्रश्न 3: क्या Aspose.Imaging for .NET व्यावसायिक इमेज प्रोसेसिंग कार्यों के लिए उपयुक्त है?

A3: बिल्कुल। Aspose.Imaging for .NET छवि हेरफेर, संपादन और रूपांतरण के लिए सुविधाओं की एक विस्तृत श्रृंखला प्रदान करता है, जो इसे पेशेवर उपयोग के लिए उपयुक्त बनाता है।

### प्रश्न 4: मैं Aspose.Imaging for .NET के बारे में सहायता कहां से प्राप्त कर सकता हूं या प्रश्न कहां पूछ सकता हूं?

A4: आप यहां जा सकते हैं [Aspose.Imaging for .NET फ़ोरम](https://forum.aspose.com/) सहायता प्राप्त करने और अपने कोई भी प्रश्न पूछने के लिए।

### प्रश्न 5: मैं Aspose.Imaging for .NET के लिए अस्थायी लाइसेंस कैसे प्राप्त कर सकता हूं?

A5: आप यहाँ जाकर Aspose.Imaging for .NET के लिए अस्थायी लाइसेंस प्राप्त कर सकते हैं [इस लिंक](https://purchase.aspose.com/temporary-license/).


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}