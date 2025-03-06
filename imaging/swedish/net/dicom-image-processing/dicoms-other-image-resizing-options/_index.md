---
title: DICOMs andra bildstorleksändringsalternativ i Aspose.Imaging för .NET
linktitle: DICOMs andra bildstorleksändringsalternativ i Aspose.Imaging för .NET
second_title: Aspose.Imaging .NET Image Processing API
description: Lär dig hur du ändrar storlek på DICOM-bilder med Aspose.Imaging för .NET. En steg-för-steg-guide för effektiv medicinsk bildmanipulation.
weight: 20
url: /sv/net/dicom-image-processing/dicoms-other-image-resizing-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DICOMs andra bildstorleksändringsalternativ i Aspose.Imaging för .NET

Vill du arbeta med DICOM-bilder (Digital Imaging and Communications in Medicine) i din .NET-applikation? Aspose.Imaging för .NET tillhandahåller en kraftfull uppsättning verktyg för att manipulera DICOM-bilder effektivt. I den här handledningen kommer vi att fördjupa oss i "DICOMs andra alternativ för bildändringsstorlek" med Aspose.Imaging för .NET. Vi kommer att täcka förutsättningarna, importera namnutrymmen och tillhandahålla en steg-för-steg-guide som hjälper dig att förstå och implementera DICOM-bildstorleksändring på ett effektivt sätt.

## Förutsättningar

Innan vi börjar, se till att du har följande förutsättningar på plats:

1. Installera Aspose.Imaging för .NET
För att arbeta med DICOM-bilder med Aspose.Imaging för .NET måste du installera biblioteket. Du kan ladda ner den från webbplatsen.

[Ladda ner Aspose.Imaging för .NET](https://releases.aspose.com/imaging/net/)

2. Skapa en utvecklingsmiljö
Se till att du har en .NET-utvecklingsmiljö inställd, inklusive Visual Studio eller någon annan kompatibel IDE.

3. DICOM-bild
Du bör ha en DICOM-bildfil (t.ex. "file.dcm") som du vill ändra storlek på med Aspose.Imaging för .NET.

## Importera namnområden

I din C#-kod måste du importera de nödvändiga namnrymden för att använda Aspose.Imaging. Så här gör du:

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
```

Låt oss nu dela upp processen för att ändra storlek på bilder i flera steg.

## Steg 1: Ladda DICOM-bilden
För att börja måste du ladda DICOM-bilden från ditt filsystem.

```csharp
string dataDir = "Your Document Directory";
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
{
    // Din kod här
}
```

## Steg 2: Ändra storlek efter höjd proportionellt
Du kan ändra storlek på DICOM-bilden proportionellt genom att ange höjden i pixlar och storleksändringstypen. I det här exemplet använder vi "AdaptiveResample" som storleksändringstyp.

```csharp
image.ResizeHeightProportionally(100, ResizeType.AdaptiveResample);
```

## Steg 3: Spara den ändrade storleken på bilden
När du har ändrat storlek på bilden kan du spara den i önskat format. Här sparar vi den som en BMP-bild.

```csharp
image.Save(dataDir + "DICOMSOtherImageResizingOptions_out.bmp", new BmpOptions());
```

## Steg 4: Ändra storlek efter bredd proportionellt
Du kan också ändra storlek på DICOM-bilden proportionellt genom att ange bredden i pixlar och storleksändringstypen.

```csharp
image1.ResizeWidthProportionally(150, ResizeType.AdaptiveResample);
```

## Steg 5: Spara den ändrade storleken på bilden
Spara den ändrade storleken som en BMP-bild, precis som i föregående steg.

```csharp
image1.Save(dataDir + "DICOMSOtherImageResizingOptions1_out.bmp", new BmpOptions());
```

Grattis! Du har lyckats ändra storlek på en DICOM-bild med Aspose.Imaging för .NET. Det här biblioteket erbjuder olika alternativ för att manipulera DICOM-bilder, vilket gör det till ett värdefullt verktyg för vård och medicinsk bildbehandling.

## Slutsats

I den här handledningen utforskade vi "DICOMs andra alternativ för bildstorleksändring" med Aspose.Imaging för .NET. Vi täckte förutsättningarna, importerade namnutrymmen och gav en steg-för-steg-guide för att ändra storlek på DICOM-bilder. Aspose.Imaging för .NET förenklar processen att arbeta med medicinska bilder, och erbjuder ett brett utbud av funktioner för vårdapplikationer.

Har du fler frågor eller behöver hjälp med Aspose.Imaging för .NET? Kolla in dokumentationen eller besök Aspose community-forum för support:

- [Aspose.Imaging för .NET-dokumentation](https://reference.aspose.com/imaging/net/)
- [Aspose.Imaging för .NET-stöd](https://forum.aspose.com/)

## FAQ's

### F1: Vad är DICOM?

A1: DICOM står för Digital Imaging and Communications in Medicine. Det är en standard för att överföra, lagra och dela medicinska bilder, såsom röntgen, MRI och CT-skanningar, i digitalt format.

### F2: Kan jag använda Aspose.Imaging för .NET gratis?

S2: Aspose.Imaging för .NET är ett kommersiellt bibliotek. Du kan ladda ner en gratis testversion för att utvärdera dess funktioner, men en licens krävs för full användning.

### F3: Vilka andra bildmanipuleringsalternativ erbjuder Aspose.Imaging för .NET?

S3: Aspose.Imaging för .NET erbjuder ett brett utbud av bildbehandlingsalternativ, inklusive formatkonvertering, bildförbättring och ritning på bilder. Du kan utforska hela uppsättningen funktioner i dokumentationen.

### F4: Är Aspose.Imaging för .NET lämpligt för vårdtillämpningar?

S4: Ja, Aspose.Imaging för .NET används ofta i hälsovårdstillämpningar för att hantera DICOM-bilder, vilket gör det till ett värdefullt verktyg för utveckling av medicinsk bildbehandling.

### F5: Kan jag få en tillfällig licens för Aspose.Imaging för .NET?
w
 S5: Ja, du kan få en tillfällig licens för test- och utvärderingsändamål. Besök[Asposes tillfälliga licenssida](https://purchase.aspose.com/temporary-license/) för mer information.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
