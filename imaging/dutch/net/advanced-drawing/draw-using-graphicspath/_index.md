---
date: 2026-01-30
description: Leer hoe je tekst op een afbeelding tekent, vormen tekent en vormen vult
  met een patroon met behulp van Aspose.Imaging voor .NET.
linktitle: Draw Using GraphicsPath – draw text on image, shapes and patterns
second_title: Aspose.Imaging .NET Image Processing API
title: Hoe tekst op een afbeelding te tekenen met Aspose.Imaging voor .NET
url: /nl/net/advanced-drawing/draw-using-graphicspath/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Hoe Tekst op Afbeelding Tekenen met Aspose.Imaging voor .NET

In deze tutorial lopen we stap voor stap **uit hoe je tekst op een afbeelding tekent** en laten we ook zien hoe je vormen op een afbeelding tekent en vormen vult met een patroon met behulp van de krachtige Aspose.Imaging‑bibliotheek. Of je nu een rapportagetool bouwt, een aangepaste badge‑generator, of gewoon programmatically afbeeldingen wilt annoteren, de onderstaande stappen geven je een solide basis.

## Snelle Antwoorden
- **Wat kan ik tekenen?** Tekst, basisvormen (ellips, rechthoek) en patroonvullingen.  
- **Welke klasse staat centraal?** `GraphicsPath` gecombineerd met `Graphics`.  
- **Heb ik een licentie nodig?** Een gratis proefversie werkt voor ontwikkeling; een licentie is vereist voor productie.  
- **Ondersteunde formaten?** BMP, PNG, JPEG, TIFF en nog veel meer via Aspose.Imaging.  
- **Voorvereisten?** Visual Studio, .NET 6+ (of .NET Framework 4.6+), en Aspose.Imaging voor .NET.

## Wat is tekst op afbeelding tekenen met Aspose.Imaging?
Aspose.Imaging biedt een high‑level API die de low‑level GDI+‑aanroepen abstraheert. Door het `Graphics`‑object te gebruiken samen met een `GraphicsPath`, kun je vector‑gebaseerde tekeningen samenstellen — tekst, vormen en patroonvullingen — en deze renderen op een bitmap of een ander ondersteund afbeeldingsformaat.

## Waarom vormen op afbeelding tekenen en vormen vullen met een patroon?
- **Visuele nadruk:** Markeer gebieden met aangepaste hatch‑patronen.  
- **Branding:** Voeg bedrijfslogo’s of watermerken toe die tekst en graphics combineren.  
- **Dynamische graphics:** Genereer grafieken, badges of certificaten on‑the‑fly zonder externe ontwerptools.

## Voorvereisten

1. **Visual Studio** – elke recente editie (Community, Professional of Enterprise).  
2. **Aspose.Imaging voor .NET** – download het van de officiële site: [Download Aspose.Imaging for .NET](https://releases.aspose.com/imaging/net/).  
3. **Basiskennis C#** – je moet vertrouwd zijn met klassen, namespaces en de `using`‑directive.

## Namespaces Importeren

Open je project en zorg ervoor dat de Aspose.Imaging‑namespace beschikbaar is:

```csharp
using Aspose.Imaging;
```

## Stap 1: De Omgeving Instellen

Eerst maken we een leeg canvas dat onze tekening zal bevatten.

```csharp
public static void Run()
{
    Console.WriteLine("Running example DrawingUsingGraphicsPath");
    string dataDir = "Your Document Directory";

    // Create an instance of BmpOptions and set its various properties
    BmpOptions ImageOptions = new BmpOptions();
    ImageOptions.BitsPerPixel = 24;

    // Create an instance of FileCreateSource and assign it to Source property
    ImageOptions.Source = new FileCreateSource(dataDir + "sample_1.bmp", false);

    // Create an instance of Image and initialize an instance of Graphics
    using (Image image = Image.Create(ImageOptions, 500, 500))
    {
        Graphics graphics = new Graphics(image);
        graphics.Clear(Color.White);
```

Hier configureren we een BMP van 500 × 500 pixel met een witte achtergrond, klaar om op te tekenen.

## Stap 2: GraphicsPath Maken, Vormen en Tekst Toevoegen

Nu bouwen we een `GraphicsPath` die zowel vormen **als de tekst die we op de afbeelding willen tekenen** bevat.

```csharp
        GraphicsPath graphicspath = new GraphicsPath();
        Figure figure = new Figure();

        figure.AddShape(new EllipseShape(new RectangleF(0, 0, 499, 499)));
        figure.AddShape(new RectangleShape(new RectangleF(0, 0, 499, 499)));
        figure.AddShape(new TextShape("Aspose.Imaging", new RectangleF(170, 225, 170, 100), new Font("Arial", 20), StringFormat.GenericTypographic));

        graphicspath.AddFigures(new[] { figure });
```

- **TextShape**” rechullen met een Hatch‑Patroon

Met het pad klaar, tekenen we het met een pen en vullen we vervolgens de binnenkant met een hatch‑brush — dit demonstreert **vormen vullen met patroon**.

```csharp
        graphics.DrawPath(new Pen(Color.Blue), graphicspath);

        // Create an instance of HatchBrush and set its properties
        HatchBrush hatchbrush = new HatchBrush();
        hatchbrush.BackgroundColor = Color.Brown;
        hatchbrush.ForegroundColor = Color.Blue;
        hatchbrush.HatchStyle = HatchStyle.Vertical;

        graphics.FillPath(hatchbrush, graphicspath);

        image.Save();
        Console.WriteLine("Processing completed successfully.");
    }
    Console.WriteLine("Finished example DrawingUsingGraphicsPath");
}
```

De `HatchBrush` schildert een verticaal blauw lijntje‑patroon over een bruine achtergrond, waardoor de vormen een onderscheidende uitstraling krijgen.

## Veelvoorkomende Toepassingen

| Scenario | Hoe de code helpt |
|----------|--------------------|
| **Badge‑generatie** | Combineer een bedrijfslogo (ellips), een rand (rechthoek) en de naam van de medewerker (tekst) in één afbeelding. |
| **Dynamische grafieken** | Teken data‑gedreven vormen en annoteer ze met waarden via `TextShape`. |
| **Watermerken** | Render semi‑transparante tekst over een bestaande foto en vul een achtergrondpatroon voor subtiele branding. |

## Problemen Oplossen & Tips

- **Bestandspaden** – Zorg dat `dataDir` naar een beschrijfbare map wijst; anders gooit `FileCreateSource` een uitzondering.  
- **Kleurcontrast** – Bij gebruik van patroonvullingen, kies voor‑ en achtergrondkleuren die voldoende contrast bieden voor leesbaarheid.  
- **Prestaties** – Voor grote afbeeldingen, overweeg `RasterImage` in plaats van `BmpOptions` om het geheugenverbruik te verlagen.

## Veelgestelde Vragen

**V: Is Aspose.Imaging voor .NET compatibel met de nieuwste .NET‑frameworks?**  
A: Ja, de bibliotheek wordt regelmatig bijgewerkt om .NET 6, .NET 7 en de nieuwste .NET Framework‑versies te ondersteunen.

**V: Kan ik de getekende afbeelding naar een ander formaat converteren (bijv. PNG of JPEG)?**  
A: Absoluut. Na het opslaan van de BMP kun je deze laden met `Image.Load` en `Save` aanroepen met een andere bestandsextensie.

**V: Waar vind ik meer gedetailleerde documentatie?**  
A: Bezoek de officiële docs op [Aspose.Imaging documentation](https://reference.aspose.com/imaging/net/).

**V: Is er een gratis proefversie beschikbaar?**  
A: Ja, je kunt een proefversie downloaden via [hier](https://releases.aspose.com/).

**V: Hoe koop ik een licentie voor productiegebruik?**  
A: Licenties kunnen direct worden gekocht in de Aspose‑winkel: [deze link](https://purchase.aspose.com/buy).

## Conclusie

Je hebt nu geleerd hoe je **tekst op afbeelding tekent**, **vormen op afbeelding tekent**, en **vormen vult met patroon** met behulp van de `GraphicsPath`‑API van Aspose.Imaging. Met deze bouwblokken kun je rijke, programmatiche graphics maken voor rapporten, dashboards of elke aangepaste visuele output in je .NET‑applicaties.

Als je tegen problemen aanloopt of je creaties wilt delen, voel je vrij om deel te nemen aan de community op het [Aspose.Imaging Forum](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Laatst bijgewerkt:** 2026-01-30  
**Getest met:** Aspose.Imaging 24.12 voor .NET  
**Auteur:** Aspose