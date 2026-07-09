---
date: 2026-01-12
description: Apprenez comment ajuster le contraste dans les images DICOM – un guide
  étape par étape sur la façon d’ajuster le contraste avec Aspose.Imaging pour Java
  et de convertir DICOM en BMP.
linktitle: DICOM Image Contrast Adjustment
second_title: Aspose.Imaging Java Image Processing API
title: Comment ajuster le contraste des images DICOM avec Aspose.Imaging pour Java
url: /fr/java/image-processing-and-enhancement/dicom-image-contrast-adjustment/
weight: 23
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Comment ajuster le contraste dans les images DICOM avec Aspose.Imaging pour Java

Dans l'imagerie médicale moderne, **comment ajuster le contraste** peut faire la différence entre un diagnostic clair et un détail manqué. Ce tutoriel vous guide à travers les étapes exactes pour ajuster le contraste dans les fichiers DICOM en utilisant Aspose.Imaging pour Java, et vous montre comment convertir ces images DICOM en BMP pour une visualisation facile ou un traitement ultérieur. À la fin, vous disposerez d’un extrait de code prêt à l’emploi que vous pourrez intégrer dans n’importe quel projet Java.

## Réponses rapides
- **Que fait l'ajustement du contraste ?** Il élargit la plage entre les pixels sombres et lumineux, faisant ressortir les structures.  
- **Quelle bibliothèque est requise ?** Aspose.Imaging for Java.  
- **Puis-je exporter en BMP ?** Oui – vous pouvez convertir le DICOM en BMP après avoir ajusté le contraste.  
- **Ai‑je besoin d’une licence pour la production ?** Une licence commerciale est requise pour une utilisation autre que l’évaluation.  
- **Quelle version de Java est prise en charge ?** Java 8 et plus récent.

## Qu’est‑ce que l’ajustement du contraste et pourquoi est‑il important ?
L’ajustement du contraste améliore la distinction visuelle entre les structures anatomiques, aidant les radiologues à repérer les anomalies plus rapidement. Dans un flux de travail DICOM, ajuster le contraste avant la conversion garantit que la sortie BMP conserve la qualité diagnostique nécessaire pour les rapports ou l’archivage.

## Prérequis
Avant de plonger dans le code, assurez‑vous que vous avez :

1. **Aspose.Imaging for Java** – téléchargez‑le depuis le site officiel [here](https://releases.aspose.com/imaging/java/).  
2. **Java Development Environment** – JDK 8+ et votre IDE préféré (IntelliJ, Eclipse, VS Code, etc.).  
3. **A DICOM Image** – tout fichier .dcm que vous souhaitez améliorer ; des fichiers d’exemple sont disponibles en ligne ou vous pouvez utiliser vos propres données cliniques.

## Importer les packages
Ces importations vous donnent accès aux fonctionnalités de gestion du DICOM et d’enregistrement BMP.

```java
import com.aspose.imaging.imageoptions.BmpOptions;
import com.aspose.imaging.Image;
import com.aspose.imaging.fileformats.dicom.DicomImage;
import java.io.File;
import java.io.FileInputStream;
import java.io.IOException;
```

## Comment ajuster le contraste dans les images DICOM

Voici le flux de travail complet, étape par étape. Chaque étape est expliquée en termes simples afin que vous puissiez suivre même si vous débutez avec Aspose.Imaging.

### Étape 1 : Spécifier les chemins de fichiers
Définissez l’emplacement du DICOM d’entrée et le chemin de sortie BMP souhaité. Remplacez le texte de substitution par le répertoire réel sur votre machine.

```java
String dataDir = "Your Document Directory" + "dicom/";
String inputFile = dataDir + "image.dcm";
String outputFile = "Your Document Directory" + "AdjustingContrast_out.bmp";
```

### Étape 2 : Charger l’image DICOM
Nous ouvrons le fichier DICOM à l’aide d’un `FileInputStream`. Le bloc `try‑with‑resources` garantit que le flux est fermé automatiquement.

```java
File file = new File(inputFile);

try (FileInputStream fis = new FileInputStream(file)) {
    try (DicomImage image = (DicomImage) Image.load(fis)) {
        // All further processing happens inside this block
    }
} catch (IOException ex) {
    Logger.println(ex.getMessage());
    ex.printStackTrace();
}
```

### Étape 3 : Ajuster le contraste
À l’intérieur du bloc `try` interne, appelez `adjustContrast`. La valeur peut varier de **‑100** (diminuer) à **+100** (augmenter). Dans cet exemple, nous augmentons le contraste de 50 unités.

```java
image.adjustContrast(50);
```

### Étape 4 : Convertir le DICOM en BMP et enregistrer l’image
Après avoir ajusté le contraste, nous créons une instance `BmpOptions` et enregistrons le résultat sous forme de fichier BMP. Cette étape **convertit le DICOM en BMP**, vous offrant un format raster largement supporté.

```java
image.save(outputFile, new BmpOptions());
```

## Problèmes courants et astuces
- **Invalid DICOM file** – Assurez‑vous que le fichier .dcm n’est pas compressé avec une syntaxe de transfert non prise en charge. Aspose.Imaging prend en charge la plupart des encodages DICOM standards.  
- **Contrast value out of range** – Les valeurs au‑delà de ±100 sont limitées ; choisissez un nombre adapté à l’histogramme de l’image.  
- **Memory usage** – Les séries DICOM volumineuses peuvent consommer beaucoup de RAM. Traitez une tranche à la fois si vous rencontrez `OutOfMemoryError`.

## Conclusion
Vous avez maintenant appris **comment ajuster le contraste** dans les images DICOM en utilisant Aspose.Imaging pour Java et comment **convertir le DICOM en BMP** pour les tâches en aval. Ce flux de travail est rapide, fiable, et peut être intégré à des pipelines d’imagerie médicale plus vastes, que vous construisiez un visualiseur PACS, un outil de recherche ou un système de génération de rapports automatisé.

Aspose.Imaging pour Java abstrait la gestion du DICOM de bas niveau, vous permettant de vous concentrer sur la valeur clinique de vos images.

## Questions fréquentes
**Q: Qu’est‑ce que le DICOM et pourquoi est‑il la norme en imagerie médicale ?**  
A: DICOM (Digital Imaging and Communications in Medicine) est le format universel pour stocker, transmettre et partager les images médicales, garantissant l’interopérabilité entre les appareils et les institutions.

**Q: Puis‑je ajuster la luminosité en même temps que le contraste ?**  
A: Oui, la méthode `adjustBrightness(int value)` fonctionne de manière similaire et peut être enchaînée avant l’enregistrement.

**Q: Aspose.Imaging prend‑il en charge d’autres formats de sortie en plus du BMP ?**  
A: Absolument – vous pouvez exporter en PNG, JPEG, TIFF, et bien d’autres en utilisant la classe `*Options` correspondante.

**Q: Une licence commerciale est‑elle requise pour une utilisation en production ?**  
A: Oui. Vous pouvez acheter une licence [here](https://purchase.aspose.com/buy) ou obtenir une licence d’évaluation temporaire [here](https://purchase.aspose.com/temporary-license/).

**Q: Où puis‑je trouver plus d’aide et d’exemples ?**  
A: Le forum communautaire Aspose.Imaging pour Java fournit une documentation exhaustive et des exemples de code : [Aspose.Imaging for Java forum](https://forum.aspose.com/).

---

**Dernière mise à jour :** 2026-01-12  
**Testé avec :** Aspose.Imaging for Java 24.11  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}