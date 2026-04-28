---
date: 2026-04-28
description: Apprenez comment convertir le TIFF en PNG et comment convertir le TIFF
  en d’autres formats raster en utilisant Aspose.Imaging pour Java. Guide étape par
  étape pour la manipulation d’images.
keywords:
- tiff to png java
- how to convert tiff
- Aspose.Imaging Java
linktitle: Enregistrement de trames dans différents formats raster
second_title: Aspose.Imaging Java Image Processing API
title: tiff to png java – Convertir TIFF en PNG et enregistrer les images dans différents
  formats raster
url: /fr/java/document-conversion-and-processing/frame-saving-in-different-raster-formats/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# tiff to png java – Convertir TIFF en PNG et enregistrer les images dans différents formats raster

Travailler avec des fichiers TIFF multi‑pages est un scénario courant dans les applications axées sur les documents. Si vous devez **convertir tiff en png**—ou extraire des images individuelles et les stocker dans d’autres formats raster—Aspose.Imaging for Java rend le processus simple et performant. Dans ce tutoriel, nous parcourrons les étapes exactes pour charger un TIFF, itérer sur ses images, et enregistrer chacune d’elles au format PNG (vous pouvez facilement passer à BMP ou GIF plus tard). À la fin, vous verrez également comment **convertir tiff** vers n’importe lequel des formats raster pris en charge avec seulement quelques lignes de code.

## Réponses rapides
- **Que signifie « convertir tiff en png » ?** Cela signifie extraire chaque page d’un fichier TIFF et l’enregistrer sous forme d’image raster PNG.  
- **Quelle bibliothèque gère cela ?** Aspose.Imaging for Java offre une prise en charge complète de l’extraction des images TIFF et de la conversion de formats raster.  
- **Ai‑je besoin d’une licence ?** Un essai gratuit suffit pour le développement ; une licence complète est requise pour une utilisation en production.  
- **Puis‑je enregistrer en BMP ou GIF au lieu de PNG ?** Oui—il suffit de remplacer `PngOptions` par `BmpOptions` ou `GifOptions`.  
- **Quelle version de Java est requise ?** Java 8 ou supérieur est recommandé.

## Qu’est‑ce que « convertir tiff en png » ?
Convertir un TIFF en PNG consiste à décoder le TIFF multi‑pages, accéder à chaque image, puis encoder cette image au format PNG, qui est sans perte, adapté au web et largement supporté.

## Pourquoi utiliser Aspose.Imaging pour Java ?
- **Prise en charge étendue des formats** – Gère TIFF, PNG, JPEG, BMP, GIF, et bien d’autres.  
- **Aucune dépendance native** – Pure Java, facile à intégrer dans tout projet JVM.  
- **Haute performance** – Optimisé pour les images volumineuses et les documents multi‑pages.  
- **API simple** – Code minimal requis pour effectuer des conversions complexes.

## Pourquoi cela importe
De nombreux systèmes hérités stockent les documents numérisés sous forme de TIFF multi‑pages car le format est adapté à l’archivage. Cependant, les applications web et mobiles modernes préfèrent PNG, BMP ou GIF pour un rendu rapide et la génération de miniatures. Convertir les images TIFF à la volée réduit les coûts de stockage, améliore les temps de chargement et élargit la compatibilité entre navigateurs et appareils.

## Prérequis
1. **Environnement de développement Java** – Assurez‑vous que le JDK est installé. Téléchargez‑le depuis le [site Oracle](https://www.oracle.com/java/technologies/javase-downloads) si ce n’est pas déjà fait.  
2. **Bibliothèque Aspose.Imaging pour Java** – Accédez à la référence API dans la [documentation](https://reference.aspose.com/imaging/java/). Obtenez la bibliothèque depuis la [page de téléchargement](https://releases.aspose.com/imaging/java/). Un essai gratuit est disponible [ici](https://releases.aspose.com/), et une licence complète peut être achetée [ici](https://purchase.aspose.com/buy).  
3. **Image TIFF d’exemple** – Disposez d’un TIFF multi‑pages prêt à être traité.

Maintenant que les prérequis sont couverts, plongeons dans le code.

## Comment convertir un TIFF en PNG avec Aspose.Imaging pour Java

### Importer les packages
Tout d’abord, importez les classes Aspose.Imaging requises.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.imageoptions.PngOptions;
import com.aspose.imaging.fileformats.tiff.TiffImage;
import com.aspose.imaging.fileformats.tiff.TiffFrame;
```

### Étape 1 : Charger l’image TIFF
Initialisez le répertoire de données et chargez le fichier TIFF source.

```java
String dataDir = "Your Document Directory" + "ModifyingImages/";
try (TiffImage multiImage = (TiffImage) Image.load(dataDir + "SampleTiff1.tiff")) {
```

### Étape 2 : Enregistrer les images dans différents formats raster
Itérez sur chaque image et **enregistrez l’image en png**. Pour **convertir tiff en bmp** ou réaliser une **conversion tiff en gif**, remplacez simplement `PngOptions` par `BmpOptions` ou `GifOptions`.

```java
    int i = 0;
    for (TiffFrame tiffFrame : multiImage.getFrames()) {
        tiffFrame.save("Your Document Directory" + i + "_out.png", new PngOptions());
        i++;
    }
}
```

> **Astuce :** Conservez le bloc `try‑with‑resources` tel qu’il est affiché pour garantir que le fichier TIFF soit correctement libéré après le traitement.

## Cas d’utilisation courants
- **Document archiving:** Convertir les documents TIFF numérisés en PNG pour un aperçu web.  
- **Thumbnail generation:** Extraire la première image d’un TIFF et l’enregistrer comme petite vignette PNG.  
- **Format migration:** Migrer les actifs TIFF hérités vers des formats modernes comme BMP ou GIF pour une compatibilité avec les anciens systèmes.

## Dépannage et astuces
- **Missing frames:** Vérifiez que le TIFF source contient réellement plusieurs pages ; utilisez `multiImage.getFrames().size()` pour déboguer.  
- **Out‑of‑memory errors:** Erreurs de mémoire insuffisante : traitez les gros TIFF page par page comme indiqué plutôt que de charger le fichier complet en mémoire.  
- **Quality control:** Contrôle de la qualité : PNG est sans perte ; si vous avez besoin de fichiers plus petits, envisagez d’utiliser les options JPEG avec des réglages de qualité.

## Questions fréquemment posées

**Q1 : Quels sont les formats raster pris en charge pour l’enregistrement des images dans Aspose.Imaging pour Java ?**  
A1 : Aspose.Imaging pour Java prend en charge un large éventail de formats raster, dont PNG, JPEG, BMP, GIF, et plus encore. Vous pouvez choisir le format qui convient le mieux aux besoins de votre application.

**Q2 : Puis‑je effectuer d’autres opérations d’image avec Aspose.Imaging pour Java ?**  
A2 : Oui, Aspose.Imaging pour Java propose un ensemble complet de fonctionnalités pour la manipulation d’images, incluant le redimensionnement, le recadrage et l’application de divers filtres et effets. C’est un outil polyvalent pour tous vos besoins de traitement d’image.

**Q3 : Comment obtenir une licence complète pour Aspose.Imaging pour Java ?**  
A : Pour acheter une licence complète pour Aspose.Imaging pour Java, consultez la [page d’achat](https://purchase.aspose.com/buy). Vous y trouverez différentes options de licence adaptées à votre projet.

**Q4 : Une version d’essai gratuite est‑elle disponible pour Aspose.Imaging pour Java ?**  
A : Oui, vous pouvez accéder à une version d’essai gratuite d’Aspose.Imaging pour Java depuis la [page des releases](https://releases.aspose.com/). Cette version d’essai vous permet d’explorer les capacités de la bibliothèque avant d’effectuer un achat.

**Q5 : Où puis‑je obtenir du support ou de l’assistance pour Aspose.Imaging pour Java ?**  
A : Pour toute question, problème ou assistance concernant Aspose.Imaging pour Java, vous pouvez consulter le [forum Aspose Imaging](https://forum.aspose.com/). La communauté et l’équipe de support sont là pour vous aider.

---

**Dernière mise à jour :** 2026-04-28  
**Testé avec :** Aspose.Imaging for Java 24.11  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}