---
title: Dessiner une image vectorielle sur une image raster dans Aspose.Imaging pour .NET
linktitle: Dessiner une image vectorielle sur une image raster dans Aspose.Imaging pour .NET
second_title: API de traitement d'images Aspose.Imaging .NET
description: Découvrez comment convertir des images vectorielles en images raster dans .NET à l'aide d'Aspose.Imaging. Un guide étape par étape pour un traitement d’image efficace.
type: docs
weight: 13
url: /fr/net/vector-image-processing/draw-vector-image-to-raster-image/
---

Cherchez-vous à convertir des images vectorielles en images raster sans effort dans vos applications .NET ? Aspose.Imaging for .NET fournit une solution efficace pour cette tâche. Dans ce guide étape par étape, nous vous guiderons tout au long du processus de dessin d'images vectorielles sur des images raster à l'aide d'Aspose.Imaging pour .NET. 

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

### 1. Aspose.Imaging pour .NET

 Aspose.Imaging pour .NET devrait être installé. Si vous ne l'avez pas, vous pouvez le télécharger sur le site officiel à l'adresse[Télécharger Aspose.Imaging pour .NET](https://releases.aspose.com/imaging/net/).

### 2. Environnement de développement .NET

Assurez-vous d'avoir un environnement de développement .NET configuré sur votre ordinateur. Vous pouvez utiliser Visual Studio ou tout autre outil de développement .NET.

Maintenant, décomposons le processus de dessin d'images vectorielles en images raster en étapes simples et faciles à suivre :

## Étape 1 : initialisez votre projet

Commencez par créer un nouveau projet .NET dans votre environnement de développement. Assurez-vous que Aspose.Imaging pour .NET est intégré à votre projet.

## Étape 2 : charger l'image vectorielle

Dans cette étape, nous chargeons l'image vectorielle (au format SVG) que vous souhaitez convertir en image raster.

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ...
}
```

## Étape 3 : pixelliser l'image vectorielle

Maintenant, nous devons pixelliser l'image SVG au format PNG. C'est là que se produit la conversion du vecteur en raster.

```csharp
SvgRasterizationOptions rasterizationOptions = new SvgRasterizationOptions();
rasterizationOptions.PageSize = svgImage.Size;
PngOptions saveOptions = new PngOptions();
saveOptions.VectorRasterizationOptions = rasterizationOptions;
svgImage.Save(drawnImageStream, saveOptions);
```

## Étape 4 : Charger l'image raster

Après la rastérisation, chargez l'image PNG à partir du flux pour un dessin ultérieur.

```csharp
drawnImageStream.Seek(0, System.IO.SeekOrigin.Begin);
using (RasterImage imageToDraw = (RasterImage)Image.Load(drawnImageStream))
{
    // ...
}
```

## Étape 5 : dessiner l'image raster

Maintenant, nous pouvons dessiner l'image raster sur l'image SVG existante.

```csharp
Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D graphics =
    new Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D(svgImage);

int width = imageToDraw.Width / 2;
int height = imageToDraw.Height / 2;
Point origin = new Point((svgImage.Width - width) / 2, (svgImage.Height - height) / 2);
Size size = new Size(width, height);
graphics.DrawImage(imageToDraw, origin, size);
```

## Étape 6 : Enregistrez le résultat

Enfin, enregistrez l'image résultante. Vous disposez maintenant d’une image raster qui inclut votre image vectorielle.

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## Conclusion

Dans ce didacticiel, nous avons montré comment convertir des images vectorielles en images raster à l'aide d'Aspose.Imaging pour .NET. Avec ces étapes simples, vous pouvez facilement intégrer cette fonctionnalité dans vos applications .NET.

### Questions fréquemment posées

### Qu’est-ce qu’Aspose.Imaging pour .NET ?
Aspose.Imaging for .NET est une bibliothèque .NET qui fournit de puissantes fonctionnalités de traitement d'image, notamment la possibilité de travailler avec différents formats d'image, de convertir des images et d'effectuer des tâches avancées de manipulation d'images.

### Où puis-je trouver la documentation officielle d’Aspose.Imaging pour .NET ?
 Vous pouvez trouver la documentation officielle d'Aspose.Imaging pour .NET[ici](https://reference.aspose.com/imaging/net/).

### Existe-t-il une version d'essai gratuite disponible ?
 Oui, vous pouvez accéder à un essai gratuit d'Aspose.Imaging pour .NET[ici](https://releases.aspose.com/).

### Comment puis-je obtenir une licence temporaire pour Aspose.Imaging pour .NET ?
 Si vous avez besoin d'un permis temporaire, vous pouvez en obtenir un[ici](https://purchase.aspose.com/temporary-license/).

### Où puis-je obtenir de l’assistance pour Aspose.Imaging pour .NET ?
 Pour toute assistance ou question, vous pouvez visiter le[Forum Aspose.Imaging](https://forum.aspose.com/).
