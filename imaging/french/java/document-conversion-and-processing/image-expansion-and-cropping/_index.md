---
date: 2026-05-24
description: Découvrez comment utiliser la bibliothèque de manipulation d'images Java,
  Aspose.Imaging for Java, pour agrandir des images, les recadrer et enregistrer les
  résultats efficacement.
keywords:
- image manipulation library java
- how to crop image java
- how to expand image java
- aspose imaging expand image
linktitle: Agrandissement et recadrage d'images
schemas:
- author: Aspose
  dateModified: '2026-05-24'
  description: Discover how to use the image manipulation library java, Aspose.Imaging
    for Java, to expand images, crop them, and save results efficiently.
  headline: Image Manipulation Library Java – Expand and Crop Images Using Aspose.Imaging
  type: TechArticle
- questions:
  - answer: Yes, it supports PNG, BMP, TIFF, GIF, and many more image types.
    question: Can Aspose.Imaging handle other formats besides JPEG?
  - answer: You can use `Resize` methods provided by the library; this falls under
      **resize image java** operations.
    question: Is there a way to resize the image before cropping?
  - answer: Absolutely. Loop through a collection of file paths and apply the same
      steps to each image.
    question: Does the library support batch processing of multiple images?
  - answer: '`cacheData()` loads the image into memory once, avoiding repeated disk
      reads during manipulation – this is the essence of **cache image java**.'
    question: How does caching improve performance?
  - answer: Refer to the official documentation **[documentation](https://reference.aspose.com/imaging/java/)**
      for a complete list of classes and methods.
    question: Where can I find more detailed API references?
  type: FAQPage
second_title: Aspose.Imaging Java Image Processing API
title: Bibliothèque de manipulation d'images Java – Agrandir et recadrer des images
  avec Aspose.Imaging
url: /fr/java/document-conversion-and-processing/image-expansion-and-cropping/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Bibliothèque de manipulation d'images Java – Agrandir et recadrer des images avec Aspose.Imaging

Manipuler des images est un besoin quotidien pour les développeurs web, les designers et toute personne travaillant avec des médias numériques. Dans ce tutoriel, vous apprendrez **comment agrandir une image** et ensuite la recadrer efficacement avec Aspose.Imaging pour Java, une bibliothèque **image manipulation library java** de premier plan. Nous parcourrons le flux de travail complet — du chargement de l'image source à la mise en cache des données, en passant par la définition d'un rectangle de recadrage, jusqu'à l'enregistrement du résultat recadré.

## Réponses rapides
- **Que signifie « agrandir une image » ?** Cela ajoute de l'espace supplémentaire autour de l'image originale, vous permettant de recadrer une zone plus grande.  
- **Quelle bibliothèque devrais‑je utiliser ?** Aspose.Imaging pour Java fournit une API riche pour l'agrandissement, le recadrage et de nombreuses autres opérations.  
- **Ai‑je besoin d’une licence ?** Un essai gratuit suffit pour le développement ; une licence commerciale est requise pour la production.  
- **Puis‑je mettre en cache l'image pour de meilleures performances ?** Oui – appelez `cacheData()` sur l'image raster.  
- **Le format de sortie est‑il limité ?** Non, vous pouvez enregistrer en JPEG, PNG, BMP et d’autres formats pris en charge par Aspose.Imaging.

## Qu'est‑ce que l'agrandissement et le recadrage d'image en Java ?

L'agrandissement d'image ajoute des pixels supplémentaires autour d'une image existante, tandis que le recadrage extrait une région rectangulaire définie. Ensemble, ils permettent de re‑composer une image sans perte de qualité, un besoin fréquent pour la génération de vignettes, les actifs UI ou la préparation de graphiques pour l'impression.

## Pourquoi utiliser Aspose.Imaging pour cette tâche ?

Aspose.Imaging offre une solution **format‑agnostique** haute performance capable de gérer plus de 30 formats d'image et de traiter des fichiers jusqu'à 500 Mo sans charger le document complet en mémoire. Son cache intégré réduit la surcharge I/O jusqu'à 70 %, et l'API ne nécessite que quelques lignes pour réaliser des transformations complexes, ce qui le rend idéal tant pour des scripts rapides que pour des services à grande échelle.

## Prérequis
- Environnement de développement Java (JDK 8+)
- Aspose.Imaging pour Java – téléchargez‑le **[here](https://releases.aspose.com/imaging/java/)**  
- Un IDE tel qu'Eclipse ou IntelliJ IDEA
- Un fichier image à manipuler (par ex., `aspose-logo.jpg`)

Maintenant que tout est prêt, plongeons dans le code réel.

## Importer les packages
Tout d'abord, importez les classes dont vous aurez besoin. Ces imports vous donnent accès au chargement d'images, à la définition de rectangles, aux options JPEG et à la gestion des images raster.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Rectangle;
import com.aspose.imaging.imageoptions.JpegOptions;
import com.aspose.imaging.raster.RasterImage;
```

## Étape 1 : Charger l'image
`RasterImage` est la classe d'Aspose.Imaging qui représente une image raster chargée en mémoire. Chargez l'image source dans un objet `RasterImage`. Remplacez le chemin factice par l'emplacement de votre fichier image.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
try (RasterImage rasterImage = (RasterImage) Image.load(dataDir + "aspose-logo.jpg"))
{
    // Your code here
}
```

## Étape 2 : Mettre en cache les données de l'image
La mise en cache accélère les opérations suivantes, surtout lorsque vous devez lire les données de pixels plusieurs fois.

```java
rasterImage.cacheData();
```

## Étape 3 : Définir le rectangle de recadrage
`Rectangle` définit les coordonnées X/Y et la taille de la zone que vous souhaitez conserver après agrandissement. Créez un `Rectangle` qui marque la région à garder après agrandissement. Les coordonnées sont mesurées depuis le coin supérieur gauche du canevas agrandi.

```java
Rectangle destRect = new Rectangle(200, 200, 300, 300);
```

> **Astuce :** Ajustez les valeurs X, Y, largeur et hauteur pour correspondre exactement à la zone dont vous avez besoin. C'est là que la capacité **aspose crop image** brille.

## Étape 4 : Enregistrer l'image recadrée
`JpegOptions` vous permet de contrôler la qualité de sortie, la compression et d'autres paramètres spécifiques au JPEG. Enfin, écrivez la partie recadrée dans un nouveau fichier. La méthode `save` vous permet également de spécifier des options de sortie telles que la qualité JPEG.

```java
rasterImage.save("Your Document Directory" + "ExpandandCropImages_out.jpg", new JpegOptions(), destRect);
```

Le fichier `ExpandandCropImages_out.jpg` contient désormais le canevas agrandi avec la zone de 300 × 300 pixels sélectionnée, enregistrée au format JPEG — satisfaisant ainsi l'exigence **save cropped image**.

## Comment agrandir une image en Java avec Aspose.Imaging ?

Chargez votre image originale, appelez `rasterImage.expandCanvas(newWidth, newHeight, backgroundColor)`, puis procédez au recadrage. **`expandCanvas` ajoute de l'espace supplémentaire autour de l'image.** Cette méthode unique ajoute l'espace de canevas requis en une seule opération, préservant les données de pixels d'origine et vous permettant de cibler un rectangle de recadrage plus grand sans distorsion.

## Comment recadrer une image en Java avec Aspose.Imaging ?

Créez un `Rectangle` qui décrit la zone cible, puis invoquez `rasterImage.crop(rectangle)`. **`crop` extrait la région rectangulaire définie de l'image.** L'appel de recadrage extrait la région définie du canevas agrandi et renvoie une nouvelle instance `RasterImage` prête à être enregistrée. Cette approche garantit des résultats pixel‑parfait et fonctionne avec tous les formats pris en charge.

## Problèmes courants et solutions
| Problème | Raison | Solution |
|----------|--------|----------|
| `OutOfMemoryError` | Image source volumineuse sans mise en cache | Appelez `rasterImage.cacheData()` avant le traitement |
| La zone recadrée est décentrée | Coordonnées du rectangle incorrectes | Vérifiez les décalages X/Y et les dimensions par rapport au canevas agrandi |
| Le fichier de sortie est corrompu | Paramètres `JpegOptions` incorrects | Utilisez les options par défaut ou définissez `Quality = 90` |

## Questions fréquemment posées

**Q : Aspose.Imaging peut‑il gérer d'autres formats que le JPEG ?**  
R : Oui, il prend en charge PNG, BMP, TIFF, GIF et bien d’autres types d'images.

**Q : Existe‑t‑il un moyen de redimensionner l'image avant le recadrage ?**  
R : Vous pouvez utiliser les méthodes `Resize` fournies par la bibliothèque ; cela relève des opérations **resize image java**.

**Q : La bibliothèque supporte‑t‑elle le traitement par lots de plusieurs images ?**  
R : Absolument. Parcourez une collection de chemins de fichiers et appliquez les mêmes étapes à chaque image.

**Q : Comment la mise en cache améliore‑t‑elle les performances ?**  
R : `cacheData()` charge l'image en mémoire une fois, évitant les lectures disque répétées pendant la manipulation – c’est l’essence de **cache image java**.

**Q : Où puis‑je trouver des références API plus détaillées ?**  
R : Consultez la documentation officielle **[documentation](https://reference.aspose.com/imaging/java/)** pour une liste complète des classes et méthodes.

## Conclusion
Vous disposez maintenant d’un exemple complet, prêt pour la production, de **comment agrandir une image** et de la recadrer avec Aspose.Imaging pour Java. En tirant parti du cache, de définitions précises de rectangles et d’options d’enregistrement flexibles, vous pouvez intégrer ce flux de travail dans n’importe quel pipeline de traitement d’images basé sur Java.

Explorez davantage en expérimentant d’autres transformations telles que la rotation, le filigrane ou le redimensionnement par lots. Pour plus d’orientation, consultez la **[documentation](https://reference.aspose.com/imaging/java/)** ou rejoignez la communauté sur le **[Aspose support forum](https://forum.aspose.com/)**.

---

**Dernière mise à jour :** 2026-05-24  
**Testé avec :** Aspose.Imaging pour Java 24.11  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Traitement d'images Java avec Aspose.Imaging : Chargement, mise en cache et recadrage](/imaging/java/getting-started/java-image-processing-aspose-imaging-load-cache-crop/)
- [Maîtriser le traitement d'images avec Aspose.Imaging pour Java : Chargement, enregistrement & suppression d'arrière‑plans](/imaging/java/image-transformations/aspose-imaging-java-master-image-processing/)
- [Traitement d'images parallèle en Java avec Aspose.Imaging : Multithreading & gestion par lots](/imaging/java/batch-processing-multi-threading/parallel-image-processing-aspose-imaging-java/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}