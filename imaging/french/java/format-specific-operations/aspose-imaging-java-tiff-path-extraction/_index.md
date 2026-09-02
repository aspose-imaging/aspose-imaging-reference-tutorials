---
date: '2026-09-02'
description: Apprenez à créer un clipping path et à l'extraire des images TIFF à l'aide
  d'Aspose.Imaging for Java. Suivez les instructions step‑by‑step pour convertir efficacement
  un TIFF en PSD.
keywords:
- create clipping path
- how to extract path
- how to convert tiff
- aspose imaging java
- convert tiff to psd
lastmod: '2026-09-02'
og_description: Apprenez à créer un clipping path et à l'extraire des images TIFF
  à l'aide d'Aspose.Imaging for Java. Suivez le code step‑by‑step pour convertir un
  TIFF en PSD.
og_image_alt: Guide showing how to create clipping path in TIFF using Aspose.Imaging
  Java
og_title: Créer un clipping path dans un TIFF avec Aspose.Imaging for Java
schemas:
- author: Aspose
  dateModified: '2026-09-02'
  description: Learn how to create clipping path and extract it from TIFF images using
    Aspose.Imaging for Java. Follow step‑by‑step instructions to convert TIFF to PSD
    efficiently.
  headline: Create clipping path in TIFF with Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to create clipping path and extract it from TIFF images using
    Aspose.Imaging for Java. Follow step‑by‑step instructions to convert TIFF to PSD
    efficiently.
  name: Create clipping path in TIFF with Aspose.Imaging for Java
  steps:
  - name: '**Free trial** – start with a 30‑day trial.'
    text: '**Free trial** – start with a 30‑day trial.'
  - name: '**Temporary license** – obtain one from the [temporary license page](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary license** – obtain one from the [temporary license page](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – buy a full license at [Aspose''s website](https://purchase.aspose.com/buy).'
    text: '**Purchase** – buy a full license at [Aspose''s website](https://purchase.aspose.com/buy).'
  - name: '**Graphic design workflows** – Convert TIFF to PSD to edit layers and masks
      in Photoshop.'
    text: '**Graphic design workflows** – Convert TIFF to PSD to edit layers and masks
      in Photoshop.'
  - name: '**Automated image pipelines** – Batch‑process thousands of TIFFs, extracting
      or adding paths on the fly.'
    text: '**Automated image pipelines** – Batch‑process thousands of TIFFs, extracting
      or adding paths on the fly.'
  - name: '**Data‑driven visualizations** – Use vector paths to generate precise charts
      or schematics from raster sources.'
    text: '**Data‑driven visualizations** – Use vector paths to generate precise charts
      or schematics from raster sources.'
  type: HowTo
- questions:
  - answer: Yes, provided you have a valid commercial license; a free trial is available
      for evaluation.
    question: Can I use Aspose.Imaging for Java in a commercial application?
  - answer: The library supports over 100 formats, including TIFF, PSD, BMP, JPEG,
      PNG, and many more.
    question: What image formats does Aspose.Imaging support?
  - answer: Verify that the source TIFF actually contains vector path resources; use
      the `hasPathResources()` check before extraction.
    question: How do I troubleshoot path extraction errors?
  - answer: Absolutely – combine the extraction code with Java’s parallel streams
      or an executor service to handle many files efficiently.
    question: Is batch processing of multiple TIFFs possible?
  - answer: Complex shapes may need manual adjustment after creation; the API handles
      standard Bezier curves and straight lines reliably.
    question: Are there limitations when creating clipping paths in TIFF?
  type: FAQPage
tags:
- create clipping path
- TIFF processing
- Aspose.Imaging
- Java image manipulation
- PSD conversion
title: Créer un clipping path dans un TIFF avec Aspose.Imaging for Java
url: /fr/java/format-specific-operations/aspose-imaging-java-tiff-path-extraction/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Créer un chemin de détourage dans un TIFF avec Aspose.Imaging pour Java

Dans ce guide complet, vous apprendrez **comment créer un chemin de détourage** dans un fichier TIFF et comment extraire les chemins existants en utilisant Aspose.Imaging pour Java. À la fin, vous pourrez convertir des images TIFF en fichiers PSD entièrement éditables, les rendant prêts pour Photoshop ou tout éditeur compatible vecteur.

## Réponses rapides
- **Qu'est‑ce qu'un chemin de détourage ?** Un contour vectoriel qui définit les zones transparentes et opaques d'une image.  
- **Puis‑je extraire un chemin existant d'un TIFF ?** Oui – Aspose.Imaging peut lire les ressources de chemin intégrées et les enregistrer en tant que PSD.  
- **Comment ajouter un nouveau chemin de détourage ?** Créez un `PathResource`, remplissez-le avec des enregistrements vectoriels et assignez‑le au cadre actif de l'image.  
- **Ai‑je besoin d'une licence pour une utilisation en production ?** Une licence valide d'Aspose.Imaging est requise pour les déploiements commerciaux.  
- **Quelle version de Java est requise ?** JDK 8 ou supérieur ; la bibliothèque fonctionne avec Java 11, 17 et les versions ultérieures.

## Qu'est‑ce qu'un chemin de détourage ?
Un chemin de détourage est un contour basé sur des vecteurs qui indique aux moteurs de rendu quelles parties d'une image afficher ou masquer. Il est stocké comme une ressource de chemin à l'intérieur des fichiers TIFF ou PSD et peut être édité dans Adobe Photoshop.

## Pourquoi convertir un TIFF en PSD ?
Convertir un TIFF en PSD permet une édition sans perte des calques, masques et chemins de détourage. Aspose.Imaging prend en charge **plus de 50 formats d'entrée et de sortie** et peut traiter des TIFF de plusieurs centaines de pages sans charger le fichier complet en mémoire, offrant ainsi une conversion par lots haute performance.

## Prérequis
- **Java Development Kit (JDK)** 8 ou plus récent installé.  
- **Bibliothèque Aspose.Imaging for Java** (ajoutez via Maven, Gradle ou téléchargement direct).  
- Familiarité de base avec les concepts de programmation Java.

## Comment configurer Aspose.Imaging pour Java
Avant d'ajouter du code, assurez‑vous que la bibliothèque est correctement référencée dans votre système de construction et que vous disposez d'un fichier de licence valide. Cela garantit que l'API fonctionne sans restrictions d'évaluation et que toutes les fonctionnalités, y compris la manipulation des chemins, sont disponibles.

### Maven
Ajoutez la dépendance suivante à votre fichier `pom.xml` :
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle
Incluez cette ligne dans votre fichier `build.gradle` :
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Téléchargement direct
Téléchargez la dernière version depuis [Aspose.Imaging for Java releases](https://releases.aspose.com/imaging/java/).

#### Acquisition de licence
1. **Essai gratuit** – commencez avec un essai de 30 jours.  
2. **Licence temporaire** – obtenez‑en une depuis la [temporary license page](https://purchase.aspose.com/temporary-license/).  
3. **Achat** – achetez une licence complète sur le [site d'Aspose](https://purchase.aspose.com/buy).

Une fois installé et licencié, initialisez Aspose.Imaging dans votre projet :
```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("path_to_license_file");
```

## Comment extraire un chemin de détourage d'un TIFF ?
Extraire un chemin de détourage implique de charger le TIFF, de localiser les ressources de chemin intégrées, puis d'écrire ces ressources dans un nouveau fichier PSD. Le processus lit les données vectorielles directement depuis l'image source, préservant la précision et évitant la conversion raster.

Chargez le TIFF, parcourez ses ressources de chemin, et enregistrez le résultat en tant que PSD. Cette opération lit les données vectorielles intégrées et les écrit dans un nouveau fichier en une seule passe.
```java
String filePath = "YOUR_DOCUMENT_DIRECTORY/SupportExtractingPathsFromTiff/Sample.tif";
try (TiffImage image = (TiffImage) com.aspose.imaging.Image.load(filePath)) {
    // Proceed with extraction steps...
}
```

Parcourez les ressources de chemin dans le cadre actif et collectez‑les :
```java
for (PathResource path : image.getActiveFrame().getPathResources()) {
    System.out.println(path.getName());  // Output the name of each path resource found.
}
```

Enregistrez l'image avec les chemins extraits dans un nouveau fichier PSD :
```java
String outFilePath = "YOUR_OUTPUT_DIRECTORY/SampleWithPaths.psd";
image.save(outFilePath);
```

## Comment créer un chemin de détourage dans un TIFF ?
La création d'un chemin de détourage nécessite de construire un `PathResource` qui décrit le contour vectoriel souhaité, de l'attacher au cadre actif du TIFF, puis d'enregistrer l'image (ou une copie) en tant que PSD afin que le chemin soit conservé. Cette approche vous permet d'ajouter programmétiquement des masques vectoriels aux fichiers raster.

PathResource représente un chemin vectoriel stocké à l'intérieur d'un fichier image.  
Initialisez un nouveau `PathResource` avec les attributs requis :
```java
final PathResource pathResource = new PathResource();
pathResource.setBlockId((short) 2000); // Set Block ID per Photoshop specs
pathResource.setName("My Clipping Path"); // Name your clipping path for easy identification

// Create and add vector path records using the provided coordinates.
pathResource.setRecords(createRecords(0.2f, 0.2f, 0.8f, 0.2f, 0.8f, 0.8f, 0.2f, 0.8f));
```

Assignez la ressource de chemin créée au cadre actif de l'image :
```java
List<PathResource> list = new LinkedList<>();
list.add(pathResource);
image.getActiveFrame().setPathResources(list);
```

Enregistrez le TIFF modifié en tant que PSD contenant désormais le chemin de détourage :
```java
String outFilePath2 = "YOUR_OUTPUT_DIRECTORY/ImageWithPath.psd";
image.save(outFilePath2);
```

## Méthodes d'assistance

### Créer des enregistrements
Générez des enregistrements de chemin vectoriel en utilisant des nœuds de Bézier et des enregistrements de longueur :
```java
private static List<VectorPathRecord> createRecords(float ... coordinates) {
    List<VectorPathRecord> records = createBezierRecords(coordinates); 
    LengthRecord lr = new LengthRecord();
    lr.setOpen(false);
    lr.setRecordCount(records.size());
    
    records.add(0, lr);
    return records;
}
```

### Créer des enregistrements Bézier
Convertissez des tableaux de coordonnées en enregistrements de chemin vectoriel Bézier :
```java
private static List<VectorPathRecord> createBezierRecords(float[] coordinates) {
    final List<VectorPathRecord> list = new LinkedList<>();
    
    for (int index = 0; index < coordinates.length - 1; index += 2) {
        PointF point = new PointF(coordinates[index], coordinates[index + 1]);
        list.add(createBezierRecord(point));
    }
    
    return list;
}
```

### Créer un enregistrement Bézier
Définissez un seul enregistrement de chemin vectoriel à nœud Bézier :
```java
private static VectorPathRecord createBezierRecord(PointF point) {
    BezierKnotRecord it = new BezierKnotRecord();
    it.setPathPoints(new PointF[] { point, point, point });
    return it;
}
```

## Applications pratiques
1. **Flux de travail en conception graphique** – Convertissez le TIFF en PSD pour éditer les calques et masques dans Photoshop.  
2. **Pipelines d'images automatisés** – Traitez par lots des milliers de TIFF, en extrayant ou ajoutant des chemins à la volée.  
3. **Visualisations basées sur les données** – Utilisez des chemins vectoriels pour générer des graphiques ou schémas précis à partir de sources raster.

## Considérations de performance
- **Gestion de la mémoire** – Utilisez try‑with‑resources pour garantir que les objets image sont libérés rapidement.  
- **Traitement par lots** – Parallelisez les conversions avec le `ForkJoinPool` de Java pour de grands ensembles d'images.  
- **Gestion de la résolution** – Ajustez le DPI uniquement lorsque nécessaire afin de maintenir un temps de traitement faible tout en préservant la qualité.

## Conclusion
Vous savez maintenant comment **créer un chemin de détourage** dans des fichiers TIFF et extraire les chemins existants en utilisant Aspose.Imaging pour Java. Ces techniques vous permettent d'intégrer une manipulation d'image sophistiquée dans n'importe quel flux de travail basé sur Java, des utilitaires de bureau aux pipelines de traitement de niveau entreprise.

### Prochaines étapes
- Expérimentez avec différentes formes vectorielles et attributs de chemin.  
- Explorez d'autres fonctionnalités d'Aspose.Imaging telles que le filigrane, la conversion de formats et la gestion des métadonnées.

## Questions fréquemment posées

**Q : Puis‑je utiliser Aspose.Imaging pour Java dans une application commerciale ?**  
R : Oui, à condition de disposer d'une licence commerciale valide ; un essai gratuit est disponible pour l'évaluation.

**Q : Quels formats d'image Aspose.Imaging prend‑il en charge ?**  
R : La bibliothèque prend en charge plus de 100 formats, dont TIFF, PSD, BMP, JPEG, PNG et bien d'autres.

**Q : Comment dépanner les erreurs d'extraction de chemin ?**  
R : Vérifiez que le TIFF source contient réellement des ressources de chemin vectoriel ; utilisez la vérification `hasPathResources()` avant l'extraction.

**Q : Le traitement par lots de plusieurs TIFF est‑il possible ?**  
R : Absolument – combinez le code d'extraction avec les flux parallèles de Java ou un service d'exécution pour gérer efficacement de nombreux fichiers.

**Q : Existe‑t‑il des limitations lors de la création de chemins de détourage dans un TIFF ?**  
R : Les formes complexes peuvent nécessiter un ajustement manuel après création ; l'API gère de manière fiable les courbes de Bézier standard et les lignes droites.

---
**Dernière mise à jour :** 2026-09-02  
**Testé avec :** Aspose.Imaging for Java 24.12  
**Auteur :** Aspose  

## Ressources

- [Documentation Aspose.Imaging](https://reference.aspose.com/imaging/java/)
- [Télécharger Aspose.Imaging pour Java](https://releases.aspose.com/imaging/java/)
- [Acheter une licence](https://purchase.aspose.com/buy)
- [Essai gratuit](https://releases.aspose.com/imaging/java/)
- [Licence temporaire](https://purchase.aspose.com/temporary-license/)
- [Forum de support Aspose](https://forum.aspose.com/c/imaging/14)

## Tutoriels associés

- [Convertir une image en PSD avec Aspose.Imaging pour Java – Guide étape par étape](/imaging/java/format-conversion-export/convert-images-to-psd-using-aspose-imaging-java-guide/)
- [Comment convertir un TIFF en GraphicsPath avec Aspose.Imaging Java](/imaging/java/advanced-drawing-graphics/aspose-imaging-java-tiff-graphicspath-conversion/)
- [Charger et enregistrer efficacement des images TIFF en Java avec Aspose.Imaging](/imaging/java/image-loading-saving/aspose-imaging-java-tiff-image-saving/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}