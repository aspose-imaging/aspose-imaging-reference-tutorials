---
title: Ajustez la luminosité de l'image DICOM avec Aspose.Imaging pour .NET
linktitle: Ajuster la luminosité de l'image DICOM dans Aspose.Imaging pour .NET
second_title: API de traitement d'images Aspose.Imaging .NET
description: Découvrez comment régler la luminosité de l’image DICOM dans Aspose.Imaging pour .NET. Améliorez facilement les images médicales.
weight: 10
url: /fr/net/dicom-image-processing/adjust-brightness-of-dicom-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajustez la luminosité de l'image DICOM avec Aspose.Imaging pour .NET

Dans le monde de l’imagerie médicale, la gestion des fichiers DICOM (Digital Imaging and Communications in Medicine) est de la plus haute importance. Ces fichiers contiennent des données médicales vitales et il est parfois nécessaire d'apporter des ajustements aux images qu'ils contiennent, comme changer leur luminosité. Dans ce guide étape par étape, nous allons vous montrer comment régler la luminosité d'une image DICOM à l'aide d'Aspose.Imaging pour .NET.

## Conditions préalables

Avant de plonger dans le processus étape par étape, assurez-vous que les conditions préalables suivantes sont remplies :

-  Aspose.Imaging pour .NET : vous devriez avoir installé cette puissante bibliothèque. Sinon, vous pouvez le télécharger depuis le[site web](https://releases.aspose.com/imaging/net/).

- Votre répertoire de documents : assurez-vous d'avoir configuré un répertoire dans lequel vous pouvez stocker vos fichiers image DICOM.

Maintenant que nous avons couvert les conditions préalables, passons aux étapes permettant d'ajuster la luminosité d'une image DICOM.

## Importer des espaces de noms

Dans votre projet C#, vous devez importer les espaces de noms nécessaires pour travailler avec Aspose.Imaging. Incluez les espaces de noms suivants en haut de votre fichier de code :

```csharp
using System;
using System.IO;
using Aspose.Imaging.FileFormats.Dicom;
using Aspose.Imaging.ImageOptions;
```

## Étape 1 : initialiser DicomImage

 Tout d'abord, vous devrez initialiser le`DicomImage` classe en chargeant votre fichier image DICOM. Voici comment procéder :

```csharp
// Le chemin d'accès au répertoire des documents.
string dataDir = "Your Document Directory";
using (var fileStream = new FileStream(dataDir + "file.dcm", FileMode.Open, FileAccess.Read))
using (DicomImage image = new DicomImage(fileStream))
{
    // Votre code ira ici
}
```

 Dans le code ci-dessus, remplacez`"Your Document Directory"` avec le chemin réel vers votre répertoire de documents et`"file.dcm"` avec le nom de votre fichier DICOM.

## Étape 2 : Ajustez la luminosité

 À l'intérieur de`using`bloc, vous pouvez maintenant régler la luminosité de l’image DICOM. Dans cet exemple, nous augmentons la luminosité de 50 unités, mais vous pouvez ajuster cette valeur selon vos besoins :

```csharp
// Ajuster la luminosité
image.AdjustBrightness(50);
```

Cette étape garantit que la luminosité de votre image DICOM est modifiée selon vos besoins.

## Étape 3 : Enregistrez l'image résultante

 Une fois que vous avez ajusté la luminosité, il est essentiel de sauvegarder l'image modifiée. Pour ce faire, créez une instance de`BmpOptions` pour l'image résultante et enregistrez-la sous forme de fichier BMP :

```csharp
// Créez une instance de BmpOptions pour l'image résultante et enregistrez l'image résultante
image.Save(dataDir + "AdjustBrightnessDICOM_out.bmp", new BmpOptions());
```

 Assurez-vous de remplacer`"AdjustBrightnessDICOM_out.bmp"` avec le nom et l'emplacement du fichier de sortie souhaité.

## Conclusion

Dans ce didacticiel, nous avons montré comment ajuster la luminosité d'une image DICOM à l'aide d'Aspose.Imaging pour .NET. Cette bibliothèque simplifie le processus de travail avec les données d'imagerie médicale, facilitant ainsi l'amélioration et la modification des images à diverses fins médicales.

En explorant les capacités d'Aspose.Imaging, vous constaterez qu'il s'agit d'un outil précieux dans votre flux de travail d'imagerie médicale. N'hésitez pas à expérimenter différentes valeurs de luminosité pour obtenir les résultats souhaités. Grâce à ces connaissances, vous pouvez gérer et améliorer efficacement les images DICOM dans vos projets médicaux.

## FAQ

### Q1 : Aspose.Imaging for .NET convient-il aux professionnels du domaine de l’imagerie médicale ?

A1 : Oui, Aspose.Imaging est une bibliothèque polyvalente utilisée par les professionnels du domaine de l'imagerie médicale pour traiter, améliorer et gérer efficacement les fichiers DICOM.

### Q2 : Puis-je utiliser Aspose.Imaging à des fins personnelles et commerciales ?

 A2 : Aspose.Imaging propose des options de licence pour un usage personnel et commercial. Vous pouvez explorer ces options sur le[page d'achat](https://purchase.aspose.com/buy).

### Q3 : Existe-t-il une version d'essai disponible pour Aspose.Imaging pour .NET ?

 A3 : Oui, vous pouvez télécharger une version d'essai gratuite d'Aspose.Imaging à partir de[ici](https://releases.aspose.com/).

### Q4 : Où puis-je trouver une assistance ou une assistance supplémentaire avec Aspose.Imaging ?

A4 : Vous pouvez obtenir de l'aide et vous connecter avec la communauté Aspose.Imaging sur le[Forums Aspose](https://forum.aspose.com/).

### Q5 : Quelles autres fonctionnalités de manipulation d’images Aspose.Imaging propose-t-il ?

A5 : Aspose.Imaging offre un large éventail de fonctionnalités pour la manipulation d'images, notamment le redimensionnement, le recadrage, la rotation et diverses options de filtrage, ce qui en fait une solution complète pour travailler avec des images médicales.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
