---
date: '2026-11-04'
description: Apprenez à créer un PNG animé en Java avec une licence Aspose Imaging,
  ajoutez la dépendance Maven, convertissez le TIFF en APNG et enregistrez l'image.
keywords:
- aspose imaging license
- convert tiff to apng
- tiff to png conversion
- add maven dependency java
- control animation speed java
lastmod: '2026-11-04'
og_description: Apprenez à créer un PNG animé en Java avec une licence Aspose Imaging,
  ajoutez la dépendance Maven, convertissez le TIFF en APNG et contrôlez la vitesse
  d'animation.
og_image_alt: Guide showing how to generate animated PNGs in Java with Aspose Imaging
og_title: Créer un PNG animé en Java avec une licence Aspose Imaging
schemas:
- author: Aspose
  dateModified: '2026-11-04'
  description: Learn how to create animated PNG in Java with an Aspose Imaging license,
    add the Maven dependency, convert TIFF to APNG and save the image.
  headline: Create animated PNG in Java using an Aspose Imaging license
  type: TechArticle
- description: Learn how to create animated PNG in Java with an Aspose Imaging license,
    add the Maven dependency, convert TIFF to APNG and save the image.
  name: Create animated PNG in Java using an Aspose Imaging license
  steps:
  - name: '**Web development** – Animated banners, icons, or loading spinners that
      work across browsers without needing GIF support.'
    text: '**Web development** – Animated banners, icons, or loading spinners that
      work across browsers without needing GIF support.'
  - name: '**Desktop applications** – Enrich Swing or JavaFX UI components with subtle
      motion cues.'
    text: '**Desktop applications** – Enrich Swing or JavaFX UI components with subtle
      motion cues.'
  - name: '**Data visualization** – Animate chart transitions or step‑by‑step walkthroughs
      for reports.'
    text: '**Data visualization** – Animate chart transitions or step‑by‑step walkthroughs
      for reports.'
  type: HowTo
- questions:
  - answer: You must set the value yourself with `setDefaultFrameTime(int ms)`; there
      is no hidden default.
    question: What is the default frame duration for APNG using Aspose.Imaging?
  - answer: Yes—load the file, modify the frame timings via `ApngOptions`, and save
      it again.
    question: Can I adjust animation speed in an existing APNG file?
  - answer: Ensure the image path is correct, allocate enough heap memory for large
      files, and use `try‑with‑resources` to release resources promptly.
    question: What are common pitfalls when loading images with Aspose.Imaging?
  - answer: Visit [Aspose's download page](https://releases.aspose.com/imaging/java/)
      to request a trial.
    question: How do I obtain a free trial license for Aspose.Imaging?
  - answer: Absolutely—you can combine it with Spring, Apache Commons, or any UI framework
      such as JavaFX.
    question: Is Aspose.Imaging compatible with other Java libraries?
  type: FAQPage
tags:
- aspose imaging
- animated png java
- tiff conversion
- maven dependency
- java image processing
title: Créer un PNG animé en Java avec une licence Aspose Imaging
url: /fr/java/animation-multi-frame-images/aspose-imaging-java-animated-png-guide/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Créer un PNG animé en Java avec une licence Aspose Imaging

## Introduction

Si vous devez **créer des PNG animés en Java** et que vous recherchez une solution fiable et prête pour la production, une **licence Aspose Imaging** vous donne un accès complet à l'API haute performance de la bibliothèque. Que vous construisiez un portail web, une interface de bureau ou un tableau de bord de visualisation de données, les PNG animés (APNG) ajoutent un mouvement fluide sans les inconvénients des GIF. Ce tutoriel vous guide à travers l'ajout de la dépendance Maven, la conversion d'un TIFF multi‑pages en APNG, et le contrôle du timing des images, afin que vous puissiez livrer rapidement des animations soignées.

## Réponses rapides
- **Quelle bibliothèque permet la création d'APNG en Java ?** Aspose.Imaging avec la dépendance Maven Aspose Imaging.  
- **Quel format peut être converti en APNG ?** Les fichiers TIFF multi‑pages peuvent être convertis en PNG animés.  
- **Comment contrôler la vitesse de l'animation ?** Utilisez `ApngOptions.setDefaultFrameTime(milliseconds)`.  
- **Ai‑je besoin d’une licence pour la production ?** Oui—une licence Aspose Imaging supprime les limites d'évaluation et débloque toutes les fonctionnalités.  
- **Puis‑je utiliser Maven ou Gradle ?** Les deux sont pris en charge ; il suffit d’ajouter la dépendance appropriée.

## Qu’est‑ce qu’une licence Aspose Imaging ?
Une **licence Aspose Imaging** est un fichier qui débloque l’ensemble complet et illimité des fonctionnalités de la bibliothèque Aspose.Imaging pour Java, en supprimant les filigranes d’évaluation et les limites d’utilisation. Vous chargez la licence une fois au démarrage de l’application, et tous les appels API ultérieurs s’exécutent sans restrictions d’essai.

## Pourquoi utiliser Aspose.Imaging pour les APNG ?
Aspose.Imaging traite **plus de 150 formats d’image** (y compris JPEG, PNG, TIFF, BMP et WebP) et peut gérer des documents de plusieurs centaines de pages tout en maintenant l’utilisation de la mémoire sous 200 Mo sur une JVM typique de 8 Go. L’encodeur APNG natif de la bibliothèque préserve la transparence, la profondeur de couleur complète et le timing par image sans outils externes, ce qui en fait l’option la plus rapide et la plus fiable pour les développeurs Java.

## Prérequis
- Java 8 ou supérieur installé.  
- Un IDE tel qu’IntelliJ IDEA ou Eclipse.  
- Maven ou Gradle pour la gestion des dépendances (ou le fichier JAR).

## Ajout de la dépendance Maven Aspose Imaging

### Maven

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Gradle

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

Pour ceux qui préfèrent les téléchargements directs, vous pouvez obtenir la dernière version depuis la [page de téléchargement d’Aspose](https://releases.aspose.com/imaging/java/). Vous pouvez également consulter les [versions d’Aspose.Imaging pour Java](https://releases.aspose.com/imaging/java/) pour les notes de version.

## Acquisition de licence

Pour débloquer l’ensemble complet des fonctionnalités sans limites d’évaluation :

- **Essai gratuit :** Commencez avec un essai gratuit pour tester les fonctionnalités.  
- **Licence temporaire :** Obtenez une licence temporaire pour un accès prolongé pendant le développement.  
- **Achat :** Pour une utilisation à long terme, achetez une licence commerciale.

Initialisez la licence dans votre code :

```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("path/to/your/license/file.lic");
```

`License` charge le fichier de licence Aspose.Imaging pour débloquer toutes les fonctionnalités.

## Comment convertir un TIFF en APNG avec Aspose.Imaging ?
Chargez le TIFF source, configurez les options APNG, puis enregistrez le résultat. La bibliothèque extrait chaque page du TIFF comme une image distincte et écrit un PNG animé conforme aux normes. Ce processus vous permet également de définir le timing par défaut des images, de choisir le niveau de compression et, éventuellement, de redimensionner les images avant l’enregistrement, vous offrant un contrôle complet sur la qualité finale de l’animation et la taille du fichier.

### Chargement d’une image
`Image` est la classe de base représentant un objet image dans Aspose.Imaging.

```java
import com.aspose.imaging.Image;
```

```java
String inputFilePath = "YOUR_DOCUMENT_DIRECTORY/img4.tif";

try (Image image = Image.load(inputFilePath)) {
    // The image is now loaded and ready for manipulation.
}
```

### Définition de la durée par défaut des images pour l’APNG
`ApngOptions` configure les paramètres pour enregistrer une image en tant que PNG animé.

```java
import com.aspose.imaging.imageoptions.ApngOptions;
```

```java
ApngOptions op = new ApngOptions();
op.setDefaultFrameTime(500); // Default frame time set to 500 milliseconds
```

### Enregistrement de l’image en tant qu’APNG
Préparez le chemin de sortie et invoquez `save` avec les options configurées :

```java
String outputFilePath = "YOUR_OUTPUT_DIRECTORY/img4.tif.500ms.png";
```

```java
try (Image image = Image.load("YOUR_DOCUMENT_DIRECTORY/img4.tif")) {
    ApngOptions op = new ApngOptions();
    op.setDefaultFrameTime(500); // Frame time set to 500 ms
    
    image.save(outputFilePath, op);
}
```

La ligne `image.save(outputFilePath, op);` **enregistre l’image en tant qu’APNG**. Assurez‑vous que le fichier de sortie se termine par `.png` et que `ApngOptions` reflète le timing des images souhaité.

## Comment enregistrer une image en tant qu’APNG en Java ?
Appelez `image.save` avec une instance `ApngOptions` qui spécifie le temps d’image par défaut. Ajustez `setDefaultFrameTime` pour accélérer ou ralentir l’animation, et vous pouvez réutiliser le même appel pour d’autres formats source comme les PDF multi‑pages. L’utilisation d’un bloc try‑with‑resources garantit que les ressources image sont libérées rapidement, évitant les fuites de mémoire lors du traitement par lots.

## Applications pratiques
1. **Développement web** – Bannières animées, icônes ou indicateurs de chargement qui fonctionnent sur tous les navigateurs sans nécessiter la prise en charge des GIF.  
2. **Applications de bureau** – Enrichissez les composants UI Swing ou JavaFX avec des indices de mouvement subtils.  
3. **Visualisation de données** – Animez les transitions de graphiques ou les présentations pas à pas pour les rapports.

Combinez Aspose.Imaging avec des bibliothèques comme Swing, JavaFX ou Spring Boot pour offrir une expérience utilisateur fluide.

## Considérations de performance
- **Redimensionner judicieusement :** Les résolutions plus élevées augmentent l’utilisation de la mémoire ; réduisez la taille lorsque c’est possible.  
- **Libérer rapidement :** Utilisez `try‑with‑resources` (comme montré) pour libérer les ressources natives.  
- **Traitement par lots :** Réutilisez une seule instance `License` et évitez de charger plusieurs fois le même fichier source lors de la génération de nombreux APNG.

## Problèmes courants et solutions
| Problème | Cause | Solution |
|----------|-------|----------|
| **OutOfMemoryError** lors du chargement de gros TIFF | L’image est trop grande pour le tas JVM | Augmentez `-Xmx` ou réduisez la taille avant le traitement |
| **Images vides** dans le APNG de sortie | Les pages du TIFF source ont des dimensions différentes | Redimensionnez toutes les pages à une taille commune avant l’enregistrement |
| **Licence non appliquée** | Chemin du fichier de licence incorrect | Vérifiez le chemin et assurez‑vous que le fichier est lisible au moment de l’exécution |

## Questions fréquemment posées

**Q : Quelle est la durée d’image par défaut pour l’APNG avec Aspose.Imaging ?**  
R : Vous devez définir vous‑même la valeur avec `setDefaultFrameTime(int ms)` ; il n’existe pas de valeur par défaut cachée.

**Q : Puis‑je ajuster la vitesse de l’animation dans un fichier APNG existant ?**  
R : Oui—chargez le fichier, modifiez le timing des images via `ApngOptions`, puis enregistrez‑le à nouveau.

**Q : Quels sont les pièges courants lors du chargement d’images avec Aspose.Imaging ?**  
R : Assurez‑vous que le chemin de l’image est correct, allouez suffisamment de mémoire du tas pour les gros fichiers, et utilisez `try‑with‑resources` pour libérer les ressources rapidement.

**Q : Comment obtenir une licence d’essai gratuite pour Aspose.Imaging ?**  
R : Visitez la [page de téléchargement d’Aspose](https://releases.aspose.com/imaging/java/) pour demander un essai.

**Q : Aspose.Imaging est‑il compatible avec d’autres bibliothèques Java ?**  
R : Absolument—vous pouvez le combiner avec Spring, Apache Commons ou tout framework UI tel que JavaFX.

## Ressources
- **Documentation** : [Aspose.Imaging Documentation](https://reference.aspose.com/imaging/java/)  
- **Téléchargement** : [Latest Release Download](https://releases.aspose.com/imaging/java/)  
- **Achat** : [Buy Aspose.Imaging](https://purchase.aspose.com/buy)  
- **Essai gratuit** : [Get Started with Free Trial](https://releases.aspose.com/imaging/java/)  
- **Licence temporaire** : [Acquire Temporary License](https://purchase.aspose.com/temporary-license/)  
- **Forum de support** : [Aspose Community Support](https://forum.aspose.com/c/imaging/14)

---

**Dernière mise à jour :** 2026-11-04  
**Testé avec :** Aspose.Imaging 25.5 pour Java  
**Auteur :** Aspose

## Tutoriels associés

- [Comment créer un GIF animé avec Aspose.Imaging Java : contrôle des images et des boucles](/imaging/java/animation-multi-frame-images/gif-manipulation-java-aspose-imaging-guide/)
- [Comment créer un TIFF multi‑pages avec Aspose.Imaging pour Java – Guide complet](/imaging/java/animation-multi-frame-images/create-multi-page-tiff-aspose-imaging-java/)
- [traiter un TIFF multi‑images en Java avec Aspose.Imaging](/imaging/java/animation-multi-frame-images/java-aspose-imaging-multi-frame-tiff-processing/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}