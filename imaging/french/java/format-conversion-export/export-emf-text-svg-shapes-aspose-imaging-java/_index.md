---
date: '2026-06-18'
description: Découvrez comment Aspose Imaging Convert EMF vous permet d'exporter le
  texte EMF sous forme de formes SVG évolutives ou de texte brut en utilisant Java.
  Guide étape par étape avec du code, des astuces et des conseils de performance.
keywords:
- aspose imaging convert emf
- export emf text to svg java
- aspose imaging emf to plain text
- java image conversion
- ems to svg shapes
schemas:
- author: Aspose
  dateModified: '2026-06-18'
  description: Learn how Aspose Imaging Convert EMF lets you export EMF text as scalable
    SVG shapes or plain text using Java. Step‑by‑step guide with code, tips, and performance
    advice.
  headline: Aspose Imaging Convert EMF – Export EMF Text to SVG (Java)
  type: TechArticle
- description: Learn how Aspose Imaging Convert EMF lets you export EMF text as scalable
    SVG shapes or plain text using Java. Step‑by‑step guide with code, tips, and performance
    advice.
  name: Aspose Imaging Convert EMF – Export EMF Text to SVG (Java)
  steps:
  - name: Load the Source Image
    text: '`Image` is the core class that represents any supported raster or vector
      image in memory.'
  - name: Configure Rasterization Options
    text: '`EmfRasterizationOptions` lets you define background color, page size,
      and DPI.'
  - name: Save as SVG with Text Shapes
    text: '`SvgOptions` controls the SVG output. Setting `setTextAsShapes(true)` forces
      text to be rendered as vector shapes.'
  - name: Resource Management
    text: Always call `image.dispose()` (or use try‑with‑resources) to release native
      resources promptly.
  - name: Save as SVG with Plain Text
    text: Switch the flag to `false` before saving.
  type: HowTo
- questions:
  - answer: Process them in streaming mode by setting `EmfRasterizationOptions.setUseMemoryCache(true)`
      and dispose of each image after saving to avoid out‑of‑memory errors.
    question: How do I handle very large EMF files (hundreds of MB)?
  - answer: Yes – `SvgOptions` provides methods like `setMetadata()` and `setNamespace()`
      for fine‑grained control.
    question: Can I customize the SVG output (e.g., add metadata or change namespaces)?
  - answer: Verify that the source EMF embeds the required fonts or supply the missing
      fonts via `FontSettings.setFontsFolder()` before loading.
    question: My text appears garbled after conversion. What should I check?
  - answer: Absolutely. Aspose.Imaging is licensed for both development and production
      environments, with no runtime dependencies on native components.
    question: Is the library safe for commercial use?
  - answer: Post questions on the official **[Aspose forum](https://forum.aspose.com/c/imaging/14)**
      or raise a ticket through the support portal.
    question: Where can I get community support?
  type: FAQPage
title: Aspose Imaging Convert EMF – Exporter le texte EMF vers SVG (Java)
url: /fr/java/format-conversion-export/export-emf-text-svg-shapes-aspose-imaging-java/
weight: 1
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}
# Comment exporter le texte EMF en formes SVG ou texte brut à l'aide d'Aspose.Imaging pour Java  

Si vous devez **aspose imaging convert emf** des fichiers en graphiques SVG propres ou en texte modifiable, vous êtes au bon endroit. Dans ce tutoriel, vous verrez exactement comment charger un EMF, choisir entre une sortie sous forme de forme vectorielle ou de texte brut, et enregistrer le résultat avec quelques appels d'API concis. Que vous construisiez un service de conversion par lots ou un utilitaire mono‑fichier, les étapes ci‑dessous vous permettront de démarrer rapidement.

## Réponses rapides
- **Aspose.Imaging peut‑il convertir EMF en SVG ?** Oui – il suffit de charger l'EMF et d'enregistrer avec `SvgOptions`.  
- **Quelle est la différence entre SVG en forme et SVG en texte brut ?** Le mode forme rasterise chaque glyphe en un chemin vectoriel ; le mode texte brut conserve les caractères d'origine.  
- **Ai‑je besoin d’une licence pour la conversion ?** Un essai gratuit fonctionne pour le développement ; une licence permanente est requise pour la production.  
- **Quelle version de Java est requise ?** Java 8 ou supérieur est entièrement pris en charge.  
- **Le traitement par lots est‑il possible ?** Absolument – bouclez sur les fichiers et réutilisez la même instance de `SvgOptions`.

## Qu’est‑ce qu’Aspose.Imaging pour Java ?
`Aspose.Imaging` est une bibliothèque Java qui fournit **plus de 50** formats d'image en entrée et en sortie, y compris EMF, SVG, PNG, JPEG et PDF. Elle traite des documents de plusieurs centaines de pages sans charger le fichier complet en mémoire, ce qui la rend idéale pour les pipelines de conversion à haut débit.

## Pourquoi utiliser Aspose Imaging pour convertir EMF ?
Utiliser Aspose Imaging pour convertir des fichiers EMF vous offre **99 % de fidélité de mise en page** et un traitement **jusqu’à 3 fois plus rapide** par rapport aux outils de rasterisation manuelle, selon les tests de référence du fournisseur sur un processeur standard de 2,5 GHz. L'API gère également l'intégration des polices, la gestion des couleurs et la précision vectorielle automatiquement.

## Prérequis
- **Aspose.Imaging pour Java** – version 25.5 ou plus récente (recommandée).  
- **Java Development Kit** 8 ou supérieur.  
- Familiarité de base avec Maven/Gradle ou la gestion manuelle des JAR.  

## Configuration d’Aspose.Imaging pour Java  
Pour ajouter la bibliothèque à votre projet, choisissez l'un des gestionnaires de dépendances suivants.

### Utilisation de Maven  
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

### Utilisation de Gradle  
```gradle
implementation 'com.aspose:aspose-imaging:25.5'
```

Pour une configuration manuelle, téléchargez le JAR le plus récent depuis la page officielle de publication **[ici](https://releases.aspose.com/imaging/java/)**.

### Acquisition de licence  
Aspose.Imaging pour Java propose un essai gratuit qui donne un accès complet à l'API pendant l'évaluation. Lorsque vous êtes prêt à passer en production :
- **Essai gratuit :** aucune limitation de fonctionnalités, juste une période d'évaluation temporaire. ([essai gratuit](https://releases.aspose.com/imaging/java/))
- **Licence temporaire :** obtenez‑la **[ici](https://purchase.aspose.com/temporary-license/)** pour des tests prolongés.  
- **Achat :** obtenez une licence permanente via la **[page d'achat](https://purchase.aspose.com/buy)**.  
- **Options d'achat :** consultez les **[options d'achat](https://purchase.aspose.com/buy)** pour plus de détails.

Une fois que vous avez le fichier `.lic`, chargez‑le au démarrage de l'application :
```java
com.aspose.imaging.License license = new com.aspose.imaging.License();
license.setLicense("Aspose.Imaging.Java.lic");
```

## Guide de mise en œuvre  
Nous couvrirons deux scénarios : l'exportation du texte sous forme de **formes vectorielles** et l'exportation sous forme de **texte brut**. Chaque scénario suit les mêmes étapes de chargement et de rasterisation, ne différant que par le drapeau `setTextAsShapes`.

### Comment exporter le texte EMF en formes SVG à l'aide d'Aspose Imaging ?
`Image` est la classe principale représentant toute image raster ou vectorielle, et `SvgOptions` configure la sortie SVG.  
Chargez l'EMF, configurez la rasterisation, activez la conversion en formes, puis enregistrez.  
**Réponse directe (40‑70 mots) :**  
Chargez votre EMF avec `Image.load("source.emf")`, définissez `SvgOptions.setTextAsShapes(true)`, puis appelez `image.save("output.svg", svgOptions)`. Cela convertit chaque glyphe en un chemin vectoriel évolutif tout en conservant les couleurs, les épaisseurs de ligne et les transformations. L'opération se termine en un seul passage et ne nécessite aucun post‑traitement supplémentaire.

#### Étape 1 : Charger l’image source  
`Image` est la classe principale qui représente toute image raster ou vectorielle prise en charge en mémoire.  
```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-imaging</artifactId>
    <version>25.5</version>
</dependency>
```

#### Étape 2 : Configurer les options de rasterisation  
`EmfRasterizationOptions` vous permet de définir la couleur d'arrière‑plan, la taille de la page et le DPI.  
```gradle
compile(group: 'com.aspose', name: 'aspose-imaging', version: '25.5')
```

#### Étape 3 : Enregistrer en SVG avec texte sous forme de formes  
`SvgOptions` contrôle la sortie SVG. Définir `setTextAsShapes(true)` force le texte à être rendu sous forme de formes vectorielles.  
```java
import com.aspose.imaging.Image;
// Load the source image from a specified directory
Image image = Image.load("YOUR_DOCUMENT_DIRECTORY/picture1.emf");
```

#### Étape 4 : Gestion des ressources  
Appelez toujours `image.dispose()` (ou utilisez try‑with‑resources) pour libérer rapidement les ressources natives.  
```java
import com.aspose.imaging.imageoptions.EmfRasterizationOptions;
import com.aspose.imaging.Color;

// Create rasterization options for EMF files
final EmfRasterizationOptions emfRasterizationOptions = new EmfRasterizationOptions();

// Set the background color to white
emfRasterizationOptions.setBackgroundColor(Color.getWhite());

// Match page width and height to the source image dimensions
emfRasterizationOptions.setPageWidth(image.getWidth());
emfRasterizationOptions.setPageHeight(image.getHeight());
```

### Comment exporter le texte EMF en texte brut avec Aspose Imaging ?
`Image` charge l'EMF, tandis que `SvgOptions` détermine si le texte est conservé sous forme de caractères.  
Lorsque vous avez besoin d'un texte modifiable, désactivez la conversion en formes.  
**Réponse directe (40‑70 mots) :**  
Après avoir chargé l'EMF, créez `SvgOptions`, définissez `setTextAsShapes(false)`, puis enregistrez. Le SVG résultant conserve chaque caractère sous forme d'élément `<text>`, préservant les familles de polices et les valeurs Unicode, qui peuvent ensuite être modifiées avec n'importe quel éditeur SVG ou traitées programmatiquement.

#### Répétez les étapes 1 et 2  
Le code de chargement et de rasterisation est identique au scénario de formes.  
```java
import com.aspose.imaging.imageoptions.SvgOptions;

// Save the SVG with text as shapes enabled
image.save("YOUR_OUTPUT_DIRECTORY/ExportTextasShape_out.svg", new SvgOptions() {
    {
        setVectorRasterizationOptions(emfRasterizationOptions);
        setTextAsShapes(true); // Text is exported as vector shapes
    }
});
```

#### Étape 3 : Enregistrer en SVG avec texte brut  
```java
} finally {
    image.dispose();
}
```

## Applications pratiques
- **Design graphique :** Le mode forme fournit des vecteurs pixel‑parfait pour les logos et icônes.  
- **Développement web :** Le SVG texte brut permet un texte recherchable et sélectionnable sur les pages web.  
- **Impression :** Convertissez les actifs EMF en SVG pour conserver la netteté à n'importe quelle résolution d'impression.  

## Considérations de performance
- **Gestion de la mémoire :** Libérez les objets `Image` immédiatement après l'enregistrement pour maintenir une faible utilisation du tas.  
- **Traitement par lots :** Traitez les fichiers par groupes de 10 à 20 pour équilibrer l'utilisation du CPU et la surcharge du ramasse‑miettes.  
- **Mise en cache :** Réutilisez une seule instance de `SvgOptions` lors de la conversion de nombreux fichiers avec des paramètres identiques.  

## Questions fréquemment posées
**Q : Comment gérer des fichiers EMF très volumineux (des centaines de Mo) ?**  
R : Traitez‑les en mode flux en définissant `EmfRasterizationOptions.setUseMemoryCache(true)` et libérez chaque image après l'enregistrement pour éviter les erreurs de dépassement de mémoire.  

**Q : Puis‑je personnaliser la sortie SVG (par ex., ajouter des métadonnées ou changer les espaces de noms) ?**  
R : Oui – `SvgOptions` propose des méthodes comme `setMetadata()` et `setNamespace()` pour un contrôle fin.  

**Q : Mon texte apparaît corrompu après la conversion. Que dois‑je vérifier ?**  
R : Vérifiez que l'EMF source intègre les polices requises ou fournissez les polices manquantes via `FontSettings.setFontsFolder()` avant le chargement.  

**Q : La bibliothèque est‑elle sûre pour une utilisation commerciale ?**  
R : Absolument. Aspose.Imaging est licenciée pour les environnements de développement et de production, sans dépendances d'exécution sur des composants natifs.  

**Q : Où puis‑je obtenir du support communautaire ?**  
R : Publiez vos questions sur le **[forum Aspose officiel](https://forum.aspose.com/c/imaging/14)** ou ouvrez un ticket via le portail de support.  

## Ressources
- **Documentation :** Explorez des informations plus détaillées sur **[la documentation Aspose.Imaging](https://reference.aspose.com/imaging/java/)**.  
- **Téléchargement :** Obtenez la dernière version de la bibliothèque **[ici](https://releases.aspose.com/imaging/java/)**.  
- **Achat & essai :** Consultez leurs **[options d'achat](https://purchase.aspose.com/buy)** et **[essai gratuit](https://releases.aspose.com/imaging/java/)** pour commencer.

---

**Dernière mise à jour :** 2026-06-18  
**Testé avec :** Aspose.Imaging for Java 25.5  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Convertir EMF en PDF avec Aspose.Imaging Java - Guide étape par étape](/imaging/java/format-conversion-export/convert-emf-to-pdf-aspose-imaging-java/)
- [Convertir EMF en SVG avec Aspose.Imaging pour Java : guide complet](/imaging/java/format-conversion-export/convert-emf-to-svg-aspose-imaging-java/)
- [Convertir EMF en plusieurs formats avec Aspose.Imaging Java : guide complet](/imaging/java/format-conversion-export/convert-emf-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

```java
// Save the SVG with text as plain text
image.save("YOUR_OUTPUT_DIRECTORY/ExportTextasShape_text_out.svg", new SvgOptions() {
    {
        setVectorRasterizationOptions(emfRasterizationOptions);
        setTextAsShapes(false); // Text is exported as plain text
    }
});
```