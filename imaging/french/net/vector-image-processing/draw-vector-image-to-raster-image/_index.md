---
"description": "Apprenez à convertir des images vectorielles en images raster dans .NET avec Aspose.Imaging. Un guide étape par étape pour un traitement d'images efficace."
"linktitle": "Convertir une image vectorielle en image raster dans Aspose.Imaging pour .NET"
"second_title": "API de traitement d'images .NET Aspose.Imaging"
"title": "Convertir une image vectorielle en image raster dans Aspose.Imaging pour .NET"
"url": "/fr/net/vector-image-processing/draw-vector-image-to-raster-image/"
"weight": 13
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Convertir une image vectorielle en image raster dans Aspose.Imaging pour .NET


Vous souhaitez convertir facilement des images vectorielles en images raster dans vos applications .NET ? Aspose.Imaging pour .NET offre une solution efficace. Dans ce guide étape par étape, nous vous expliquerons comment convertir des images vectorielles en images raster avec Aspose.Imaging pour .NET. 

## Prérequis

Avant de plonger dans le didacticiel, assurez-vous que vous disposez des prérequis suivants :

### 1. Aspose.Imaging pour .NET

Aspose.Imaging pour .NET doit être installé. Si ce n'est pas le cas, vous pouvez le télécharger depuis le site web à l'adresse [Télécharger Aspose.Imaging pour .NET](https://releases.aspose.com/imaging/net/).

### 2. Environnement de développement .NET

Assurez-vous d'avoir un environnement de développement .NET configuré sur votre ordinateur. Vous pouvez utiliser Visual Studio ou tout autre outil de développement .NET.

Décomposons maintenant le processus de dessin d’images vectorielles en images raster en étapes simples et faciles à suivre :

## Étape 1 : Initialisez votre projet

Commencez par créer un nouveau projet .NET dans votre environnement de développement. Assurez-vous d'avoir intégré Aspose.Imaging pour .NET à votre projet.

## Étape 2 : charger l'image vectorielle

Dans cette étape, nous chargeons l’image vectorielle (au format SVG) que vous souhaitez convertir en image raster.

```csharp
string dataDir = "Your Document Directory";

using (SvgImage svgImage = (SvgImage)Image.Load(dataDir + "asposenet_220_src02.svg"))
{
    // ...
}
```

## Étape 3 : pixelliser l'image vectorielle

Nous devons maintenant pixelliser l'image SVG au format PNG. C'est ici qu'intervient la conversion du vecteur au raster.

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

## Étape 5 : Dessiner l'image raster

Nous pouvons maintenant dessiner l’image raster sur l’image SVG existante.

```csharp
Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D graphics =
    new Aspose.Imaging.FileFormats.Svg.Graphics.SvgGraphics2D(svgImage);

int width = imageToDraw.Width / 2;
int height = imageToDraw.Height / 2;
Point origin = new Point((svgImage.Width - width) / 2, (svgImage.Height - height) / 2);
Size size = new Size(width, height);
graphics.DrawImage(imageToDraw, origin, size);
```

## Étape 6 : Enregistrer le résultat

Enfin, enregistrez l'image résultante. Vous disposez désormais d'une image matricielle incluant votre image vectorielle.

```csharp
using (SvgImage resultImage = graphics.EndRecording())
{
    resultImage.Save(dataDir + "asposenet_220_src02.DrawVectorImage.svg");
}
```

## Conclusion

Dans ce tutoriel, nous avons montré comment convertir des images vectorielles en images raster avec Aspose.Imaging pour .NET. Grâce à ces étapes simples, vous pourrez facilement intégrer cette fonctionnalité à vos applications .NET.

### Questions fréquemment posées

### Qu'est-ce qu'Aspose.Imaging pour .NET ?
Aspose.Imaging pour .NET est une bibliothèque .NET qui fournit de puissantes fonctionnalités de traitement d'image, notamment la possibilité de travailler avec différents formats d'image, de convertir des images et d'effectuer des tâches avancées de manipulation d'image.

### Où puis-je trouver la documentation d'Aspose.Imaging pour .NET ?
Vous pouvez trouver la documentation d'Aspose.Imaging pour .NET [ici](https://reference.aspose.com/imaging/net/).

### Existe-t-il une version d'essai gratuite disponible ?
Oui, vous pouvez accéder à un essai gratuit d'Aspose.Imaging pour .NET [ici](https://releases.aspose.com/).

### Comment obtenir une licence temporaire pour Aspose.Imaging pour .NET ?
Si vous avez besoin d’un permis temporaire, vous pouvez en obtenir un [ici](https://purchase.aspose.com/temporary-license/).

### Où puis-je obtenir de l'aide pour Aspose.Imaging pour .NET ?
Pour toute assistance ou question, vous pouvez visiter le [Forum Aspose.Imaging](https://forum.aspose.com/).


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}