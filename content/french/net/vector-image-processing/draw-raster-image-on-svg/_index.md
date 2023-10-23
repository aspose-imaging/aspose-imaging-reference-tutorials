---
title: Comment dessiner une image raster sur SVG dans Aspose.Imaging pour .NET
linktitle: Dessiner une image raster sur SVG dans Aspose.Imaging pour .NET
second_title: API de traitement d'images Aspose.Imaging .NET
description: Apprenez à dessiner des images raster sur SVG à l'aide d'Aspose.Imaging pour .NET. Améliorez vos applications .NET avec des images dynamiques.
type: docs
weight: 11
url: /fr/net/vector-image-processing/draw-raster-image-on-svg/
---

Dans le monde de la programmation .NET, Aspose.Imaging se présente comme une bibliothèque fiable et polyvalente pour gérer diverses tâches liées aux images. Une fonctionnalité fascinante qu'il offre est la possibilité de dessiner une image raster sur un canevas SVG. Dans ce guide étape par étape, nous vous guiderons tout au long du processus de dessin d'une image raster sur un SVG à l'aide d'Aspose.Imaging pour .NET.

## Conditions préalables

Avant d’entrer dans les détails, assurez-vous d’avoir les conditions préalables suivantes en place :

-  Aspose.Imaging pour .NET : vous devez avoir installé la bibliothèque. Sinon, vous pouvez le télécharger depuis le[Page de téléchargement d'Aspose.Imaging pour .NET](https://releases.aspose.com/imaging/net/).

-  Votre répertoire de documents : remplacer`"Your Document Directory"` avec le chemin réel vers votre répertoire de travail.

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

- Ensuite, chargez l’image du canevas SVG à l’endroit où vous souhaitez dessiner l’image raster.

```csharp
using (SvgImage canvasImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
```

## Étape 3 : Dessiner sur l'image SVG

 Vous pouvez maintenant commencer à dessiner sur l’image SVG existante. Pour ce faire, vous devez créer une instance de`SvgGraphics2D`:

```csharp
SvgGraphics2D graphics = new SvgGraphics2D(canvasImage);
```

## Étape 4 : dessiner l'image raster

- Définissez les limites où vous souhaitez dessiner l'image raster et spécifiez la région source à partir de l'image raster.

```csharp
graphics.DrawImage(
    new Rectangle(0, 0, imageToDraw.Width, imageToDraw.Height),
    new Rectangle(67, 67, imageToDraw.Width, imageToDraw.Height),
    imageToDraw);
```

## Étape 5 : Enregistrez le résultat

Après avoir dessiné l'image raster sur le canevas SVG, vous pouvez enregistrer l'image résultante :

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawImage.svg");
}
```

## Conclusion

Toutes nos félicitations! Vous avez réussi à dessiner une image raster sur un canevas SVG à l'aide d'Aspose.Imaging pour .NET. Cela peut être incroyablement utile pour créer des images riches et dynamiques au sein de vos applications .NET.

 Pour plus d’informations et une documentation détaillée, visitez le[Documentation Aspose.Imaging pour .NET](https://reference.aspose.com/imaging/net/).

## Questions fréquemment posées

### Qu’est-ce qu’Aspose.Imaging pour .NET ?
   Aspose.Imaging for .NET est une puissante bibliothèque de traitement d'images qui permet aux développeurs de créer, manipuler et convertir des images dans différents formats au sein d'applications .NET.

### Puis-je utiliser Aspose.Imaging pour .NET dans des projets commerciaux ?
    Oui, vous pouvez utiliser Aspose.Imaging pour .NET dans des projets commerciaux et non commerciaux. Les détails de la licence peuvent être trouvés sur le[page d'achat](https://purchase.aspose.com/buy).

### Existe-t-il un essai gratuit disponible ?
    Oui, vous pouvez obtenir un essai gratuit d'Aspose.Imaging pour .NET à partir de[ici](https://releases.aspose.com/).

### Où puis-je obtenir de l'aide ou poser des questions ?
    Si vous avez des questions ou avez besoin d'aide, vous pouvez visiter le[Forum Aspose.Imaging](https://forum.aspose.com/).

### Comment puis-je obtenir une licence temporaire pour Aspose.Imaging for .NET ?
    Vous pouvez obtenir une licence temporaire auprès de[ici](https://purchase.aspose.com/temporary-license/).


