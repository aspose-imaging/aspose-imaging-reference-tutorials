---
date: 2026-01-17
description: Apprenez à ajuster la luminosité des images avec Aspose.Imaging pour
  Java. Ce tutoriel de traitement d'images Java montre une amélioration d'image Java
  sans effort.
linktitle: Image Brightness Adjustment
second_title: Aspose.Imaging Java Image Processing API
title: Comment ajuster la luminosité des images avec Aspose.Imaging pour Java
url: /fr/java/image-processing-and-enhancement/image-brightness-adjustment/
weight: 25
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Comment ajuster la luminosité des images avec Aspose.Imaging pour Java

## Introduction

L’ajustement de la luminosité est l’une des tâches les plus courantes en **Java Image Processing**. Que vous prépariez des scans médicaux, retouchiez des photos de produits ou simplement amélioriez des images personnelles, sachez **comment ajuster la luminosité** rapidement et de manière fiable peut vous faire gagner des heures de travail manuel. Dans ce tutoriel, nous parcourrons un exemple complet, prêt pour la production, qui montre **comment ajuster la luminosité** à l'aide d'Aspose.Imaging pour Java, une bibliothèque puissante qui gère des dizaines de formats dès le départ.

## Réponses rapides
- **Que signifie « ajuster la luminosité » ?** Cela modifie la luminosité globale de chaque pixel de l'image.
- **Quelle bibliothèque est utilisée ?** Aspose.Imaging pour Java.
- **Ai-je besoin d'une licence ?** Un essai gratuit fonctionne pour le développement ; une licence commerciale est requise pour la production.
- **Formats pris en charge ?** BMP, JPEG, PNG, DICOM, TIFF et bien d'autres.
- **Durée de mise en œuvre typique ?** Environ 10 minutes pour un script de base.

## Qu’est‑ce que « how to ajuster la luminosité » en traitement d’image Java ?

Ajuster la luminosité signifie appliquer un décalage uniforme aux valeurs d’intensité des pixels. Dans Aspose.Imaging, cela est exposé via la méthode `adjustBrightness(int value)`, où les valeurs positives éclaircissent l’image et les valeurs négatives l’assombrissent.

## Pourquoi utiliser Aspose.Imaging pour l’amélioration d’images Java ?

- **Prise en charge de grands formats** – Gère DICOM, BMP, JPEG, PNG, TIFF, etc., sans codecs supplémentaires.
- **API simple** : une seule ligne appelle à des ajustements courants tels que la luminosité, le contraste et le gamma.
- **Performances optimisées** – Fonctionne efficacement avec les images médicales volumineuses et les photos haute résolution.

- **Multiplateforme** – Fonctionne sur n'importe quelle JVM, ce qui le rend idéal pour les pipelines de traitement côté serveur.

## Prérequis

Avant de vous plonger dans le code, assurez-vous de disposer des éléments suivants :

1. **Environnement de développement Java** – Installez la dernière version du JDK depuis le [site web](https://www.oracle.com/java/technologies/javase-downloads).

2. **Aspose.Imaging pour Java** – Suivez le guide d'installation sur le site web d'Aspose.Imaging, à l'adresse [Documentation Aspose.Imaging pour Java](https://reference.aspose.com/imaging/java/).

3. **Image d'exemple** – Un fichier DICOM (`image.dcm`) ou tout autre format compatible que vous souhaitez éclaircir. 4. **IDE** – Eclipse, IntelliJ IDEA ou tout autre IDE Java de votre choix.

Avec ces prérequis prêts, commençons à coder.

## Importer des packages

Tout d’abord, importez les classes Aspose.Imaging requises :

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.dicom.DicomImage;
import com.aspose.imaging.imageoptions.BmpOptions;
```

## Guide étape par étape

### Étape 1 : Définir les chemins d’accès aux fichiers

Définissez les emplacements d’entrée et de sortie. Remplacez « Votre répertoire de documents » par le chemin d’accès réel sur votre ordinateur.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "AdjustingBrightness_out.bmp";
```

### Étape 2 : Charger l’image DICOM

Utilisez la méthode `Image.load` pour charger le fichier DICOM en mémoire.

```java
try (DicomImage image = (DicomImage) Image.load(inputFile)) {
    // Image is now ready for processing.
}
```

### Étape 3 : Ajuster la luminosité

Dans le bloc `try`, appelez `adjustBrightness`. Une valeur de `50` éclaircit sensiblement l’image ; utilisez des nombres négatifs pour l’assombrir.

```java
image.adjustBrightness(50);
```

> **Conseil :** Pour des ajustements subtils, commencez par des valeurs comprises entre `-20` et `20`. Testez différents niveaux pour éviter d’écrêter les hautes lumières ou les ombres.

### Étape 4 : Enregistrer l’image résultante

Enfin, enregistrez l’image modifiée sur le disque en utilisant les options BMP (vous pouvez choisir d’autres formats si nécessaire).

```java
image.save(outputFile, new BmpOptions());
```

Une fois le programme terminé, le fichier `AdjustingBrightness_out.bmp` contiendra la version éclaircie de votre image DICOM d'origine.

## Problèmes courants et solutions

| Problème | Cause | Solution |

|-------|-------|-----|

| **Aucun fichier de sortie créé** | Chemin incorrect ou autorisations d'écriture manquantes | Vérifiez le chemin d'accès à `outputFile` et assurez-vous que le répertoire existe et que vous disposez des droits d'écriture. |

| **Image délavée** | Valeur de luminosité trop élevée | Réduisez la valeur d'ajustement ou appliquez une correction de contraste après l'éclaircissement. |

| **Erreur de format non pris en charge** | Tentative de chargement d'un format non géré par le chargeur DICOM | Utilisez la classe d'image appropriée (par exemple, `BmpImage`) pour les fichiers non DICOM. |

## Foire aux questions

### Q1 : Aspose.Imaging pour Java est-il adapté aux tâches professionnelles de traitement d'images ?

R1 : Oui, Aspose.Imaging pour Java est une bibliothèque polyvalente conçue pour le traitement d'images professionnel, offrant un large éventail de fonctionnalités et d'options.

### Q2 : Puis-je utiliser Aspose.Imaging pour Java avec d'autres bibliothèques Java ?

R2 : Absolument ! Aspose.Imaging pour Java s'intègre parfaitement avec d'autres bibliothèques et frameworks Java.

### Q3 : Quels formats d'image sont pris en charge par Aspose.Imaging pour Java ?

R3 : Aspose.Imaging pour Java prend en charge de nombreux formats d'image, notamment BMP, JPEG, PNG, TIFF, GIF, et bien d'autres.

### Q4 : Existe-t-il une version d'essai gratuite d'Aspose.Imaging pour Java ?

R4 : Oui, vous pouvez essayer Aspose.Imaging pour Java gratuitement. Rendez-vous [ici](https://releases.aspose.com/) pour commencer.

### Q5 : Où puis-je obtenir de l'aide concernant Aspose.Imaging pour Java ?

A5 : Vous trouverez de l’aide et pourrez rejoindre la communauté sur le forum [Aspose.Imaging for Java](https://forum.aspose.com/).

## Conclusion

Dans ce **tutoriel de traitement d’images Java**, nous avons montré **comment ajuster la luminosité** avec Aspose.Imaging for Java. En suivant ces quatre étapes simples (importation des packages, définition des chemins d’accès, chargement de l’image, ajustement de la luminosité et enregistrement), vous pouvez intégrer des fonctionnalités robustes d’**amélioration d’images Java** dans n’importe quelle application, des chaînes de traitement d’images médicales aux flux de travail photo pour le e-commerce. Expérimentez avec différentes valeurs de luminosité, combinez-les avec des ajustements de contraste ou de gamma, et exploitez pleinement le potentiel de vos données visuelles.

---

**Dernière mise à jour :** 17/01/2026

**Testé avec :** Aspose.Imaging for Java 24.12

**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}