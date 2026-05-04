---
date: 2025-12-24
description: Apprenez comment agrandir une image et effectuer le recadrage d’images
  en Java avec Aspose.Imaging for Java. Suivez ce guide étape par étape pour agrandir,
  recadrer et enregistrer des images.
linktitle: Image Expansion and Cropping
second_title: Aspose.Imaging Java Image Processing API
title: Comment agrandir l'image et la recadrer avec Aspose.Imaging Java
url: /fr/java/document-conversion-and-processing/image-expansion-and-cropping/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Comment agrandir une image et la recadrer avec Aspose.Imaging Java

Manipuler des images est un besoin quotidien pour les développeurs web, les designers et toute personne travaillant avec les médias numériques. Dans ce tutoriel, vous apprendrez **comment agrandir une image** et ensuite la recadrer efficacement avec Aspose.Imaging pour Java. Nous parcourrons le flux de travail complet — du chargement de l’image source à la mise en cache des données, en passant par la définition d’un rectangle de recadrage, jusqu’à l’enregistrement du résultat recadré.

## Réponses rapides
- **Que signifie « agrandir une image » ?** Cela ajoute de l’espace supplémentaire sur le canevas autour de l’image originale, vous permettant de recadrer une zone plus grande.
- **Quelle bibliothèque dois-je utiliser ?** Aspose.Imaging pour Java fournit une API riche pour l’agrandissement d’image, le recadrage et de nombreuses autres opérations.
- **Ai‑je besoin d’une licence ?** Un essai gratuit suffit pour le développement ; une licence commerciale est requise pour une utilisation en production.
- **Puis‑je mettre en cache l’image pour de meilleures performances ?** Oui – appelez `cacheData()` sur l’image raster.
- **Le format de sortie est‑il limité ?** Non, vous pouvez enregistrer en JPEG, PNG, BMP et d’autres formats pris en charge par Aspose.Imaging.

## Qu’est‑ce que l’agrandissement et le recadrage d’image en Java ?
L’agrandissement d’image ajoute des pixels supplémentaires autour d’une image existante, tandis que le recadrage extrait une région rectangulaire définie. Ensemble, ils vous permettent de re‑cadencer une image sans perdre de qualité, une exigence courante pour la génération de vignettes, les actifs d’interface utilisateur ou la préparation de graphiques pour l’impression.

## Pourquoi utiliser Aspose.Imaging pour cette tâche ?
- **API haute performance** – la mise en cache intégrée (`cacheData`) réduit la surcharge d’E/S.
- **Indépendant du format** – fonctionne avec JPEG, PNG, BMP, TIFF, et plus encore.
- **Code simple** – quelques lignes remplacent un code natif de traitement d’image complexe.
- **Prêt pour l’entreprise** – fiable tant pour les scripts simples que pour les services à grande échelle.

## Prérequis
- Environnement de développement Java (JDK 8+)
- Aspose.Imaging pour Java – téléchargez‑le **[ici](https://releases.aspose.com/imaging/java/)**  
- Un IDE tel qu’Eclipse ou IntelliJ IDEA
- Un fichier image à utiliser (par ex., `aspose-logo.jpg`)

Une fois que tout est configuré, plongeons dans le code réel.

## Importer les packages
Tout d’abord, importez les classes dont vous avez besoin. Ces imports vous donnent accès au chargement d’image, à la définition de rectangles, aux options JPEG et à la gestion des images raster.

```java
import com.aspose.imaging.Image;
import com.aspose.imaging.Rectangle;
import com.aspose.imaging.imageoptions.JpegOptions;
import com.aspose.imaging.raster.RasterImage;
```

## Étape 1 : charger l’image
Chargez l’image source dans un objet `RasterImage`. Remplacez le chemin factice par l’emplacement de votre fichier image.

```java
String dataDir = "Your Document Directory" + "ConvertingImages/";
try (RasterImage rasterImage = (RasterImage) Image.load(dataDir + "aspose-logo.jpg"))
{
    // Your code here
}
```

## Étape 2 : mettre en cache les données de l’image
La mise en cache accélère les opérations suivantes, surtout lorsque vous lirez les données de pixels plusieurs fois.

```java
rasterImage.cacheData();
```

## Étape 3 : définir le rectangle de recadrage
Créez un `Rectangle` qui délimite la région que vous souhaitez conserver après l’agrandissement. Les coordonnées sont mesurées à partir du coin supérieur gauche du canevas agrandi.

```java
Rectangle destRect = new Rectangle(200, 200, 300, 300);
```

> **Astuce :** Ajustez les valeurs X, Y, largeur et hauteur pour correspondre exactement à la zone souhaitée. C’est ici que la capacité **aspose crop image** brille.

## Étape 4 : enregistrer l’image recadrée
Enfin, écrivez la portion recadrée dans un nouveau fichier. La méthode `save` vous permet également de spécifier des options de sortie comme la qualité JPEG.

```java
rasterImage.save("Your Document Directory" + "ExpandandCropImages_out.jpg", new JpegOptions(), destRect);
```

Le fichier `ExpandandCropImages_out.jpg` contient maintenant le canevas agrandi avec la zone de 300 × 300 pixels sélectionnée enregistrée en JPEG — répondant à l’exigence **save cropped image**.

## Problèmes courants et solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| `OutOfMemoryError` | Image source volumineuse sans mise en cache | Appelez `rasterImage.cacheData()` avant le traitement |
| La zone recadrée est décentrée | Coordonnées du rectangle incorrectes | Vérifiez les décalages X/Y et les dimensions par rapport au canevas agrandi |
| Le fichier de sortie est corrompu | Paramètres `JpegOptions` incorrects | Utilisez les options par défaut ou définissez `Quality = 90` |

## Questions fréquentes

**Q : Aspose.Imaging peut‑il gérer d’autres formats que le JPEG ?**  
R : Oui, il prend en charge PNG, BMP, TIFF, GIF et bien d’autres types d’images.

**Q : Existe‑t‑il un moyen de redimensionner l’image avant le recadrage ?**  
R : Vous pouvez utiliser les méthodes `Resize` fournies par la bibliothèque ; cela relève des opérations **resize image java**.

**Q : La bibliothèque prend‑elle en charge le traitement par lots de plusieurs images ?**  
R : Absolument. Parcourez une collection de chemins de fichiers et appliquez les mêmes étapes à chaque image.

**Q : Comment la mise en cache améliore‑t‑elle les performances ?**  
R : `cacheData()` charge l’image en mémoire une fois, évitant les lectures disque répétées pendant la manipulation – c’est l’essence de **cache image java**.

**Q : Où puis‑je trouver des références API plus détaillées ?**  
R : Consultez la documentation officielle **[documentation](https://reference.aspose.com/imaging/java/)** pour une liste complète des classes et méthodes.

## Conclusion
Vous disposez maintenant d’un exemple complet, prêt pour la production, de **comment agrandir une image** et de la recadrer en utilisant Aspose.Imaging pour Java. En tirant parti de la mise en cache, de définitions précises de rectangles et d’options d’enregistrement flexibles, vous pouvez intégrer ce flux de travail dans n’importe quel pipeline de traitement d’image basé sur Java.

Explorez davantage en expérimentant d’autres transformations telles que la rotation, le filigrane ou le redimensionnement par lots. Pour des conseils supplémentaires, consultez la **[documentation](https://reference.aspose.com/imaging/java/)** ou rejoignez la communauté sur le **[forum de support Aspose](https://forum.aspose.com/)**.

---

**Dernière mise à jour :** 2025-12-24  
**Testé avec :** Aspose.Imaging for Java 24.11  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}