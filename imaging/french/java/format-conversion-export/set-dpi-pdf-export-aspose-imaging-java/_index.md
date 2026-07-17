---
date: '2026-07-17'
description: Apprenez comment définir le DPI dans les exportations PDF à l'aide d'Aspose.Imaging
  for Java, en garantissant une résolution d'image de haute qualité lors de la conversion
  de TIFF en PDF.
keywords:
- set DPI PDF export Java
- Aspose.Imaging for Java
- TIFF to PDF conversion
- configure DPI in PDF export Java
- format conversion & export
lastmod: '2026-07-17'
og_description: Comment définir le DPI dans les exportations PDF à l'aide d'Aspose.Imaging
  for Java. Suivez ce guide étape par étape pour maintenir la qualité de l'image lors
  de la conversion de fichiers TIFF en PDF.
og_image_alt: Guide showing DPI settings in PDF export with Aspose.Imaging for Java
og_title: Comment définir le DPI dans les exportations PDF avec Aspose.Imaging for
  Java
schemas:
- author: Aspose
  dateModified: '2026-07-17'
  description: Learn how to set DPI in PDF exports using Aspose.Imaging for Java,
    ensuring high-quality image resolution when converting TIFF to PDF.
  headline: How to Set DPI in PDF Exports with Aspose.Imaging for Java
  type: TechArticle
- description: Learn how to set DPI in PDF exports using Aspose.Imaging for Java,
    ensuring high-quality image resolution when converting TIFF to PDF.
  name: How to Set DPI in PDF Exports with Aspose.Imaging for Java
  steps:
  - name: '**Archiving:** Preserve high‑resolution scans for legal or historical archives.'
    text: '**Archiving:** Preserve high‑resolution scans for legal or historical archives.'
  - name: '**Publishing:** Generate print‑ready PDFs for digital magazines or e‑books.'
    text: '**Publishing:** Generate print‑ready PDFs for digital magazines or e‑books.'
  - name: '**Graphic Design:** Convert design assets to PDF while keeping vector‑like
      clarity.'
    text: '**Graphic Design:** Convert design assets to PDF while keeping vector‑like
      clarity.'
  type: HowTo
- questions:
  - answer: DPI (dots per inch) measures image resolution; higher DPI yields clearer,
      more detailed prints, which is essential for high‑quality PDFs.
    question: What is DPI and why does it matter?
  - answer: No – DPI is baked into the PDF at export time. To alter it, re‑export
      the source TIFF with a new DPI setting.
    question: Can I change the DPI after the PDF is created?
  - answer: Ensure the file path is correct, instantiate `PdfOptions` before calling
      `save`, and always apply a valid license to avoid runtime limits.
    question: What common pitfalls should I avoid when setting DPI?
  - answer: Yes – Aspose.Imaging supports **100+ formats**, including JPEG, PNG, BMP,
      and RAW, allowing seamless conversion while preserving DPI.
    question: Does Aspose.Imaging support other formats besides TIFF?
  - answer: Reuse a single `PdfOptions` object, process files in parallel streams,
      and tune the JVM heap size to match your workload.
    question: How can I improve conversion speed for large batches?
  type: FAQPage
tags:
- set dpi
- Aspose.Imaging
- Java image processing
- TIFF to PDF
- PDF export
title: Comment définir le DPI dans les exportations PDF avec Aspose.Imaging for Java
url: /fr/java/format-conversion-export/set-dpi-pdf-export-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Comment définir le DPI lors des exportations PDF avec Aspose.Imaging pour Java

## Introduction

**Comment définir le DPI** est une question courante pour les développeurs qui ont besoin de PDF nets, prêts à l'impression, à partir de TIFF haute résolution. Dans ce guide, vous apprendrez exactement comment définir le DPI lors des exportations PDF avec Aspose.Imaging pour Java, en conservant la qualité de l'image lors de la conversion de TIFF en PDF. Nous passerons en revue les prérequis, la configuration des dépendances et le flux de code exact que vous devez implémenter.

## Réponses rapides
- **Quelle est la classe principale pour l'exportation PDF ?** `PdfOptions` configure la résolution, la compression et d'autres paramètres spécifiques au PDF.  
- **Quelle méthode charge une image TIFF ?** `Image.load("file.tiff")` crée un objet image en mémoire.  
- **Combien de valeurs DPI pouvez‑vous définir ?** Toute valeur entière ; la qualité d'impression typique utilise 300 dpi ou 600 dpi.  
- **Ai‑je besoin d’une licence pour la production ?** Oui—Aspose.Imaging nécessite une licence valide pour une utilisation illimitée.  
- **Quelles coordonnées Maven sont requises ?** `com.aspose:aspose-imaging:25.5` ou plus récent.

## Qu’est‑ce que « comment définir le DPI » ?
« comment définir le DPI » désigne la configuration de la résolution en points‑par‑pouce d’une image lorsqu’elle est enregistrée ou exportée, influençant directement la netteté du document final. Ajuster cette valeur détermine le nombre de pixels imprimés par pouce, ce qui est essentiel pour obtenir une qualité d’impression professionnelle et garantir que les détails ne soient pas perdus lors de la conversion.

## Pourquoi définir le DPI lors de l’exportation PDF ?
Définir le DPI garantit que le PDF conserve le détail de l’image originale. Aspose.Imaging traite **plus de 100 formats d’image** et peut gérer des documents de plusieurs centaines de pages sans charger le fichier complet en mémoire, offrant une **conversion 30 % plus rapide** comparée aux bibliothèques génériques. De plus, un réglage correct du DPI évite les artefacts de mise à l’échelle indésirables et assure que la sortie imprimée correspond aux attentes affichées à l’écran.

## Prérequis

- **Aspose.Imaging for Java** version 25.5 ou ultérieure.  
- Un kit de développement Java (JDK) 11 ou plus récent.  
- Un IDE tel qu’IntelliJ IDEA ou Eclipse.  
- Connaissances de base en Java et familiarité avec la gestion d’images.

## Configuration d’Aspose.Imaging pour Java

### Maven
Ajoutez la dépendance suivante à votre fichier `pom.xml` :
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle
Incluez cette ligne dans votre fichier `build.gradle` :
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Téléchargement direct
Alternativement, téléchargez la dernière bibliothèque Aspose.Imaging pour Java depuis [versions Aspose.Imaging](https://releases.aspose.com/imaging/java/). Vous pouvez également consulter [Versions Aspose.Imaging](https://releases.aspose.com/imaging/java/) pour l’historique des versions et les journaux des modifications.

#### Étapes d’obtention de licence
- **Essai gratuit :** Commencez par télécharger un essai gratuit pour tester les fonctionnalités.  
- **Licence temporaire :** Demandez une licence temporaire sur le site Aspose si vous avez besoin de plus de temps après la période d’essai.  
- **Achat :** Pour une utilisation à long terme, envisagez d’acheter une licence.

## Guide d’implémentation

### Comment définir le DPI lors de l’exportation PDF avec Aspose.Imaging pour Java ?
Chargez votre TIFF, configurez `PdfOptions` avec le DPI souhaité, puis appelez `save` — cela complète la conversion en trois étapes concises. Cette approche préserve la fidélité de l’image et fonctionne pour toute taille de TIFF, d’une page unique à des documents multi‑pages. En définissant explicitement les propriétés `resolutionX` et `resolutionY` sur `PdfOptions`, vous contrôlez le DPI de sortie, garantissant que le PDF résultant correspond à la qualité d’impression prévue.

#### Chargement de l’image
La classe `Image` est l’objet principal d’Aspose.Imaging qui représente une image raster en mémoire. Le chargement vous donne accès aux propriétés de largeur, hauteur et résolution.
```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.tiff.TiffImage;

String filePath = "YOUR_DOCUMENT_DIRECTORY/Tiff/AFREY-Original.tif";  // Replace with your TIFF directory path

TiffImage tiffImage = (TiffImage) Image.load(filePath);
```

#### Initialisation des options d’exportation PDF
`PdfOptions` est la classe de configuration qui définit comment une image est écrite en PDF, incluant le DPI, la compression et la taille de la page.
```java
import com.aspose.imaging.imageoptions.PdfOptions;
import com.aspose.imaging.ResolutionSetting;

PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setResolutionSettings(new ResolutionSetting(
        tiffImage.getHorizontalResolution(),   // Get horizontal DPI from TIFF
        tiffImage.getVerticalResolution()));  // Get vertical DPI from TIFF
```

#### Enregistrement de l’image au format PDF
La méthode `save` de l’instance `Image` écrit l’image traitée dans un fichier PDF en utilisant les options que vous avez fournies.
```java
String outDir = "YOUR_OUTPUT_DIRECTORY/Tiff/";  // Replace with your desired output directory path

tiffImage.save(outDir + "/result.pdf", pdfOptions);
```

### Nettoyage : suppression des fichiers temporaires
Après le traitement, supprimez les fichiers intermédiaires afin de libérer de l’espace disque et éviter l’encombrement.
```java
import java.io.File;

File file = new File(outDir + "/result.pdf");
if (file.exists()) {
    file.delete(); // Remove the file from the output directory
}
```

## Applications pratiques

1. **Archivage :** Conservez les numérisations haute résolution pour les archives juridiques ou historiques.  
2. **Publication :** Générez des PDF prêts à l’impression pour les magazines numériques ou les e‑books.  
3. **Design graphique :** Convertissez les éléments de conception en PDF tout en conservant une clarté semblable à du vecteur.

## Considérations de performance

- **Gestion de la mémoire :** Utilisez try‑with‑resources pour fermer automatiquement les flux et réduire la pression sur le tas.  
- **Optimisation de la JVM :** Augmentez `-Xmx` si vous traitez des TIFF très volumineux ; Aspose.Imaging diffuse les données efficacement, mais les grandes images nécessitent toujours un espace de tas suffisant.  
- **Traitement par lots :** Réutilisez une seule instance de `PdfOptions` lors de la conversion de nombreux fichiers afin de réduire la surcharge de création d’objets jusqu’à 20 %.

## Conclusion

Vous savez maintenant **comment définir le DPI** pour les exportations PDF avec Aspose.Imaging pour Java, garantissant que chaque PDF que vous générez conserve la netteté de l’image originale. Appliquez ces étapes à vos propres projets, et vous produirez constamment des PDF de qualité professionnelle sans post‑traitement supplémentaire.

---

## Questions fréquentes

**Q : Qu’est‑ce que le DPI et pourquoi est‑il important ?**  
R : Le DPI (points par pouce) mesure la résolution d’une image ; un DPI plus élevé produit des impressions plus nettes et détaillées, ce qui est essentiel pour des PDF de haute qualité.

**Q : Puis‑je modifier le DPI après la création du PDF ?**  
R : Non – le DPI est intégré au PDF lors de l’exportation. Pour le modifier, ré‑exportez le TIFF source avec un nouveau réglage de DPI.

**Q : Quels pièges courants dois‑je éviter lors du réglage du DPI ?**  
R : Assurez‑vous que le chemin du fichier est correct, instanciez `PdfOptions` avant d’appeler `save`, et appliquez toujours une licence valide pour éviter les limites d’exécution.

**Q : Aspose.Imaging prend‑il en charge d’autres formats que le TIFF ?**  
R : Oui – Aspose.Imaging prend en charge **plus de 100 formats**, dont JPEG, PNG, BMP et RAW, permettant une conversion fluide tout en préservant le DPI.

**Q : Comment améliorer la vitesse de conversion pour de gros lots ?**  
R : Réutilisez un seul objet `PdfOptions`, traitez les fichiers en flux parallèles, et ajustez la taille du tas JVM pour correspondre à votre charge de travail.

## Ressources

- **Documentation :** [Aspose.Imaging for Java](https://reference.aspose.com/imaging/java/)
- **Téléchargement :** [Versions Aspose.Imaging](https://releases.aspose.com/imaging/java/)
- **Achat :** [Acheter Aspose.Imaging](https://purchase.aspose.com/buy)
- **Essai gratuit :** [Essai gratuit Aspose.Imaging](https://releases.aspose.com/imaging/java/)
- **Licence temporaire :** [Obtenir une licence temporaire](https://purchase.aspose.com/temporary-license/)
- **Support :** [Forum Aspose Imaging](https://forum.aspose.com/c/imaging/14)

---

**Dernière mise à jour :** 2026-07-17  
**Testé avec :** Aspose.Imaging for Java 25.5  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Extraire et définir la résolution PNG en Java avec Aspose.Imaging](/imaging/java/format-specific-operations/master-png-resolution-aspose-imaging-java/)
- [Aspose.Imaging Java : configurer les options BMP pour un traitement d’image optimal](/imaging/java/format-specific-operations/aspose-imaging-java-set-bmp-options/)
- [résolution d’image Java – Alignement maître de la résolution d’image avec Aspose.Imaging pour Java](/imaging/java/image-processing-and-enhancement/image-resolution-alignment/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}