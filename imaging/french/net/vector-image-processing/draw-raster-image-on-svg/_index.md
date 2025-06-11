---
"description": "Apprenez à dessiner des images raster sur SVG avec Aspose.Imaging pour .NET. Améliorez vos applications .NET avec des images dynamiques."
"linktitle": "Dessiner une image raster au format SVG dans Aspose.Imaging pour .NET"
"second_title": "API de traitement d'images .NET Aspose.Imaging"
"title": "Comment dessiner une image raster au format SVG dans Aspose.Imaging pour .NET"
"url": "/fr/net/vector-image-processing/draw-raster-image-on-svg/"
"weight": 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Comment dessiner une image raster au format SVG dans Aspose.Imaging pour .NET


Dans le monde de la programmation .NET, Aspose.Imaging est une bibliothèque fiable et polyvalente pour gérer diverses tâches liées aux images. Elle offre notamment la possibilité de dessiner une image matricielle sur un canevas SVG. Dans ce guide étape par étape, nous vous expliquerons comment dessiner une image matricielle sur un fichier SVG avec Aspose.Imaging pour .NET.

## Prérequis

Avant de plonger dans les détails, assurez-vous que vous disposez des conditions préalables suivantes :

- Aspose.Imaging pour .NET : la bibliothèque doit être installée. Sinon, vous pouvez la télécharger depuis le [Page de téléchargement d'Aspose.Imaging pour .NET](https://releases.aspose.com/imaging/net/).

- Votre répertoire de documents : remplacer `"Your Document Directory"` avec le chemin réel vers votre répertoire de travail.

Maintenant, décomposons le processus en étapes faciles à suivre :

## Étape 1 : Importer les espaces de noms nécessaires

Vous devez importer les espaces de noms requis pour travailler avec Aspose.Imaging :

```csharp
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Svg;
using Aspose.Imaging.FileFormats.Svg.Graphics;
using System;
```

## Étape 2 : Charger les images

- Tout d’abord, chargez l’image raster que vous souhaitez dessiner sur le canevas SVG.

```csharp
string dataDir = "Your Document Directory";
using (RasterImage imageToDraw = (RasterImage)Image.Load(dataDir + "asposenet_220_src01.png"))
```

- Ensuite, chargez l’image canevas SVG à l’endroit où vous souhaitez dessiner l’image raster.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Étape 3 : Dessiner sur l'image SVG

Vous pouvez maintenant commencer à dessiner sur l'image SVG existante. Pour cela, vous devez créer une instance de `SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Étape 4 : Dessiner l'image raster

- Définissez les limites où vous souhaitez dessiner l’image raster et spécifiez la région source de l’image raster.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Étape 5 : Enregistrer le résultat

Après avoir dessiné l'image raster sur le canevas SVG, vous pouvez enregistrer l'image résultante :

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Conclusion

Félicitations ! Vous avez réussi à dessiner une image raster sur un canevas SVG avec Aspose.Imaging pour .NET. Cela peut s'avérer extrêmement utile pour créer des images riches et dynamiques dans vos applications .NET.

Pour plus d'informations et une documentation détaillée, visitez le [Documentation d'Aspose.Imaging pour .NET](https://reference.aspose.com/imaging/net/).

## Questions fréquemment posées

### Qu'est-ce qu'Aspose.Imaging pour .NET ?
   Aspose.Imaging pour .NET est une puissante bibliothèque de traitement d'images qui permet aux développeurs de créer, manipuler et convertir des images dans divers formats au sein d'applications .NET.

### Puis-je utiliser Aspose.Imaging pour .NET dans des projets commerciaux ?
   Oui, vous pouvez utiliser Aspose.Imaging pour .NET dans des projets commerciaux et non commerciaux. Les détails de la licence sont disponibles sur le site [page d'achat](https://purchase.aspose.com/buy).

### Existe-t-il un essai gratuit disponible ?
   Oui, vous pouvez obtenir un essai gratuit d'Aspose.Imaging pour .NET à partir de [ici](https://releases.aspose.com/).

### Où puis-je obtenir de l’aide ou poser des questions ?
   Si vous avez des questions ou besoin d'assistance, vous pouvez visiter le [Forum Aspose.Imaging](https://forum.aspose.com/).

### Comment puis-je obtenir une licence temporaire pour Aspose.Imaging pour .NET ?
   Vous pouvez obtenir un permis temporaire auprès de [ici](https://purchase.aspose.com/temporary-license/).




{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}