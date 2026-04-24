---
date: 2025-12-20
description: Apprenez à recadrer une image en rectangle et à agrandir une image en
  utilisant Java avec Aspose.Imaging. Guide étape par étape pour les développeurs.
linktitle: Image Expansion or Cropping
second_title: Aspose.Imaging Java Image Processing API
title: Recadrer l'image en rectangle avec Aspose.Imaging pour Java
url: /fr/java/document-conversion-and-processing/image-expansion-or-cropping/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Recadrer une image en rectangle avec Aspose.Imaging pour Java

Dans le monde numérique d'aujourd'hui, où tout évolue rapidement, pouvoir **crop image to rectangle** rapidement et de manière fiable est une exigence fondamentale pour tout flux de travail d'images basé sur Java. Que vous construisiez un service web qui doit recadrer des photos téléchargées par les utilisateurs, générer des vignettes pour un catalogue e‑commerce, ou simplement préparer des ressources pour une campagne marketing, Aspose.Imaging pour Java vous offre une API propre et haute performance pour accomplir la tâche. Dans ce tutoriel, nous allons parcourir à la fois le recadrage d'un rectangle à partir d'une image et l'expansion du canevas d'une image en Java — parfait pour quiconque souhaite maîtriser les techniques **how to crop image java**.

## Réponses rapides
- **Quelle bibliothèque est la meilleure pour le recadrage d'images Java ?** Aspose.Imaging for Java.
- **Puis-je recadrer à un rectangle arbitraire ?** Oui – définissez n'importe quel X, Y, largeur et hauteur.
- **Ai‑je besoin d'une licence pour le développement ?** Un essai gratuit suffit pour les tests ; une licence est requise en production.
- **L'expansion d'une image est‑elle possible ?** Absolument – vous pouvez augmenter la taille du canevas avant le recadrage.
- **Quelle version de Java est prise en charge ?** Java 8 et ultérieure.

## Qu'est‑ce que “crop image to rectangle” ?
Recadrer une image en rectangle signifie extraire une sous‑section du bitmap original définie par une région rectangulaire (décalage X, décalage Y, largeur, hauteur). Le reste de l'image est supprimé, vous laissant avec une nouvelle image plus petite qui ne contient que la zone dont vous avez besoin.

## Pourquoi utiliser Aspose.Imaging pour Java ?
- **Aucune dépendance externe** – Java pur, fonctionne sur n'importe quelle plateforme.
- **Large prise en charge des formats** – JPEG, PNG, BMP, TIFF, et plus.
- **Cache haute performance** – `cacheData()` réduit la surcharge d'E/S.
- **API simple** – appels en une ligne pour charger, définir un rectangle et enregistrer.

## Prérequis
- **Environnement de développement Java** – JDK 8+ installé et configuré.
- **Aspose.Imaging pour Java** – téléchargez depuis le [site web](https://releases.aspose.com/imaging/java/).
- **Connaissances de base en Java** – familiarité avec les classes, try‑with‑resources et les chemins de fichiers.
- **Image à travailler** – tout JPEG/PNG que vous souhaitez recadrer ou agrandir.

## Importation des packages
Tout d'abord, indiquez le code vers le dossier contenant vos images source. Cet extrait reste inchangé par rapport au tutoriel original.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ConvertingImages/";
```

Remplacez `"Your Document Directory"` par le chemin absolu sur votre machine.

## Étape 1 : charger l'image
Charger l'image est la base de toute manipulation. Nous appelons également `cacheData()` pour garder le bitmap en mémoire afin d'accélérer les opérations suivantes.

```java
try (RasterImage rasterImage = (RasterImage) Image.load(dataDir + "aspose-logo.jpg"))
{
    rasterImage.cacheData();
}
```

> **Astuce :** Utilisez un bloc `try‑with‑resources` (comme indiqué) pour garantir que l'image soit automatiquement fermée, évitant les fuites de mémoire.

## Étape 2 : définir la région à recadrer
Ici nous créons un `Rectangle` qui représente la zone exacte que vous souhaitez conserver. Le rectangle peut commencer en dehors des limites originales – Aspose.Imaging élargira automatiquement le canevas (utile pour le scénario **expand image using java**).

```java
// Create an instance of Rectangle class and define X, Y, Width, and Height of the rectangle
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

- **X / Y** – les valeurs négatives déplacent le rectangle vers la gauche/haut, provoquant l'expansion du canevas.
- **Largeur / Hauteur** – taille de la région recadrée.

## Étape 3 : enregistrer l'image recadrée (ou agrandie)
Enfin, écrivez le résultat sur le disque. La méthode `save` prend le chemin de destination, les options de format d'image, et le rectangle que nous avons défini.

```java
rasterImage.save("Your Document Directory" + "Grayscaling_out.jpg", new JpegOptions(), destRect);
```

Le fichier de sortie `Grayscaling_out.jpg` contient maintenant le résultat du **crop image to rectangle**. Si le rectangle dépasse l'image originale, la zone supplémentaire est remplie avec un arrière‑plan par défaut (transparent pour PNG, noir pour JPEG).

## Cas d'utilisation courants
| Scénario | Pourquoi c'est important |
|----------|---------------------------|
| **Génération de vignettes** | Extraire rapidement une région centrale pour une taille cohérente. |
| **Recadrage d'image de profil utilisateur** | Imposer une zone d'avatar carrée ou rectangulaire. |
| **Expansion du canevas avant d'ajouter des filigranes** | Ajouter de l'espace autour d'une image sans déformer l'original. |
| **Traitement par lots de documents numérisés** | Recadrer les marges en une seule passe. |

## Dépannage et astuces
- **L'image ne se charge pas ?** Vérifiez le chemin du fichier et assurez‑vous que le format d'image est pris en charge.
- **Bords noirs inattendus après expansion ?** Définissez une couleur d'arrière‑plan dans `JpegOptions` ou utilisez PNG pour la transparence.
- **Problèmes de performance avec de grandes images ?** Augmentez la taille du tas Java (`-Xmx`) ou traitez les images par lots plus petits.

## Questions fréquemment posées

**Q : Quels formats d'image Aspose.Imaging pour Java prend‑il en charge ?**  
R : JPEG, PNG, BMP, TIFF, GIF, ICO, PSD, et bien d’autres. Consultez la documentation officielle pour la liste complète.

**Q : Puis‑je effectuer d'autres manipulations d'image avec Aspose.Imaging pour Java ?**  
R : Absolument ! Redimensionnement, rotation, filtrage et conversion de format sont tous disponibles.

**Q : Aspose.Imaging pour Java convient‑il aux applications web ?**  
R : Oui. La bibliothèque est thread‑safe et fonctionne bien dans les conteneurs de servlets et les services Spring Boot.

**Q : Comment obtenir du support pour Aspose.Imaging pour Java ?**  
R : Consultez le [forum](https://forum.aspose.com/) pour l'aide communautaire, ou ouvrez un ticket de support avec une licence valide.

**Q : Existe‑t‑il un essai gratuit pour Aspose.Imaging pour Java ?**  
R : Oui, vous pouvez explorer la bibliothèque avec un essai gratuit. Téléchargez‑la depuis [ici](https://releases.aspose.com/).

## Conclusion
Vous avez maintenant appris comment **crop image to rectangle** et même **expand image using Java** avec la puissante API Aspose.Imaging. En maîtrisant ces fondamentaux, vous pouvez créer des pipelines de traitement d'images robustes, améliorer la réactivité de l'UI et fournir un contenu visuel soigné dans n'importe quelle application Java.

---

**Last Updated:** 2025-12-20  
**Tested With:** Aspose.Imaging for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}