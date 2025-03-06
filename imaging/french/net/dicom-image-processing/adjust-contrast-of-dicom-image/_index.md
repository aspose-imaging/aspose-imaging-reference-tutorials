---
title: Réglage du contraste de l'image DICOM avec Aspose.Imaging pour .NET
linktitle: Ajuster le contraste de l'image DICOM dans Aspose.Imaging pour .NET
second_title: API de traitement d'images Aspose.Imaging .NET
description: Améliorez les images médicales avec Aspose.Imaging pour .NET. Ajustez le contraste de l’image DICOM en quelques étapes simples.
weight: 11
url: /fr/net/dicom-image-processing/adjust-contrast-of-dicom-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Réglage du contraste de l'image DICOM avec Aspose.Imaging pour .NET

Dans le monde de l’imagerie médicale, un contrôle précis de la qualité des images est primordial. Aspose.Imaging for .NET fournit une solution puissante pour manipuler facilement les images DICOM. Dans ce didacticiel étape par étape, nous vous guiderons tout au long du processus de réglage du contraste d'une image DICOM à l'aide d'Aspose.Imaging pour .NET. Ce didacticiel est conçu pour ceux qui souhaitent améliorer la visibilité des images médicales à des fins de diagnostic ou de recherche. 

## Conditions préalables

Avant de plonger dans le didacticiel, vous devez remplir quelques conditions préalables :

1. Aspose.Imaging pour la bibliothèque .NET
 La bibliothèque Aspose.Imaging for .NET doit être installée. Vous pouvez trouver la bibliothèque et la documentation détaillée sur le[Page Aspose.Imaging pour .NET](https://reference.aspose.com/imaging/net/).

2. Environnement de développement
Assurez-vous d'avoir configuré un environnement de développement .NET, tel que Visual Studio.

Maintenant que nous avons les prérequis couverts, commençons à régler le contraste d'une image DICOM étape par étape.

## Importation des espaces de noms nécessaires

Pour commencer, vous devez importer les espaces de noms requis pour votre projet. Cela vous permet d'accéder aux classes et méthodes nécessaires pour travailler avec des images DICOM.

### Étape 1 : Importer les espaces de noms

```csharp
using System;
using System.IO;
using Aspose.Imaging;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.FileFormats.Dicom.DicomImage;
using Aspose.Imaging.ImageOptions;
```

Assurez-vous d'inclure ces espaces de noms en haut de votre fichier de code C#.

## Guide étape par étape

Maintenant que nous avons importé les espaces de noms nécessaires, décomposons le processus d'ajustement du contraste d'une image DICOM en plusieurs étapes.

### Étape 2 : définir le répertoire des documents

Tout d’abord, vous devez spécifier le répertoire où se trouve votre image DICOM.

```csharp
string dataDir = "Your Document Directory";
```

 Remplacer`"Your Document Directory"` avec le chemin réel vers votre image DICOM.

### Étape 3 : Charger l'image DICOM

Dans cette étape, nous chargeons l'image DICOM à partir du flux de fichiers spécifié.

```csharp
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
```

 Ici,`"file.dcm"` doit être remplacé par le nom de fichier de votre image DICOM.

### Étape 4 : Ajustez le contraste

Pour améliorer la visibilité de l'image DICOM, vous pouvez régler le contraste. La ligne de code suivante augmente le contraste de 50 %.

```csharp
image.AdjustContrast(50);
```

 Vous pouvez modifier la valeur`50` pour répondre à vos besoins spécifiques en matière de réglage du contraste.

### Étape 5 : Enregistrez l'image résultante

 Pour conserver l'image modifiée, vous devez la sauvegarder. Créer une instance de`BmpOptions` pour l'image résultante, puis enregistrez-la.

```csharp
image.Save(dataDir + "AdjustContrastDICOM_out.bmp", new BmpOptions());
```

 Remplacer`"AdjustContrastDICOM_out.bmp"`avec le nom de fichier de sortie souhaité.

## Conclusion

Dans ce didacticiel, nous avons exploré comment ajuster le contraste d'une image DICOM à l'aide d'Aspose.Imaging pour .NET. Grâce à la puissance de cette bibliothèque, vous pouvez affiner les images médicales pour les rendre plus informatives et adaptées à des fins de diagnostic ou de recherche.

 Pour plus d'informations, visitez le[Documentation Aspose.Imaging pour .NET](https://reference.aspose.com/imaging/net/) . Si vous ne l'avez pas déjà fait, vous pouvez télécharger la bibliothèque depuis[ici](https://releases.aspose.com/imaging/net/) ou obtenir un permis temporaire auprès de[ce lien](https://purchase.aspose.com/temporary-license/).

Avez-vous des questions sur la manipulation d'images DICOM ou sur l'utilisation d'Aspose.Imaging pour .NET ? Répondons à quelques requêtes courantes dans la FAQ ci-dessous.

## FAQ

### Q1 : Qu'est-ce qu'un format d'image DICOM ?

A1 : DICOM signifie Imagerie numérique et communications en médecine. Il s'agit d'un format standard utilisé pour le stockage et l'échange d'images médicales, telles que les radiographies et les IRM.

### Q2 : Puis-je ajuster le contraste d’autres formats d’image à l’aide d’Aspose.Imaging pour .NET ?

A2 : Aspose.Imaging pour .NET prend principalement en charge les images DICOM. Vous pouvez consulter la documentation pour vérifier la compatibilité avec d'autres formats.

### Q3 : Aspose.Imaging pour .NET est-il gratuit ?

 A3 : Aspose.Imaging for .NET est une bibliothèque commerciale, mais vous pouvez l'explorer avec un essai gratuit disponible[ici](https://releases.aspose.com/).

### Q4 : Existe-t-il d'autres ajustements d'image que je peux effectuer avec Aspose.Imaging pour .NET ?

A4 : Oui, Aspose.Imaging pour .NET fournit un large éventail de fonctionnalités de manipulation d'images, notamment le redimensionnement, le recadrage et le filtrage.

### Q5 : Puis-je utiliser Aspose.Imaging pour .NET pour le traitement d’images non médicales ?

A5 : Absolument ! Bien qu'Aspose.Imaging soit polyvalent pour le traitement d'images médicales, il peut également être utilisé pour des tâches générales de manipulation d'images.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
