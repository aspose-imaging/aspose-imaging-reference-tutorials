---
date: '2026-06-28'
description: Apprenez à convertir ODP en PNG avec Aspose.Imaging for Java, à définir
  des polices personnalisées et à désactiver les polices système pour un rendu précis.
keywords:
- how to convert odp
- maven aspose imaging
- aspose imaging license
- disable system fonts
- java convert presentation image
schemas:
- author: Aspose
  dateModified: '2026-06-28'
  description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  headline: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts
    & Export Guide
  type: TechArticle
- description: Learn how to convert ODP to PNG using Aspose.Imaging for Java, set
    custom fonts, and disable system fonts for accurate rendering.
  name: How to Convert ODP to PNG with Aspose.Imaging for Java – Custom Fonts & Export
    Guide
  steps:
  - name: '**Free Trial** – No license required, limited features.'
    text: '**Free Trial** – No license required, limited features.'
  - name: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
    text: '**Temporary License** – Request one on the [Aspose website](https://purchase.aspose.com/temporary-license/).'
  - name: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Purchase** – Buy a subscription or perpetual license from [Aspose purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
    text: '**Brand‑consistent slide decks** – Export presentations as PNGs for web
      publishing while preserving corporate fonts.'
  - name: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
    text: '**Automated report generation** – Convert each slide to an image for inclusion
      in PDF reports or email newsletters.'
  - name: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
    text: '**Legacy archive creation** – Store ODP content as PNGs to guarantee future
      accessibility without needing ODP viewers.'
  type: HowTo
- questions:
  - answer: Aspose.Imaging for Java works with JDK 8 and newer; JDK 11 is recommended
      for long‑term support.
    question: What is the minimum Java version required?
  - answer: Yes, set `rasterizationOptions.setPageNumber(specificSlideIndex)` before
      calling `save`.
    question: Can I convert only selected slides?
  - answer: Load the file with `LoadOptions` that includes the password, then proceed
      with the same font settings.
    question: How do I handle password‑protected ODP files?
  - answer: It marginally improves speed because the engine skips the lookup of system
      fonts, especially noticeable on machines with large font collections.
    question: Does disabling system fonts affect performance?
  - answer: Explore the official [Aspose.Imaging documentation](https://reference.aspose.com/imaging/java/)
      for additional scenarios such as batch conversion and image transformations.
    question: Where can I find more code samples?
  type: FAQPage
title: Comment convertir ODP en PNG avec Aspose.Imaging for Java – Guide des polices
  personnalisées et de l'exportation
url: /fr/java/format-conversion-export/export-odp-to-png-aspose-imaging-java-custom-fonts/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Comment convertir ODP en PNG avec Aspose.Imaging pour Java – Polices personnalisées et guide d'exportation

Dans les applications Java modernes, la conversion de fichiers OpenDocument Presentation (ODP) en images PNG de haute qualité est une exigence courante—surtout lorsqu'il faut préserver l'identité visuelle grâce à des polices personnalisées. Ce tutoriel montre **comment convertir ODP** en PNG avec Aspose.Imaging pour Java, vous guide dans la configuration d'un dossier de polices personnalisées, la désactivation des polices de secours du système, et le réglage fin des options de rasterisation pour des performances optimales.

**Ce que vous apprendrez**
- Comment définir un répertoire de polices personnalisé pour la conversion ODP.  
- Comment désactiver les polices alternatives du système afin que seules vos polices choisies soient utilisées.  
- Comment exporter un fichier ODP en PNG avec des dimensions précises et des paramètres de police.  
- Conseils pour améliorer la vitesse et l'utilisation de la mémoire lors du traitement de présentations volumineuses.

## Réponses rapides
- **Puis-je utiliser Maven pour ajouter Aspose.Imaging ?** Oui, ajoutez la dépendance Maven et exécutez `mvn install`.  
- **Ai-je besoin d'une licence pour la production ?** Une licence valide d'Aspose.Imaging est requise pour une utilisation illimitée.  
- **Mes polices personnalisées seront‑elles respectées ?** Définissez le dossier de polices et désactivez les alternatives système pour les appliquer.  
- **Quels formats d'image sont pris en charge ?** Aspose.Imaging prend en charge plus de 120 formats raster et vectoriels, dont PNG, JPEG, TIFF et WebP.  
- **L'API est‑elle thread‑safe ?** Oui, la plupart des classes Aspose.Imaging sont sûres pour une utilisation concurrente lorsque vous créez des instances séparées par thread.

## Qu’est‑ce que « how to convert odp » ?
*« How to convert odp »* désigne le processus de transformation d'un fichier OpenDocument Presentation en un autre format—généralement PNG—tout en préservant la mise en page, les polices et la fidélité visuelle. Aspose.Imaging pour Java fournit un flux de travail à méthode unique qui gère cette conversion sans nécessiter d'outils externes, permettant aux développeurs d'intégrer la conversion directement dans leurs applications avec un code minimal.

## Pourquoi utiliser Aspose.Imaging pour Java ?
Aspose.Imaging prend en charge **plus de 120 formats de sortie** et peut rasteriser des fichiers ODP multi‑pages sans charger le document complet en mémoire, réduisant l'utilisation maximale de RAM jusqu'à 70 % sur les présentations volumineuses. La bibliothèque offre également une gestion intégrée des polices, éliminant le besoin de moteurs de rendu tiers.

## Prérequis
- **Bibliothèques** : Aspose.Imaging pour Java ≥ 25.5.  
- **JDK** : Version 8 ou plus récente.  
- **IDE** : IntelliJ IDEA, Eclipse, ou tout éditeur compatible Java.  
- **Connaissances de base** : Java I/O, programmation orientée objet et concepts d'image.

## Instructions d'installation

### Maven
Ajoutez la dépendance suivante à votre `pom.xml` et exécutez `mvn clean install` :

```xml
<dependency>
  <groupId>com.aspose</groupId>
  <artifactId>aspose-imaging</artifactId>
  <version>25.5</version>
</dependency>
```

### Gradle
Incluez la bibliothèque dans votre fichier `build.gradle` et rafraîchissez le projet :

```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

### Téléchargement direct
Téléchargez le dernier JAR depuis [versions d'Aspose.Imaging pour Java](https://releases.aspose.com/imaging/java/).

## Étapes d'obtention de licence
Pour débloquer toutes les fonctionnalités, appliquez une licence temporaire ou permanente :

1. **Essai gratuit** – Aucune licence requise, fonctionnalités limitées.  
2. **Licence temporaire** – Demandez‑en une sur le [site Aspose](https://purchase.aspose.com/temporary-license/).  
3. **Achat** – Achetez un abonnement ou une licence perpétuelle depuis la [page d'achat Aspose](https://purchase.aspose.com/buy).

Initialisez la bibliothèque avec votre fichier de licence :

```java
License license = new License();
license.setLicense("path/to/your/license/file");
```

## Comment définir un répertoire de polices personnalisé pour la conversion ODP ?
`FontSettings` est une classe qui gère les ressources de polices pour Aspose.Imaging. Chargez vos polices personnalisées avant le début de tout traitement d'image. Cela garantit que chaque diapositive utilise exactement les polices que vous fournissez.

Définissez le chemin du dossier de polices en utilisant `FontSettings` d'Aspose.Imaging :

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.examples.Utils;

  String dataDir = Utils.getSharedDataDir() + "otg/";
  FontSettings.setFontsFolder(Path.combine(dataDir, "fonts"));
  ```

*Ancre de définition* : `FontSettings.setFontsFolder` indique à Aspose.Imaging où rechercher les polices TrueType et OpenType sur le système de fichiers.

## Comment désactiver les polices alternatives du système lors de la conversion ODP ?
Désactiver les alternatives système oblige le moteur de rendu à ignorer les polices installées sur le système d'exploitation, garantissant que seules les polices que vous fournissez sont utilisées. Cela élimine les substitutions de polices inattendues qui peuvent modifier l'apparence visuelle de vos diapositives.

Désactivez les alternatives système avec l'appel suivant :

```java
  import com.aspose.imaging.FontSettings;

  FontSettings.setGetSystemAlternativeFont(false);
  ```

*Ancre de définition* : `FontSettings.setGetSystemAlternativeFont(false)` force le moteur à n'utiliser que les polices situées dans le dossier que vous avez défini, éliminant les substitutions inattendues.

## Comment exporter un fichier ODP en PNG avec une police spécifiée ?
`RasterizationOptions` définit comment les pages vectorielles sont rasterisées en images bitmap. En combinant la configuration des polices avec les paramètres de rasterisation, vous pouvez contrôler le DPI, la couleur d'arrière‑plan et la taille de page pour chaque PNG exporté.

Implémentez la méthode d'exportation comme indiqué ci‑dessous :

```java
  import com.aspose.imaging.FontSettings;
  import com.aspose.imaging.examples.Path;
  import com.aspose.imaging.Image;
  import com.aspose.imaging.imageoptions.OdgRasterizationOptions;
  import com.aspose.imaging.imageoptions.PngOptions;

  private static void exportToPng(String filePath, String defaultFontName, String outfileName) {
      FontSettings.setDefaultFontName(defaultFontName);
      try (Image document = Image.load(filePath)) {
          PngOptions saveOptions = new PngOptions();
          
          OdgRasterizationOptions rasterizationOptions = new OdgRasterizationOptions();
          rasterizationOptions.setPageWidth(1000); // Set the page width for rendering
          rasterizationOptions.setPageHeight(1000);  // Set the page height for rendering

          saveOptions.setVectorRasterizationOptions(rasterizationOptions);
          document.save(outfileName, saveOptions);
      }
  }

  ```

*Ancre de définition* : la classe `RasterizationOptions` contrôle le DPI, la taille de page et la couleur d'arrière‑plan des fichiers PNG générés.

### Pièges courants et solutions
- **Fichiers de police manquants** – Vérifiez que chaque `.ttf` ou `.otf` référencé dans l'ODP est présent dans le dossier que vous avez défini.  
- **Chemins de fichiers incorrects** – Utilisez des chemins absolus ou résolvez les chemins relatifs par rapport à `System.getProperty("user.dir")`.  
- **Permissions insuffisantes** – Assurez‑vous que le processus Java peut lire le répertoire de polices et écrire dans le dossier de sortie.

## Applications pratiques
1. **Diapositives cohérentes avec la marque** – Exportez les présentations en PNG pour la publication web tout en préservant les polices d'entreprise.  
2. **Génération automatisée de rapports** – Convertissez chaque diapositive en image pour l'inclure dans des rapports PDF ou des newsletters par e‑mail.  
3. **Création d'archives legacy** – Stockez le contenu ODP en PNG pour garantir une accessibilité future sans nécessiter de visionneuses ODP.

## Considérations de performance
- Utilisez la dernière version d'Aspose.Imaging pour profiter des améliorations de rasterisation multithread (jusqu'à 2× plus rapide sur des CPU à 8 cœurs).  
- Encapsulez le traitement d'image dans un bloc try‑with‑resources pour garantir la libération en temps voulu des ressources natives.  
- Ajustez `RasterizationOptions` (par ex., DPI inférieur) lors du traitement de milliers de diapositives afin d'équilibrer qualité et utilisation de la mémoire.

## Questions fréquentes

**Q : Quelle est la version minimale de Java requise ?**  
R : Aspose.Imaging pour Java fonctionne avec JDK 8 et supérieur ; JDK 11 est recommandé pour le support à long terme.

**Q : Puis‑je convertir uniquement des diapositives sélectionnées ?**  
R : Oui, définissez `rasterizationOptions.setPageNumber(specificSlideIndex)` avant d'appeler `save`.

**Q : Comment gérer les fichiers ODP protégés par mot de passe ?**  
R : Chargez le fichier avec `LoadOptions` incluant le mot de passe, puis poursuivez avec les mêmes paramètres de police.

**Q : La désactivation des polices système affecte‑t‑elle les performances ?**  
R : Elle améliore légèrement la vitesse car le moteur saute la recherche des polices système, ce qui est particulièrement perceptible sur les machines disposant de grandes collections de polices.

**Q : Où puis‑je trouver plus d'exemples de code ?**  
R : Explorez la [documentation officielle d'Aspose.Imaging](https://reference.aspose.com/imaging/java/) pour des scénarios supplémentaires tels que la conversion par lots et les transformations d'images.

## Ressources supplémentaires
- [versions d'Aspose.Imaging pour Java](https://releases.aspose.com/imaging/java/)  
- [Versions d'Aspose.Imaging](https://releases.aspose.com/imaging/java/)  
- [Commencez votre essai gratuit](https://releases.aspose.com/imaging/java/)  
- [Documentation d'Aspose.Imaging](https://reference.aspose.com/imaging/java/)  
- [Forum Aspose.Imaging](https://forum.aspose.com/c/imaging/14)  
- [Acheter une licence Aspose](https://purchase.aspose.com/buy)  
- [Demander une licence temporaire](https://purchase.aspose.com/temporary-license/)  

---

**Dernière mise à jour :** 2026-06-28  
**Testé avec :** Aspose.Imaging pour Java 25.5  
**Auteur :** Aspose

## Tutoriels associés

- [Convertir ODG en PNG avec Aspose.Imaging pour Java : guide complet](/imaging/java/format-conversion-export/convert-odg-to-png-aspose-imaging-java/)
- [Conversion d'images efficace en Java avec Aspose.Imaging : guide complet](/imaging/java/format-conversion-export/mastering-image-conversion-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}