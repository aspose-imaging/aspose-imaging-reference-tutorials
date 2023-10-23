---
title: Images DICOM en niveaux de gris avec Aspose.Imaging pour .NET
linktitle: Niveaux de gris sur DICOM dans Aspose.Imaging pour .NET
second_title: API de traitement d'images Aspose.Imaging .NET
description: Découvrez comment effectuer une échelle de gris sur des images DICOM avec Aspose.Imaging for .NET, une puissante bibliothèque de traitement d'image.
type: docs
weight: 24
url: /fr/net/dicom-image-processing/grayscale-on-dicom/
---
Si vous travaillez avec des données d'imagerie médicale au format DICOM et devez effectuer des transformations en niveaux de gris, Aspose.Imaging for .NET offre une solution puissante. Dans ce didacticiel étape par étape, nous vous guiderons tout au long du processus de mise à l'échelle des gris d'une image DICOM à l'aide d'Aspose.Imaging. Cette bibliothèque est un outil polyvalent qui vous permet de travailler avec différents formats d'image, dont DICOM, dans un environnement .NET. Commençons!

## Conditions préalables

Avant de commencer, assurez-vous que les conditions préalables suivantes sont remplies :

1.  Aspose.Imaging pour .NET : vous devez avoir installé cette bibliothèque. Vous pouvez le télécharger depuis le[Page de téléchargement d'Aspose.Imaging pour .NET](https://releases.aspose.com/imaging/net/).

2. Image DICOM : vous devriez avoir une image DICOM que vous souhaitez mettre en niveaux de gris. Si vous n'en avez pas, vous pouvez trouver des exemples d'images DICOM à des fins de test.

## Importer des espaces de noms

Tout d'abord, importons les espaces de noms nécessaires pour travailler avec Aspose.Imaging :

```csharp
using System;
using System.IO;
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

Maintenant que vous avez les prérequis en place et les espaces de noms importés, nous pouvons procéder au processus de mise à l'échelle des gris étape par étape.

## Étape 1 : initialiser l'image DICOM

 Nous commençons par initialiser l'image DICOM. Dans cet exemple, nous supposons que le fichier DICOM s'appelle "file.dcm" et se trouve dans un répertoire spécifié par`dataDir`.

```csharp
string dataDir = "Your Document Directory";
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
```

## Étape 2 : Transformation en niveaux de gris

 L'étape suivante consiste à transformer l'image DICOM chargée en sa représentation en niveaux de gris à l'aide du`Grayscale()` méthode. Cette méthode convertit automatiquement l'image en niveaux de gris.

```csharp
{
    // Transformer l'image en sa représentation en niveaux de gris
    image.Grayscale();
}
```

## Étape 3 : Enregistrez l'image en niveaux de gris

 Après avoir mis l'image en niveaux de gris, vous pouvez enregistrer l'image résultante. Dans cet exemple, nous l'enregistrons au format BMP en utilisant le`BmpOptions()`.

```csharp
image.Save(dataDir + "GrayscalingOnDICOM_out.bmp", new BmpOptions());
```

## Conclusion

Dans ce didacticiel, nous avons appris à effectuer une mise à l'échelle des gris sur une image DICOM à l'aide d'Aspose.Imaging pour .NET. Cette bibliothèque simplifie le processus de travail avec les données d'imagerie médicale et vous permet d'effectuer facilement diverses transformations. Que vous travailliez sur la recherche médicale ou sur des applications de soins de santé, Aspose.Imaging peut être un outil précieux dans votre boîte à outils de développement .NET.

## FAQ

### Q1 : Qu’est-ce que DICOM ?

A1 : DICOM signifie Imagerie numérique et communications en médecine. Il s'agit d'une norme pour la manipulation, le stockage, l'impression et la transmission d'images médicales.

### Q2 : Aspose.Imaging est-il adapté au traitement d’images non médicales ?

A2 : Oui, Aspose.Imaging est une bibliothèque polyvalente capable de gérer une large gamme de formats d'image pour diverses applications au-delà de l'imagerie médicale.

### Q3 : Où puis-je trouver plus de documentation ?

 A3 : Vous pouvez vous référer au[Documentation Aspose.Imaging pour .NET](https://reference.aspose.com/imaging/net/) pour des informations détaillées et des exemples.

### Q4 : Existe-t-il un essai gratuit ?

 A4 : Oui, vous pouvez accéder à un[essai gratuit d'Aspose.Imaging](https://releases.aspose.com/) pour évaluer ses capacités.

### Q5 : Comment puis-je obtenir de l'aide pour Aspose.Imaging ?

 A5 : Si vous avez des questions ou avez besoin d'aide, vous pouvez visiter le[Forum Aspose.Imaging](https://forum.aspose.com/) pour demander de l’aide à la communauté ou contacter leur équipe d’assistance.