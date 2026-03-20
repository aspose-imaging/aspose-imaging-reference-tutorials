---
date: '2026-03-20'
description: Apprenez à utiliser Aspose.Imaging pour Java afin de compresser les images
  TIFF avec la compression LZW, réduisant la taille du fichier tout en préservant
  la qualité.
keywords:
- compress TIFF images Java
- Aspose.Imaging LZW compression
- Java image optimization
- TIFF compression in Java with Aspose
- image compression tutorial
title: Comment utiliser Aspose.Imaging pour compresser les images TIFF en Java (Guide
  de compression LZW)
url: /fr/java/compression-optimization/compress-tiff-images-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Tutoriel : Compression d'images TIFF avec Aspose.Imaging Java

## Introduction

Dans ce tutoriel, vous apprendrez **comment utiliser Aspose.Imaging for Java** pour compresser efficacement les images TIFF. La gestion de gros fichiers TIFF peut rapidement consommer le stockage et la bande passante, mais avec la compression LZW (Lempel‑Ziv‑Welch) vous pouvez **réduire la taille du fichier TIFF** sans sacrifier la fidélité de l'image. Nous parcourrons le chargement d'un TIFF, la configuration de la **compression TIFF LZW**, et l'enregistrement du résultat optimisé — parfait pour quiconque s'intéresse à **l'optimisation d'images java**.

**Ce que vous allez apprendre**
- Comment configurer Aspose.Imaging pour Java
- Charger et traiter les images TIFF facilement
- Configurer la compression LZW en utilisant `TiffOptions`
- Enregistrer des images TIFF optimisées, plus petites tout en restant sans perte

Passons rapidement aux prérequis afin que vous puissiez commencer à compresser immédiatement.

## Quick Answers
- **Quelle bibliothèque est nécessaire ?** Aspose.Imaging for Java  
- **Quel algorithme de compression ?** LZW (sans perte)  
- **Versions Java prises en charge ?** Les JDK les plus récents (p. ex., 11, 17)  
- **Ai‑je besoin d’une licence ?** Une licence d’essai ou temporaire suffit pour les tests ; une licence commerciale est requise pour la production.  
- **Réduction de taille typique ?** Jusqu’à 30‑50 % pour les images appropriées  

## Prérequis

Avant d’implémenter la compression d’image dans votre projet Java, assurez‑vous de disposer de :

- **Bibliothèque Aspose.Imaging for Java** – indispensable pour toutes les fonctionnalités de traitement d’image.  
- **Java Development Kit (JDK)** – une version récente compatible avec la bibliothèque Aspose.  
- **Connaissances de base en Java** – la familiarité avec les entrées‑sorties de fichiers et les concepts orientés objet sera utile.

## Installation d’Aspose.Imaging pour Java

Pour commencer, ajoutez la bibliothèque Aspose.Imaging à votre système de build. Choisissez la méthode qui correspond à votre projet.

### Utilisation de Maven
Ajoutez la dépendance suivante à votre `pom.xml` :

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Utilisation de Gradle
Incluez cette ligne dans votre fichier `build.gradle` :

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Téléchargement direct
Sinon, téléchargez la dernière version depuis [versions d'Aspose.Imaging pour Java](https://releases.aspose.com/imaging/java/).

#### Acquisition de licence
Vous pouvez obtenir une licence d’essai gratuite ou demander une licence temporaire pour évaluer pleinement les capacités d’Aspose.Imaging avant l’achat.

## Comment utiliser Aspose.Imaging pour la compression TIFF en Java

Décomposons maintenant l’implémentation étape par étape. Chaque bloc de code reste identique à celui du tutoriel original, mais nous ajoutons un contexte plus clair autour.

### Chargement d’une image TIFF

**Pourquoi c’est important :** Charger correctement l’image crée un objet `Image` valide sur lequel toutes les opérations suivantes agiront.

#### Étape 1 : Importer la classe Image
```java
import com.aspose.imaging.Image;
```

#### Étape 2 : Charger l’image depuis le disque
```java
String dataDir = "YOUR_DOCUMENT_DIRECTORY" + "/sample.tiff";
Image image = Image.load(dataDir);
```

### Création de TiffOptions pour la compression d’image

**Pourquoi c’est important :** `TiffOptions` vous permet de définir exactement comment le TIFF de sortie doit être encodé, y compris le paramètre **compression TIFF LZW**.

#### Étape 1 : Importer les énumérations et la classe d’options requises
```java
import com.aspose.imaging.fileformats.tiff.enums.TiffCompressions;
import com.aspose.imaging.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.imaging.fileformats.tiff.enums.TiffPhotometrics;
import com.aspose.imaging.imageoptions.TiffOptions;
```

#### Étape 2 : Configurer les options de compression
```java
TiffOptions outputSettings = new TiffOptions(TiffExpectedFormat.Default);
outputSettings.setBitsPerSample(new int[] { 4 });
outputSettings.setCompression(TiffCompressions.Lzw);
outputSettings.setPhotometric(TiffPhotometrics.Palette);
```

### Définition d’une palette en niveaux de gris (Optionnel mais utile)

L’application d’une palette en niveaux de gris de 4 bits peut encore **réduire la taille du fichier TIFF**, surtout pour les numérisations monochromes.

#### Étape 1 : Importer l’assistant de palette
```java
import com.aspose.imaging.ColorPaletteHelper;
```

#### Étape 2 : Attribuer la palette en niveaux de gris
```java
outputSettings.setPalette(ColorPaletteHelper.create4BitGrayscale(false));
```

### Enregistrement de l’image TIFF compressée

**Pourquoi c’est important :** L’appel `save` écrit l’image sur le disque en utilisant toutes les options que vous avez configurées, produisant un fichier plus petit et compressé LZW.

#### Étape 1 : Définir le chemin de sortie
```java
String outputDir = "YOUR_OUTPUT_DIRECTORY" + "/SampleTiff_out.tiff";
```

#### Étape 2 : Enregistrer avec les paramètres de compression
```java
image.save(outputDir, outputSettings);
```

## Applications pratiques

Voici quelques scénarios réels où **comment compresser des TIFF** avec LZW peut changer la donne :

1. **Archivage de documents** – Stocker les PDF ou TIFF numérisés de façon plus efficace.  
2. **Imagerie médicale** – Conserver les détails diagnostiques tout en maîtrisant la taille des fichiers.  
3. **Archives photographiques** – Garder les originaux haute résolution sans alourdir le stockage.  
4. **Applications web** – Servir des images plus petites pour des temps de chargement plus rapides et des coûts de bande passante réduits.

## Considérations de performance

Lorsque vous travaillez avec de grandes images, gardez ces conseils à l’esprit pour maintenir des performances optimales :

- **Gestion de la mémoire :** Libérez rapidement les gros objets `Image` (`image.dispose()`) si vous traitez de nombreux fichiers dans une boucle.  
- **Optimisation de la profondeur de bits :** Ajustez `BitsPerSample` à la valeur la plus basse acceptable pour votre cas d’utilisation.  
- **Traitement par lots :** Pour les opérations en masse, envisagez le multithreading mais surveillez l’utilisation du tas JVM.

## Problèmes courants et solutions

| Symptôme | Cause probable | Solution |
|----------|----------------|----------|
| OutOfMemoryError lors du chargement de très gros TIFF | Image chargée entièrement en mémoire | Utilisez `Image.load(dataDir, new LoadOptions { BufferSize = … })` ou traitez par tuiles. |
| Le fichier enregistré est plus volumineux que l’original | `BitsPerSample` incorrect ou palette non concordante | Vérifiez que `setBitsPerSample` correspond à la profondeur de couleur de l’image source. |
| La palette en niveaux de gris apparaît incorrecte | Palette non appliquée avant l’enregistrement | Assurez‑vous que `outputSettings.setPalette(...)` est appelé **avant** `image.save`. |

## Questions fréquentes

**Q : Qu’est‑ce que la compression LZW ?**  
R : La compression Lempel‑Ziv‑Welch (LZW) est un algorithme sans perte qui réduit la taille du fichier sans perdre aucune donnée d’image.

**Q : Puis‑je utiliser Aspose.Imaging pour Java dans des projets commerciaux ?**  
R : Oui, vous pouvez acheter une licence pour une utilisation commerciale. Consultez [Achat Aspose](https://purchase.aspose.com/buy) pour plus de détails.

**Q : La bibliothèque est‑elle compatible avec toutes les versions du JDK ?**  
R : Elle prend en charge la plupart des versions récentes du JDK. Vérifiez la documentation officielle pour la compatibilité exacte.

**Q : Comment gérer les grandes images sans épuiser la mémoire ?**  
R : Mettez en œuvre des pratiques de gestion de mémoire efficaces, comme la libération rapide des objets `Image` et le traitement des images par morceaux plus petits lorsque possible.

**Q : Quels autres formats de fichiers Aspose.Imaging prend‑il en charge ?**  
R : La bibliothèque gère BMP, JPEG, PNG, GIF, et bien d’autres. Explorez la liste complète sur leur [site de documentation](https://reference.aspose.com/imaging/java/).

## Ressources

- **Documentation :** [Référence Aspose.Imaging Java](https://reference.aspose.com/imaging/java/)  
- **Téléchargement :** [Dernières versions](https://releases.aspose.com/imaging/java/)  
- **Achat :** [Acheter maintenant](https://purchase.aspose.com/buy)  
- **Essai gratuit :** [Commencer ici](https://releases.aspose.com/imaging/java/)  
- **Licence temporaire :** [Demander ici](https://purchase.aspose.com/temporary-license/)  
- **Support :** Pour plus d’assistance, visitez le [Forum Aspose](https://forum.aspose.com/c/imaging/14)

---  

**Dernière mise à jour :** 2026-03-20  
**Testé avec :** Aspose.Imaging 25.5 for Java  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}