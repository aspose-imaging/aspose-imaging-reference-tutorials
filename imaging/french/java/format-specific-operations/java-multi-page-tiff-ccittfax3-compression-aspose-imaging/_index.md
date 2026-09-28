---
date: '2026-09-28'
description: Apprenez à utiliser la compression ccittfax3 java pour créer des fichiers
  TIFF multipage avec Aspose.Imaging. Numérisez, archivez et réduisez efficacement
  la taille des fichiers pour les flux de travail de documents.
keywords:
- ccittfax3 compression java
- multi-page tiff java
- aspose imaging tutorial
- java image processing
- document archiving tiff
lastmod: '2026-09-28'
og_description: Découvrez étape par étape comment utiliser la compression ccittfax3
  java avec Aspose.Imaging pour créer des fichiers TIFF multipage efficaces pour la
  numérisation et l'archivage.
og_image_alt: Guide showing Java code that creates a multi-page TIFF using CCITTFAX3
  compression
og_title: Comment créer un TIFF multipage avec la compression ccittfax3 en Java
schemas:
- author: Aspose
  dateModified: '2026-09-28'
  description: Learn how to use ccittfax3 compression java to create multi-page TIFF
    files with Aspose.Imaging. Efficiently scan, archive, and reduce file size for
    document workflows.
  headline: How to create multi-page TIFF with ccittfax3 compression java
  type: TechArticle
- questions:
  - answer: CCITTFAX3 is limited to monochrome data; for color use JPEG or LZW compression
      instead.
    question: Can I use this approach with color images?
  - answer: Yes—the library writes each frame directly to the output stream, keeping
      memory usage low even for thousands of pages.
    question: Does Aspose.Imaging support streaming for huge TIFFs?
  - answer: Load the `.lic` file with `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.
    question: How do I apply a temporary license programmatically?
  - answer: You can render each `TiffFrame` to a `BufferedImage` and display it in
      a Swing component.
    question: Is there a way to preview the TIFF before saving?
  - answer: Aspose.Imaging supports Java 8 through Java 21, including LTS releases.
    question: Which Java versions are officially supported?
  type: FAQPage
tags:
- ccittfax3 compression
- Aspose.Imaging
- Java TIFF
- image compression
- document scanning
title: Comment créer un TIFF multipage avec la compression ccittfax3 en Java
url: /fr/java/format-specific-operations/java-multi-page-tiff-ccittfax3-compression-aspose-imaging/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Maîtriser la création de TIFF multi-pages avec la compression ccittfax3 java en utilisant Aspose.Imaging

## Introduction

Si vous devez archiver de gros volumes de documents numérisés tout en maintenant la taille des fichiers faible, **ccittfax3 compression java** est la solution idéale. Ce tutoriel vous montre comment générer des fichiers TIFF multi‑pages avec la compression CCITTFAX3 en Java en utilisant Aspose.Imaging. Vous apprendrez pourquoi cette compression fonctionne si bien pour les numérisations monochromes, comment configurer la bibliothèque, et comment ajouter chaque page en tant que trame.

**Ce que vous apprendrez**
- Comment ajouter Aspose.Imaging à un projet Java.
- Comment configurer `TiffOptions` pour la compression CCITTFAX3.
- Comment créer un `TiffImage`, redimensionner les images sources et les ajouter en tant que trames.
- Comment enregistrer efficacement le TIFF multi‑pages final.

Parcourons l'implémentation complète.

## Réponses rapides
- **Quel est le principal avantage de la compression CCITTFAX3 ?** Jusqu'à 80 % de réduction de la taille du fichier pour les numérisations noir‑et‑blanc.  
- **Quelle bibliothèque fournit un support intégré ?** Aspose.Imaging pour Java, version 25.5+.  
- **Ai‑je besoin d'une licence pour le développement ?** Une licence d'essai gratuite fonctionne pour toutes les fonctionnalités ; une licence payante est requise pour la production.  
- **Puis‑je traiter des centaines de pages ?** Oui—Aspose.Imaging diffuse les pages, de sorte que l'utilisation de la mémoire reste faible.  
- **Le code est‑il compatible avec Java 11 et ultérieur ?** Absolument ; l'API cible Java 8+.

## Qu'est-ce que la compression ccittfax3 java ?
`CCITTFAX3` est un algorithme de compression sans perte, monochrome, conçu pour les fax et les images de documents numérisés. Il encode chaque pixel sur un seul bit, offrant une sortie de haute qualité tout en réduisant considérablement la taille du fichier—souvent de 70‑80 % par rapport à un TIFF non compressé. Cela le rend idéal pour l'archivage de documents noir‑et‑blanc où la fidélité doit être préservée.

## Pourquoi utiliser Aspose.Imaging pour cette tâche ?
Aspose.Imaging prend en charge **plus de 100** formats d'entrée et de sortie, y compris PDF, PNG, JPEG et TIFF. Son architecture de diffusion peut gérer des fichiers TIFF **multi‑centaines‑de‑pages** sans charger le document entier en mémoire, ce qui le rend idéal pour les projets d'archivage à grande échelle.

## Prérequis

- **Java Development Kit (JDK)** 8 ou plus récent installé.
- **IDE** tel qu'IntelliJ IDEA ou Eclipse.
- **Maven** ou **Gradle** pour la gestion des dépendances.
- Connaissances de base en Java (classes, objets, collections).

## Configuration d'Aspose.Imaging pour Java

Ajoutez la bibliothèque à votre fichier de construction.

**Maven:**  
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```  

**Gradle:**  
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```  

### Téléchargement direct

Vous pouvez également télécharger le JAR le plus récent depuis [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

### Acquisition de licence

Une licence d'essai gratuite est disponible depuis [Aspose's Free Trial page](https://releases.aspose.com/imaging/java/). Pour une utilisation en production, achetez une licence permanente ou demandez une licence temporaire sur [Aspose Purchase](https://purchase.aspose.com/temporary-license/).

Pour une utilisation détaillée de l'API, consultez la [documentation](https://reference.aspose.com/imaging/java/) d'Aspose.Imaging pour Java.

### Initialisation de base

Après avoir ajouté la dépendance, initialisez la bibliothèque comme indiqué ci‑dessous.

```java
import com.aspose.imaging.License;

License license = new License();
license.setLicense("path_to_your_license.lic");
```  

## Comment configurer la compression ccittfax3 java pour un TIFF multi‑pages ?

`TiffOptions` est une classe qui définit le format de sortie et les paramètres de compression d'un fichier TIFF. Chargez l'objet `TiffOptions` avec l'énumération `CCITTGroup3FaxCompression`, puis définissez la source du fichier de sortie. Cette configuration en deux étapes prépare l'écrivain pour la compression monochrome et garantit que chaque page ajoutée ultérieurement sera encodée avec l'algorithme CCITTFAX3, entraînant une réduction significative de la taille tout en préservant la qualité de l'image.

```java
    import com.aspose.imaging.fileformats.tiff.TiffExpectedFormat;
    import com.aspose.imaging.imageoptions.TiffOptions;
    import com.aspose.imaging.sources.FileCreateSource;

    TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.TiffCcittFax3);
    ```  

```java
    // Replace "YOUR_OUTPUT_DIRECTORY" with your actual directory path
    outputSettings.setSource(new FileCreateSource("YOUR_OUTPUT_DIRECTORY/output.tiff", false));
    ```  

## Comment créer une instance TiffImage en Java ?

`TiffImage` représente un document TIFF multi‑pages en mémoire et fournit des méthodes pour manipuler ses trames. Commencez par définir la largeur et la hauteur communes à toutes les pages. Ensuite, créez une instance `TiffImage` en utilisant les `TiffOptions` précédemment créées. L'objet `TiffImage` agit comme un conteneur pour les trames individuelles, vous permettant d'ajouter, de supprimer ou de réorganiser les pages avant d'enregistrer le fichier final.

```java
    final int newWidth = 500;
    final int newHeight = 500;
    ```  

```java
    import com.aspose.imaging.Image;
    import com.aspose.imaging.fileformats.tiff.TiffImage;

    TiffImage tiffImage = (TiffImage) Image.create(outputSettings, newWidth, newHeight);
    ```  

## Comment charger et redimensionner les images sources depuis un dossier ?

Filtrez le répertoire cible pour les fichiers JPEG, lisez chaque image et redimensionnez‑la pour qu'elle corresponde à la toile du TIFF. Le redimensionnement avant l'ajout des trames réduit la consommation de mémoire et accélère l'opération d'enregistrement. En convertissant chaque image source aux dimensions et au format de pixel requis, vous garantissez une mise en page cohérente des pages et évitez les erreurs d'exécution lors de l'ajout des trames au document TIFF.

```java
    import java.io.File;
    import java.io.FilenameFilter;

    final File folder = new File("samples/");
    File[] files = folder.listFiles(new FilenameFilter() {
        public boolean accept(File dir, String name) {
            return name.toLowerCase().endsWith(".jpg");
        }
    });

    if (files == null) return;
    ```  

```java
    import com.aspose.imaging.RasterImage;
    import com.aspose.imaging.ResizeType;

    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);
    }
    ```  

## Comment ajouter chaque image en tant que trame au TIFF multi‑pages ?

`TiffFrame` est un objet qui contient une image de page unique et ses métadonnées associées dans un TIFF. Parcourez les images redimensionnées, créez une nouvelle `TiffFrame` et ajoutez‑la au `TiffImage`. Chaque trame devient une page distincte dans le document final, et la bibliothèque gère automatiquement les mises à jour de métadonnées nécessaires, telles que le nombre de pages et les décalages, assurant une structure TIFF multi‑pages valide.

```java
    import com.aspose.imaging.fileformats.tiff.TiffFrame;

    int index = 0;
    for (final File fileEntry : files) {
        RasterImage image = (RasterImage) Image.load(fileEntry.getAbsolutePath());
        image.resize(newWidth, newHeight, ResizeType.NearestNeighbourResample);

        TiffFrame frame = tiffImage.getActiveFrame();
        frame.savePixels(frame.getBounds(), image.loadPixels(image.getBounds()));

        if (index > 0) {
            frame = new TiffFrame(new TiffOptions(outputSettings), newWidth, newHeight);
            tiffImage.addFrame(frame);
        }
        index++;
    }
    ```  

## Comment enregistrer le fichier TIFF multi‑pages final ?

Appelez la méthode `save` sur l'instance `TiffImage`, en indiquant le chemin de sortie souhaité. La bibliothèque écrit automatiquement toutes les trames en utilisant la compression CCITTFAX3, diffuse les données vers le disque de manière efficace et ferme toutes les ressources sous‑jacentes. Après la fin de l'opération d'enregistrement, le fichier résultant contient toutes les pages avec la compression spécifiée, prêt à être distribué ou archivé.

```java
    try {
        tiffImage.save();
    } finally {
        tiffImage.close();
        outputSettings.close();
    }
    ```  

## Applications pratiques

- **Archivage de documents :** Stockez les contrats, factures ou dossiers juridiques numérisés avec un encombrement de stockage minimal.  
- **Imagerie médicale :** Compressez les scans radiologiques tout en préservant les détails diagnostiques.  
- **Production d'impression :** Générez des travaux d'impression multi‑pages que les imprimantes peuvent consommer directement.

## Considérations de performance

- Utilisez `ResizeOptions` qui préservent le ratio d'aspect pour éviter les distorsions.  
- Fermez chaque objet `Image` après avoir ajouté sa trame pour libérer la mémoire native.  
- Pour des lots très volumineux, traitez les fichiers en flux parallèles et écrivez chaque segment TIFF de façon asynchrone.

## Pièges courants et dépannage

- **Format de pixel incorrect :** CCITTFAX3 ne fonctionne qu'avec des images 1‑bit (noir‑et‑blanc). Convertissez les images couleur en niveaux de gris avant le redimensionnement.  
- **Fuites de mémoire :** Appelez toujours `dispose()` sur les objets `Image` temporaires ; sinon les tampons natifs restent alloués.  
- **Taille du fichier non réduite :** Assurez‑vous que la propriété de compression de `TiffOptions` est définie ; sinon la compression par défaut (aucune) est utilisée.

## Questions fréquemment posées

**Q : Puis‑je utiliser cette approche avec des images couleur ?**  
R : CCITTFAX3 est limité aux données monochromes ; pour la couleur, utilisez la compression JPEG ou LZW à la place.

**Q : Aspose.Imaging prend‑il en charge le streaming pour les TIFF énormes ?**  
R : Oui—la bibliothèque écrit chaque trame directement dans le flux de sortie, maintenant une faible utilisation de la mémoire même pour des milliers de pages.

**Q : Comment appliquer une licence temporaire par programme ?**  
R : Chargez le fichier `.lic` avec `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`.

**Q : Existe‑t‑il un moyen de prévisualiser le TIFF avant l'enregistrement ?**  
R : Vous pouvez rendre chaque `TiffFrame` en un `BufferedImage` et l'afficher dans un composant Swing.

**Q : Quelles versions de Java sont officiellement prises en charge ?**  
R : Aspose.Imaging prend en charge Java 8 à Java 21, y compris les versions LTS.

## Conclusion

Vous disposez maintenant d'un flux de travail complet et prêt pour la production afin de créer des fichiers TIFF multi‑pages avec **ccittfax3 compression java** en utilisant Aspose.Imaging. En suivant les étapes ci‑dessus, vous pouvez archiver efficacement d'importantes collections de documents tout en maintenant les coûts de stockage bas et la qualité d'image élevée. Explorez les fonctionnalités supplémentaires d'Aspose.Imaging—telles que l'OCR, la gestion des métadonnées et la conversion de formats—pour enrichir davantage votre pipeline de traitement de documents.

---

**Last Updated:** 2026-09-28  
**Tested With:** Aspose.Imaging 25.5 for Java  
**Author:** Aspose

## Tutoriels associés

- [Comment créer un TIFF multi‑pages avec Aspose.Imaging pour Java – Guide complet](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [Comment réduire la taille des fichiers image avec la compression LZW en Java](/imaging/java/compression-optimization/compress-tiff-images-aspose-imaging-java/)
- [Diviser les trames d'un TIFF multi‑pages avec Aspose.Imaging pour Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}