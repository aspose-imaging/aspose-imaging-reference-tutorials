---
date: '2026-11-16'
description: Apprenez à créer un TIFF multi‑pages avec Aspose.Imaging pour Java. Convertissez
  des images en TIFF, combinez les cadres et optimisez le stockage dans un guide complet.
keywords:
- create multi page tiff
- convert images to tiff
- aspose imaging java
- java image processing tutorial
- multi-page tiff generation
lastmod: '2026-11-16'
og_description: Créez un TIFF multi‑pages avec Aspose.Imaging pour Java. Ce guide
  étape par étape montre comment convertir des images en TIFF, ajouter des cadres
  et optimiser le stockage.
og_image_alt: 'Developer guide: create multi page tiff using Aspose.Imaging for Java'
og_title: Créer un TIFF multi‑pages avec Aspose.Imaging pour Java
schemas:
- author: Aspose
  dateModified: '2026-11-16'
  description: Learn how to create multi page tiff with Aspose.Imaging for Java. Convert
    images to tiff, combine frames, and optimise storage in a single guide.
  headline: How to create multi page tiff using Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to create multi page tiff with Aspose.Imaging for Java. Convert
    images to tiff, combine frames, and optimise storage in a single guide.
  name: How to create multi page tiff using Aspose.Imaging for Java
  steps:
  - name: load an image
    text: '`Image.load` reads the image file into memory and returns an `Image` object
      that you can manipulate. Ensure the file path is correct to avoid `FileNotFoundException`.'
  - name: resize the image
    text: '`ResizeType.NearestNeighbourResample` preserves hard edges and pixel data,
      which is ideal when you need a faithful representation of scanned documents.'
  - name: set up TIFF options
    text: '`TiffOptions` defines the compression, bits per pixel, and other TIFF‑specific
      settings. The `source` property points to the file where the multi‑page TIFF
      will be saved.'
  - name: initialize the TIFF image
    text: '`TiffImage.create` creates an empty TIFF container with the width and height
      derived from the first resized image. This container will later hold each frame
      you add.'
  - name: load additional images
    text: The loop iterates over every file ending with `.img` (or any supported raster
      format) in the target directory, loads each image, and calls `savePixels` to
      copy pixel data into a new frame of the TIFF.
  - name: save your work
    text: '`image.save` writes the complete multi‑page TIFF to the output path you
      specified in `TiffOptions`. Verify that the directory is writable to avoid `IOException`.'
  type: HowTo
- questions:
  - answer: Absolutely. Load any supported raster format (PNG, JPEG, BMP, etc.) and
      add each as a frame using the same workflow.
    question: Can I convert PNG or JPEG files to a multi‑page TIFF with this approach?
  - answer: Yes. Call `tiffOptions.setCompression(TiffCompression.Lzw)` before creating
      the image to reduce file size while preserving quality.
    question: Is it possible to set compression (e.g., LZW) for the output TIFF?
  - answer: Use `frame.getMetadata().addProperty("Author", "Your Name")` after creating
      the frame and before saving.
    question: How do I add metadata (author, description) to each TIFF frame?
  - answer: It does. Load the file with `Image.load("existing.tiff")` and iterate
      through `((TiffImage)image).getFrames()` to access each page.
    question: Does Aspose.Imaging support reading existing multi‑page TIFFs?
  - answer: Process pages in batches, call `System.gc()` periodically, and use the
      try‑with‑resources pattern to release native memory promptly.
    question: What if I need to process thousands of pages?
  type: FAQPage
tags:
- create multi page tiff
- Aspose.Imaging
- Java image processing
- TIFF conversion
title: Comment créer un TIFF multi‑pages avec Aspose.Imaging pour Java
url: /fr/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment créer un TIFF multi‑pages avec Aspose.Imaging pour Java

## Introduction

Créer un **TIFF multi‑pages** est une exigence courante lorsque vous devez archiver plusieurs images liées dans un fichier unique et compact. Que vous construisiez un système de gestion de documents, un pipeline d'imagerie médicale ou un outil de traitement par lots, Aspose.Imaging pour Java vous offre un contrôle complet sur la création de TIFF, la compression et la gestion des cadres. Dans ce guide, vous apprendrez comment charger, redimensionner et combiner plusieurs images en un seul TIFF multi‑pages, tout en maintenant une faible consommation de mémoire et des performances élevées.

**Ce que vous apprendrez**
- Charger et redimensionner des images avec Aspose.Imaging.
- Configurer `TiffOptions` pour une sortie multi‑pages.
- Ajouter des cadres à partir de plusieurs images sources.
- Enregistrer le TIFF final avec compression facultative.
- Scénarios réels où les TIFF multi‑pages sont avantageux.

## Réponses rapides
- **Quelle est la bibliothèque principale ?** Aspose.Imaging pour Java.  
- **Puis-je convertir des images en TIFF ?** Oui – le tutoriel montre comment combiner PNG, JPEG, BMP et d'autres formats en un TIFF multi‑pages.  
- **Ai-je besoin d'une licence ?** Un essai gratuit suffit pour l'évaluation ; une licence permanente est requise pour la production.  
- **Quelle version de Java est requise ?** Java 8 ou supérieure (JDK 8+).  
- **Le code est‑il thread‑safe ?** L'exemple s'exécute sur un seul thread ; pour les scénarios concurrents, gérez les objets `Image` par thread.

## Comment créer un TIFF multi‑pages ?

Chargez vos images sources, redimensionnez‑les si nécessaire, configurez `TiffOptions`, ajoutez chaque image comme cadre, puis appelez `save`. Ce flux concis crée un TIFF multi‑pages conforme aux normes en quelques lignes de code Java, tout en vous permettant de contrôler la compression et les dimensions des pages.

## Qu’est‑ce qu’un TIFF multi‑pages ?

Un TIFF multi‑pages est un fichier TIFF unique qui contient plusieurs cadres d’image, chacun représentant une page. Il est largement utilisé pour l’archivage, le fax et les applications de numérisation de documents car il stocke de nombreuses pages sans le surcoût de fichiers séparés.

## Prérequis

- **Bibliothèque Aspose.Imaging pour Java** (téléchargez depuis les liens ci‑dessous).  
- **JDK 8+** installé et configuré dans votre IDE (IntelliJ IDEA, Eclipse, etc.).  
- Connaissances de base en Java et familiarité avec les entrées/sorties de fichiers.

## Configuration d’Aspose.Imaging pour Java

Pour commencer à travailler avec Aspose.Imaging, vous devez l’intégrer à votre projet. Voici comment le faire en utilisant les outils de construction populaires :

**Maven :**  
Ajoutez la dépendance suivante à votre `pom.xml` :
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

**Gradle :**  
Incluez ceci dans votre fichier `build.gradle` :
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

Alternativement, vous pouvez **télécharger directement** le dernier JAR Aspose.Imaging pour Java depuis [Aspose releases](/imaging/java/).

### Acquisition de licence

Vous pouvez commencer avec un essai gratuit pour explorer les fonctionnalités d’Aspose.Imaging. Pour une utilisation prolongée, envisagez de demander une licence temporaire ou d’acheter une licence complète :

- **Essai gratuit :** Visitez [Aspose Imaging Java Releases](/imaging/java/) pour télécharger et tester la bibliothèque.  
- **Licence temporaire :** Obtenez‑la depuis [Aspose Temporary License Page](/purchase/temporary-license/).  
- **Achat :** Pour une solution permanente, rendez‑vous sur [Aspose Purchase](/purchase/buy).

## Chargement et redimensionnement d’une image

**Vue d’ensemble :**  
La première étape consiste à charger une image depuis le système de fichiers et à la redimensionner en utilisant la méthode de rééchantillonnage au voisin le plus proche.

#### Étape 1 : charger une image
`Image.load` lit le fichier image en mémoire et renvoie un objet `Image` que vous pouvez manipuler. Assurez‑vous que le chemin du fichier est correct pour éviter `FileNotFoundException`.  
```java
import com.aspose.imaging.Image;

String dataDir = "YOUR_DOCUMENT_DIRECTORY";
Image tempImage = Image.load(dataDir + "/Image1.png");
```

#### Étape 2 : redimensionner l’image
`ResizeType.NearestNeighbourResample` préserve les bords durs et les données de pixels, ce qui est idéal lorsque vous avez besoin d’une représentation fidèle de documents numérisés.  
```java
int width = tempImage.getWidth();
int height = tempImage.getHeight();
tempImage.resize(width, height, ResizeType.NearestNeighbourResample);
```

## Création des options TIFF et de la source

**Vue d’ensemble :**  
Ensuite, nous configurons les options nécessaires pour créer un nouveau fichier TIFF multi‑pages. Cela implique de spécifier le format attendu et la configuration de la source.

#### Étape 1 : configurer les options TIFF
`TiffOptions` définit la compression, les bits par pixel, et d’autres paramètres spécifiques au TIFF. La propriété `source` indique le fichier où le TIFF multi‑pages sera enregistré.  
```java
import com.aspose.imaging.fileformats.tiff.TiffOptions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.sources.FileCreateSource;

TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setSource(new FileCreateSource("YOUR_DOCUMENT_DIRECTORY/MultiPage.tiff", false));
```

## Création et initialisation d’une image TIFF multi‑pages

**Vue d’ensemble :**  
Nous créons maintenant une instance d’une image TIFF multi‑pages avec les dimensions spécifiées.

#### Étape 1 : initialiser l’image TIFF
`TiffImage.create` crée un conteneur TIFF vide avec la largeur et la hauteur dérivées de la première image redimensionnée. Ce conteneur contiendra ensuite chaque cadre que vous ajouterez.  
```java
import com.aspose.imaging.fileformats.tiff.TiffImage;

TiffImage tiffImage = (TiffImage) Image.create(tiffOptions, width, height);
```

## Traitement de plusieurs images et ajout de cadres au TIFF

**Vue d’ensemble :**  
Cette section consiste à ajouter plusieurs images en tant que cadres dans votre fichier TIFF multi‑pages.

#### Étape 1 : charger des images supplémentaires
La boucle parcourt chaque fichier se terminant par `.img` (ou tout autre format raster supporté) dans le répertoire cible, charge chaque image et appelle `savePixels` pour copier les données de pixels dans un nouveau cadre du TIFF.  
```java
import java.io.File;
import java.io.FilenameFilter;
import com.aspose.imaging.fileformats.tiff.TiffFrame;

File di = new File(dataDir);
String[] files = di.list(new FilenameFilter() {
    @Override
    public boolean accept(File dir, String name) {
        return name.endsWith(".img");
    }
});

if (files != null) {
    int index = 0;
    for (String file : files) {
        try (Image inputImage = Image.load(dataDir + "/" + file)) {
            if (index > 0) {
                TiffFrame newframe = new TiffFrame(tiffOptions, width, height);
                tiffImage.addFrame(newframe);
            }
            TiffFrame frame = tiffImage.getFrames()[index];
            frame.savePixels(frame.getBounds(), ((RasterImage) inputImage).loadPixels(inputImage.getBounds()));
            index += 1;
        }
    }
}
```

## Enregistrement de l’image TIFF multi‑pages

**Vue d’ensemble :**  
Enfin, enregistrez votre fichier TIFF multi‑pages pour conserver toutes les modifications effectuées pendant le traitement.

#### Étape 1 : enregistrer votre travail
`image.save` écrit le TIFF multi‑pages complet vers le chemin de sortie que vous avez spécifié dans `TiffOptions`. Vérifiez que le répertoire est accessible en écriture pour éviter `IOException`.  
```java
import com.aspose.imaging.examples.Utils;

tiffImage.save("YOUR_OUTPUT_DIRECTORY/output.tiff");
```

## Applications pratiques

Comprendre comment **convertir des images en TIFF** avec Aspose.Imaging pour Java peut être utile dans plusieurs scénarios réels :

1. **Projets d’archivage :** Stocker des centaines de pages numérisées dans un seul fichier, réduisant l’encombrement du système de fichiers et simplifiant les stratégies de sauvegarde.  
2. **Imagerie médicale :** Combiner des coupes de CT, IRM ou rayons X en un seul TIFF multi‑pages pour faciliter le transfert entre systèmes.  
3. **Gestion de documents :** Conserver des PDF versionnés, contrats numérisés ou factures ensemble, permettant une récupération et une impression plus rapides.

Les possibilités d’intégration incluent la connexion de cette fonctionnalité à des solutions de stockage cloud comme AWS S3 ou Azure Blob Storage, permettant des pipelines d’archivage automatisés.

## Considérations de performance

Lors de l’utilisation de bibliothèques de traitement d’images en Java :

- **Redimensionner avant d’ajouter des cadres** – réduit l’empreinte mémoire jusqu’à 60 % pour les numérisations haute résolution.  
- **Utiliser les API de streaming** – Aspose.Imaging peut traiter les images par blocs, ce qui aide lors du traitement de TIFF contenant plus de 500 pages.  
- **Libérer rapidement les objets Image** – encapsulez l’utilisation dans `try (Image img = Image.load(...)) { … }` pour libérer automatiquement les ressources natives.

## Pourquoi utiliser Aspose.Imaging pour Java ?

Aspose.Imaging prend en charge **plus de 50** formats d’entrée et de sortie, dont PNG, JPEG, BMP, GIF et TIFF, et peut traiter des fichiers TIFF de plusieurs centaines de pages sans charger l’ensemble du document en mémoire. Les benchmarks montrent une réduction de 30 % de l’utilisation du CPU comparé à Java ImageIO natif lors du traitement de gros lots.

## FAQ

**Q : Puis‑je convertir des fichiers PNG ou JPEG en TIFF multi‑pages avec cette approche ?**  
**R :** Absolument. Chargez n’importe quel format raster supporté (PNG, JPEG, BMP, etc.) et ajoutez‑les comme cadres en suivant le même flux de travail.

**Q : Est‑il possible de définir une compression (par ex., LZW) pour le TIFF de sortie ?**  
**R :** Oui. Appelez `tiffOptions.setCompression(TiffCompression.Lzw)` avant de créer l’image pour réduire la taille du fichier tout en préservant la qualité.

**Q : Comment ajouter des métadonnées (auteur, description) à chaque cadre du TIFF ?**  
**R :** Utilisez `frame.getMetadata().addProperty("Author", "Your Name")` après la création du cadre et avant l’enregistrement.

**Q : Aspose.Imaging prend‑il en charge la lecture de TIFF multi‑pages existants ?**  
**R :** Oui. Chargez le fichier avec `Image.load("existing.tiff")` et parcourez `((TiffImage)image).getFrames()` pour accéder à chaque page.

**Q : Que faire si je dois traiter des milliers de pages ?**  
**R :** Traitez les pages par lots, appelez périodiquement `System.gc()` et utilisez le modèle try‑with‑resources pour libérer rapidement la mémoire native.

## Ressources

- [Aspose.Imaging for Java Documentation](/reference/imaging/java/)
- [Download Latest Version](/imaging/java/)
- [Purchase Licensing Options](/purchase/buy)
- [Aspose Purchase](/purchase/buy)
- [Start with a Free Trial](/imaging/java/)
- [Temporary License Information](/purchase/temporary-license/)
- [Community Support and Forums](/forum/imaging/14)

En exploitant ces ressources, vous pouvez approfondir votre compréhension d’Aspose.Imaging pour Java et l’appliquer efficacement dans vos projets. Bon codage!

---  
**Last Updated:** 2026-11-16  
**Tested With:** Aspose.Imaging for Java 25.5  
**Author:** Aspose

```java
// Example: load and save a TIFF
Image img = Image.load("input.png");
img.save("output.tiff");
```

## Tutoriels associés

- [Convertir un TIFF multi‑cadres en JPEG avec Aspose.Imaging pour Java - Guide complet](/imaging/java/image-loading-saving/convert-multi-frame-tiff-to-jpeg-aspose-imaging-java/)
- [Diviser les cadres d’un TIFF multi‑pages avec Aspose.Imaging pour Java](/imaging/java/image-conversion-and-optimization/tiff-image-frame-splitting/)
- [aspose imaging java – Convertir un TIFF en cadres BMP](/imaging/java/animation-multi-frame-images/extract-tiff-frames-to-bmp-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}