---
"description": "Découvrez comment effectuer une mise à l’échelle des gris sur des images DICOM avec Aspose.Imaging pour .NET, une puissante bibliothèque de traitement d’images."
"linktitle": "Niveaux de gris sur DICOM dans Aspose.Imaging pour .NET"
"second_title": "API de traitement d'images .NET Aspose.Imaging"
"title": "Images DICOM en niveaux de gris avec Aspose.Imaging pour .NET"
"url": "/fr/net/dicom-image-processing/grayscale-on-dicom/"
"weight": 24
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Images DICOM en niveaux de gris avec Aspose.Imaging pour .NET

Si vous travaillez avec des données d'imagerie médicale au format DICOM et devez effectuer des transformations en niveaux de gris, Aspose.Imaging pour .NET offre une solution performante. Dans ce tutoriel, nous vous guiderons pas à pas dans la mise en niveaux de gris d'une image DICOM avec Aspose.Imaging. Cette bibliothèque est un outil polyvalent qui vous permet de travailler avec différents formats d'image, dont DICOM, dans un environnement .NET. C'est parti !

## Prérequis

Avant de commencer, assurez-vous de disposer des prérequis suivants :

1. Aspose.Imaging pour .NET : cette bibliothèque doit être installée. Vous pouvez la télécharger depuis le [Page de téléchargement d'Aspose.Imaging pour .NET](https://releases.aspose.com/imaging/net/).

2. Image DICOM : Vous devez disposer d'une image DICOM que vous souhaitez mettre en niveaux de gris. Si vous n'en avez pas, vous pouvez trouver des exemples d'images DICOM à des fins de test.

## Importer des espaces de noms

Tout d’abord, importons les espaces de noms nécessaires pour travailler avec Aspose.Imaging :

```csharp
using System;
using System.IO;
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

Maintenant que vous avez les prérequis en place et les espaces de noms importés, nous pouvons procéder au processus de mise à l'échelle des gris étape par étape.

## Étape 1 : Initialiser l'image DICOM

Nous commençons par initialiser l'image DICOM. Dans cet exemple, nous supposons que le fichier DICOM s'appelle « file.dcm » et se trouve dans un répertoire spécifié par `dataDir`.

```csharp
string dataDir = "Your Document Directory";
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
```

## Étape 2 : Transformation en niveaux de gris

L'étape suivante consiste à transformer l'image DICOM chargée en sa représentation en niveaux de gris à l'aide de `Grayscale()` méthode. Cette méthode convertit automatiquement l'image en niveaux de gris.

```csharp
{
    // Transformer l'image en sa représentation en niveaux de gris
    image.Grayscale();
}
```

## Étape 3 : Enregistrer l’image en niveaux de gris

Après avoir mis l'image en niveaux de gris, vous pouvez enregistrer l'image résultante. Dans cet exemple, nous l'enregistrons au format BMP en utilisant le `BmpOptions()`.

```csharp
image.Save(dataDir + "GrayscalingOnDICOM_out.bmp", new BmpOptions());
```

## Conclusion

Dans ce tutoriel, nous avons appris à appliquer des niveaux de gris à une image DICOM avec Aspose.Imaging pour .NET. Cette bibliothèque simplifie le traitement des données d'imagerie médicale et vous permet d'effectuer facilement diverses transformations. Que vous travailliez sur la recherche médicale ou les applications de santé, Aspose.Imaging peut s'avérer un outil précieux pour votre développement .NET.

## FAQ

### Q1 : Qu'est-ce que DICOM ?

A1 : DICOM signifie Digital Imaging and Communications in Medicine (imagerie et communications numériques en médecine). Il s'agit d'une norme pour la manipulation, le stockage, l'impression et la transmission d'images médicales.

### Q2 : Aspose.Imaging est-il adapté au traitement d'images non médicales ?

A2 : Oui, Aspose.Imaging est une bibliothèque polyvalente capable de gérer une large gamme de formats d’images pour diverses applications au-delà de l’imagerie médicale.

### Q3 : Où puis-je trouver plus de documentation ?

A3 : Vous pouvez vous référer au [Documentation d'Aspose.Imaging pour .NET](https://reference.aspose.com/imaging/net/) pour des informations détaillées et des exemples.

### Q4 : Existe-t-il un essai gratuit disponible ?

A4 : Oui, vous pouvez accéder à un [essai gratuit d'Aspose.Imaging](https://releases.aspose.com/) pour évaluer ses capacités.

### Q5 : Comment puis-je obtenir de l'aide pour Aspose.Imaging ?

A5 : Si vous avez des questions ou avez besoin d'aide, vous pouvez visiter le [Forum Aspose.Imaging](https://forum.aspose.com/) pour demander de l'aide à la communauté ou contacter leur équipe d'assistance.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}