---
date: 2026-01-14
description: Apprenez à convertir les fichiers DICOM en BMP et à ajuster leur gamma
  en Java avec Aspose.Imaging. Ce guide montre comment traiter facilement les images
  DICOM.
linktitle: DICOM Image Gamma Adjustment
second_title: Aspose.Imaging Java Image Processing API
title: Convertir DICOM en BMP – Ajustement du gamma avec Aspose.Imaging pour Java
url: /fr/java/image-processing-and-enhancement/dicom-image-gamma-adjustment/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DICOM en BMP – Ajustement Gamma avec Aspose.Imaging pour Java

Si vous devez **convertir DICOM en BMP** tout en ajustant le contraste de l’image, vous êtes au bon endroit. Dans ce tutoriel, nous parcourrons les étapes exactes pour charger un fichier DICOM, appliquer une correction gamma et enregistrer le résultat au format BMP à l’aide d’Aspose.Imaging pour Java. À la fin, vous comprendrez **comment traiter les fichiers DICOM** de façon programmatique et produire une sortie bitmap de haute qualité pour les flux de travail d’imagerie médicale en aval.

## Réponses rapides
- **Que signifie « convertir DICOM en BMP » ?** Cela transforme une image médicale DICOM en un bitmap BMP standard tout en préservant les données de pixels.  
- **Quelle bibliothèque gère la conversion ?** Aspose.Imaging pour Java fournit une API simple pour charger le DICOM et l’enregistrer en BMP.  
- **Ai‑je besoin d’une licence ?** Une version d’essai gratuite suffit pour le développement ; une licence commerciale est requise pour la production.  
- **Combien de temps le code met‑il à s’exécuter ?** Moins d’une seconde pour des fichiers DICOM typiques de 512 × 512 sur un CPU moderne.  
- **Puis‑je modifier la valeur gamma ?** Oui—passez n’importe quel entier (par ex. 30‑70) à `adjustGamma()` selon vos besoins de contraste.

## Qu’est‑ce que « convertir DICOM en BMP » ?
Convertir DICOM en BMP consiste à décoder le format d’image médicale DICOM et à ré‑encoder les données de pixels dans un bitmap BMP. BMP est largement supporté par les outils d’imagerie, ce qui le rend idéal pour l’inspection visuelle, les rapports ou le traitement ultérieur.

## Pourquoi ajuster le gamma lors de la conversion ?
L’ajustement gamma modifie la courbe de luminance de l’image, améliorant la visibilité des détails subtils sans altérer les données sous‑jacentes. Cela est particulièrement précieux en radiologie où le contraste peut influencer le diagnostic.

## Prérequis

### 1. Environnement de développement Java
- JDK 8 ou version supérieure installé et configuré dans votre IDE ou en ligne de commande.

### 2. Bibliothèque Aspose.Imaging pour Java
- Téléchargez la bibliothèque depuis le [lien de téléchargement](https://releases.aspose.com/imaging/java/).

### 3. Image DICOM d’entrée
- Disposez d’un fichier DICOM. Des fichiers d’exemple sont librement disponibles en ligne pour les tests.

## Importer les packages
Tout d’abord, importez les classes nécessaires. Le bloc ci‑dessous doit rester exactement tel qu’il est présenté :

```java
import com.aspose.imaging.fileformats.dicom.DicomImage;
import com.aspose.imaging.image.Image;
import com.aspose.imaging.imageoptions.BmpOptions;
import java.io.File;
import java.io.FileInputStream;
import java.io.IOException;
```

## Convertir DICOM en BMP – Guide étape par étape

### Étape 1 : Définir les chemins de fichiers
Spécifiez où se trouve le DICOM source et où le BMP doit être écrit.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = dataDir + "AdjustingGamma.bmp";
```

### Étape 2 : Charger l’image DICOM
Ouvrez le flux de fichier et créez une instance `DicomImage`.

```java
File file = new File(inputFile);

try (FileInputStream fis = new FileInputStream(file)) {
    // Load a DICOM image in an instance of DicomImage
    try (DicomImage image = (DicomImage) Image.load(fis)) {
```

### Étape 3 : Ajuster le gamma
Appliquez la correction gamma souhaitée (par ex. 50) avant l’enregistrement.

```java
        // Adjust the gamma
        image.adjustGamma(50);
```

### Étape 4 : Enregistrer le BMP résultant
Créez les options BMP et écrivez l’image traitée sur le disque. Le bloc `catch` gère les éventuels problèmes d’E/S.

```java
        // Create an instance of BmpOptions for the resultant image and save the resultant image
        image.save(outputFile, new BmpOptions());
    }
} catch (IOException ex) {
    // Handle any potential exceptions
    com.aspose.imaging.examples.Logger.println(ex.getMessage());
    ex.printStackTrace();
}
```

Voici le flux complet pour **convertir DICOM en BMP** tout en ajustant le gamma.

## Problèmes courants et solutions
- **Balises DICOM non prises en charge** – Assurez‑vous que le fichier DICOM contient des données de pixels ; les flux chiffrés ou compressés peuvent nécessiter un décodage supplémentaire.  
- **Erreurs de mémoire insuffisante** – Pour des images très volumineuses, augmentez le tas JVM (`-Xmx2g`) ou traitez l’image par tuiles.  
- **Valeur gamma incorrecte** – Des valeurs inférieures à 0 ou supérieures à 100 peuvent produire des résultats inattendus ; restez dans la plage 0‑100.

## Questions fréquentes

**Q : Qu’est‑ce qu’une image DICOM ?**  
R : DICOM (Digital Imaging and Communications in Medicine) est le format universel pour stocker et transmettre les images médicales telles que les radiographies, les scanners CT et les IRM.

**Q : Pourquoi l’ajustement gamma est‑il important pour les images DICOM ?**  
R : L’ajustement gamma améliore le contraste visuel, rendant les structures anatomiques plus faciles à voir lors de l’analyse.

**Q : Puis‑je traiter les images DICOM dans d’autres langages ?**  
R : Oui—Aspose.Imaging propose des bibliothèques pour .NET, Java et d’autres plateformes, permettant un développement multiplateforme.

**Q : Existe‑t‑il des limitations lors du travail avec des fichiers DICOM ?**  
R : Certains fichiers DICOM contiennent des métadonnées étendues ou une compression propriétaire ; une bonne connaissance du standard DICOM aide à éviter les pièges.

**Q : Où puis‑je trouver d’autres tutoriels Aspose.Imaging ?**  
R : Consultez la [documentation Aspose.Imaging](https://reference.aspose.com/imaging/java/) pour des guides supplémentaires, des références API et des projets d’exemple.

## Conclusion
En suivant ce guide, vous savez maintenant **comment traiter les fichiers DICOM**, appliquer une correction gamma et **convertir DICOM en BMP** à l’aide d’Aspose.Imaging pour Java. Cette capacité simplifie les flux de travail d’imagerie médicale, vous permettant de générer des représentations bitmap pour les rapports, l’analyse IA ou l’archivage.

Si vous rencontrez des difficultés, la communauté du [forum Aspose.Imaging](https://forum.aspose.com/) est un excellent endroit pour poser des questions et partager des idées.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2026-01-14  
**Testé avec :** Aspose.Imaging pour Java 24.11 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

---