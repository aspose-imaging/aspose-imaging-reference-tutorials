---
title: Autres options de redimensionnement d'image de DICOM dans Aspose.Imaging pour .NET
linktitle: Autres options de redimensionnement d'image de DICOM dans Aspose.Imaging pour .NET
second_title: API de traitement d'images Aspose.Imaging .NET
description: Découvrez comment redimensionner des images DICOM à l'aide d'Aspose.Imaging pour .NET. Un guide étape par étape pour une manipulation efficace des images médicales.
weight: 20
url: /fr/net/dicom-image-processing/dicoms-other-image-resizing-options/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Autres options de redimensionnement d'image de DICOM dans Aspose.Imaging pour .NET

Souhaitez-vous travailler avec des images DICOM (Digital Imaging and Communications in Medicine) dans votre application .NET ? Aspose.Imaging for .NET fournit un ensemble d'outils puissants pour manipuler efficacement les images DICOM. Dans ce didacticiel, nous approfondirons les «Autres options de redimensionnement d'image de DICOM» à l'aide d'Aspose.Imaging pour .NET. Nous couvrirons les conditions préalables, importerons les espaces de noms et fournirons un guide étape par étape pour vous aider à comprendre et à mettre en œuvre efficacement le redimensionnement des images DICOM.

## Conditions préalables

Avant de commencer, assurez-vous que les conditions préalables suivantes sont remplies :

1. Installer Aspose.Imaging pour .NET
Pour travailler avec des images DICOM à l'aide d'Aspose.Imaging pour .NET, vous devez installer la bibliothèque. Vous pouvez le télécharger sur le site Web.

[Télécharger Aspose.Imaging pour .NET](https://releases.aspose.com/imaging/net/)

2. Mettre en place un environnement de développement
Assurez-vous d'avoir configuré un environnement de développement .NET, y compris Visual Studio ou tout autre IDE compatible.

3. Image DICOM
Vous devez disposer d'un fichier image DICOM (par exemple, "file.dcm") que vous souhaitez redimensionner à l'aide d'Aspose.Imaging pour .NET.

## Importer des espaces de noms

Dans votre code C#, vous devez importer les espaces de noms nécessaires pour utiliser Aspose.Imaging. Voici comment procéder :

```csharp
using Aspose.Imaging;
using Aspose.Imaging.ImageOptions;
```

Maintenant, décomposons le processus de redimensionnement de l'image en plusieurs étapes.

## Étape 1 : Charger l'image DICOM
Pour commencer, vous devez charger l'image DICOM depuis votre système de fichiers.

```csharp
string dataDir = "Your Document Directory";
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
{
    // Votre code ici
}
```

## Étape 2 : Redimensionner proportionnellement à la hauteur
Vous pouvez redimensionner l'image DICOM proportionnellement en spécifiant la hauteur en pixels et le type de redimensionnement. Dans cet exemple, nous utilisons « AdaptiveResample » comme type de redimensionnement.

```csharp
image.ResizeHeightProportionally(100, ResizeType.AdaptiveResample);
```

## Étape 3 : Enregistrez l'image redimensionnée
Après avoir redimensionné l'image, vous pouvez l'enregistrer au format souhaité. Ici, nous l'enregistrons sous forme d'image BMP.

```csharp
image.Save(dataDir + "DICOMSOtherImageResizingOptions_out.bmp", new BmpOptions());
```

## Étape 4 : Redimensionner proportionnellement à la largeur
Vous pouvez également redimensionner l'image DICOM proportionnellement en spécifiant la largeur en pixels et le type de redimensionnement.

```csharp
image1.ResizeWidthProportionally(150, ResizeType.AdaptiveResample);
```

## Étape 5 : Enregistrez l'image redimensionnée
Enregistrez l'image redimensionnée en tant qu'image BMP, comme à l'étape précédente.

```csharp
image1.Save(dataDir + "DICOMSOtherImageResizingOptions1_out.bmp", new BmpOptions());
```

Toutes nos félicitations! Vous avez réussi à redimensionner une image DICOM à l'aide d'Aspose.Imaging pour .NET. Cette bibliothèque offre diverses options pour manipuler les images DICOM, ce qui en fait un outil précieux pour les applications de soins de santé et d'imagerie médicale.

## Conclusion

Dans ce didacticiel, nous avons exploré les « Autres options de redimensionnement d'image de DICOM » à l'aide d'Aspose.Imaging pour .NET. Nous avons couvert les conditions préalables, importé les espaces de noms et fourni un guide étape par étape pour redimensionner les images DICOM. Aspose.Imaging for .NET simplifie le processus de travail avec des images médicales, offrant un large éventail de fonctionnalités pour les applications de soins de santé.

Vous avez d’autres questions ou avez besoin d’aide avec Aspose.Imaging pour .NET ? Consultez la documentation ou visitez le forum de la communauté Aspose pour obtenir de l'aide :

- [Aspose.Imaging pour .NET Documentation](https://reference.aspose.com/imaging/net/)
- [Prise en charge d'Aspose.Imaging pour .NET](https://forum.aspose.com/)

## FAQ

### Q1 : Qu’est-ce que DICOM ?

A1 : DICOM signifie Imagerie numérique et communications en médecine. Il s'agit d'une norme permettant de transmettre, de stocker et de partager des images médicales, telles que des radiographies, des IRM et des tomodensitogrammes, au format numérique.

### Q2 : Puis-je utiliser Aspose.Imaging pour .NET gratuitement ?

A2 : Aspose.Imaging pour .NET est une bibliothèque commerciale. Vous pouvez télécharger une version d'essai gratuite pour évaluer ses fonctionnalités, mais une licence est requise pour une utilisation complète.

### Q3 : Quelles autres options de manipulation d’images Aspose.Imaging pour .NET propose-t-il ?

A3 : Aspose.Imaging pour .NET offre une large gamme d'options de traitement d'image, notamment la conversion de format, l'amélioration d'image et le dessin sur des images. Vous pouvez explorer l’ensemble des fonctionnalités dans la documentation.

### Q4 : Aspose.Imaging pour .NET est-il adapté aux applications de soins de santé ?

A4 : Oui, Aspose.Imaging pour .NET est couramment utilisé dans les applications de soins de santé pour gérer les images DICOM, ce qui en fait un outil précieux pour le développement de logiciels d'imagerie médicale.

### Q5 : Puis-je obtenir une licence temporaire pour Aspose.Imaging pour .NET ?
w
 R5 : Oui, vous pouvez obtenir une licence temporaire à des fins de tests et d'évaluation. Visite[Page de licence temporaire d'Aspose](https://purchase.aspose.com/temporary-license/) pour plus d'informations.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
