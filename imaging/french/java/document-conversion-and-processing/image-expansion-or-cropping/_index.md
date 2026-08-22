---
date: 2026-05-03
description: Apprenez à recadrer une image avec Aspose.Imaging pour Java, y compris
  le recadrage rectangulaire et l'extension du canevas. Guide étape par étape pour
  les développeurs.
keywords:
- how to crop image
- crop and expand image
- aspose imaging crop
- java image processing tutorial
- expand image canvas java
linktitle: Agrandissement ou recadrage d’image
second_title: Aspose.Imaging Java Image Processing API
title: Comment recadrer une image en rectangle avec Aspose.Imaging pour Java
url: /fr/java/document-conversion-and-processing/image-expansion-or-cropping/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Comment recadrer une image en rectangle avec Aspose.Imaging pour Java

Dans le monde numérique d'aujourd'hui, en constante évolution, savoir **comment recadrer une image** rapidement et de manière fiable est une exigence fondamentale pour tout flux de travail d'image basé sur Java. Que vous recadriez des photos téléchargées par les utilisateurs pour un service web, que vous génériez des miniatures cohérentes pour un catalogue e‑commerce, ou que vous prépariez des ressources pour une campagne marketing, Aspose.Imaging pour Java offre une API propre et haute performance pour accomplir la tâche. Dans ce tutoriel, nous parcourrons le recadrage d'un rectangle à partir d'une image et l'extension d'un canevas d'image — parfait pour quiconque souhaite maîtriser les techniques de traitement d'image en Java.

## Réponses rapides
- **Quelle bibliothèque est la meilleure pour le recadrage d'image Java ?** Aspose.Imaging for Java.  
- **Puis-je recadrer à un rectangle arbitraire ?** Oui – définissez n'importe quel X, Y, largeur et hauteur.  
- **Ai‑je besoin d'une licence pour le développement ?** Un essai gratuit suffit pour les tests ; une licence est requise pour la production.  
- **L'extension d'une image est‑elle possible ?** Absolument – vous pouvez augmenter la taille du canevas avant le recadrage.  
- **Quelle version de Java est prise en charge ?** Java 8 et ultérieure.

## Qu’est‑ce que « recadrer une image en rectangle » ?
Recadrer une image en rectangle signifie extraire une sous‑section du bitmap original définie par une région rectangulaire (décalage X, décalage Y, largeur, hauteur). Le reste de l'image est supprimé, vous laissant une nouvelle image plus petite contenant uniquement la zone souhaitée.

## Pourquoi utiliser Aspose.Imaging pour Java ?
- **Aucune dépendance externe** – Java pur, fonctionne sur n'importe quelle plateforme.  
- **Large prise en charge des formats** – JPEG, PNG, BMP, TIFF, et plus.  
- **Cache haute performance** – `cacheData()` réduit la surcharge d'E/S.  
- **API simple** – appels en une ligne pour charger, définir un rectangle et enregistrer.

## Prérequis
- **Environnement de développement Java** – JDK 8+ installé et configuré.  
- **Aspose.Imaging pour Java** – téléchargez depuis le [site web](https://releases.aspose.com/imaging/java/).  
- **Connaissances de base en Java** – familiarité avec les classes, try‑with‑resources et les chemins de fichiers.  
- **Image à travailler** – tout JPEG/PNG que vous souhaitez recadrer ou étendre.

## Importation des packages
Tout d'abord, pointez le code vers le dossier contenant vos images sources. Cet extrait reste inchangé par rapport au tutoriel original.

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

> **Astuce :** Utilisez un bloc `try‑with‑resources` (comme indiqué) pour garantir que l'image soit automatiquement fermée, évitant ainsi les fuites de mémoire.

## Étape 2 : définir la région de recadrage
Ici, nous créons un `Rectangle` qui représente la zone exacte que vous souhaitez conserver. Le rectangle peut commencer en dehors des limites originales – Aspose.Imaging étendra automatiquement le canevas (utile pour le scénario **expand image canvas java**).

```java
// Create an instance of Rectangle class and define X, Y, Width, and Height of the rectangle
Rectangle destRect = new Rectangle(-200, -200, 300, 300);
```

- **X / Y** – les valeurs négatives déplacent le rectangle vers la gauche/haut, entraînant l'expansion du canevas.  
- **Largeur / Hauteur** – taille de la région recadrée.

## Étape 3 : enregistrer l'image recadrée (ou étendue)
Enfin, écrivez le résultat sur le disque. La méthode `save` prend le chemin de destination, les options de format d'image, et le rectangle que nous avons défini.

```java
rasterImage.save("Your Document Directory" + "Grayscaling_out.jpg", new JpegOptions(), destRect);
```

Le fichier de sortie `Grayscaling_out.jpg` contient maintenant le résultat du **crop image to rectangle**. Si le rectangle dépasse l'image originale, la zone supplémentaire est remplie avec un arrière‑plan par défaut (transparent pour PNG, noir pour JPEG).

## Comment recadrer une image avec Aspose.Imaging pour Java
Cette section réitère les étapes essentielles sous forme de liste concise afin que vous puissiez les consulter rapidement lors du codage :

1. **Définir le répertoire de données** – pointez vers le dossier contenant les images sources.  
2. **Charger l'image** avec `Image.load()` et appelez `cacheData()`.  
3. **Créer un `Rectangle`** qui définit la région de recadrage (ou l'expansion du canevas).  
4. **Enregistrer** la nouvelle image en utilisant `rasterImage.save()` et en passant le rectangle.

## Recadrer et étendre l'image – cas d'utilisation réels
| Scénario | Pourquoi c'est important |
|----------|---------------------------|
| **Génération de miniatures** | Extraire rapidement une zone centrale pour une taille cohérente. |
| **Recadrage de photo de profil utilisateur** | Imposer une zone d'avatar carrée ou rectangulaire. |
| **Expansion du canevas avant d'ajouter des filigranes** | Ajouter de l'espace autour d'une image sans déformer l'original. |
| **Traitement par lots de documents numérisés** | Recadrer les marges en une seule passe. |

## Dépannage et astuces
- **L'image ne charge pas ?** Vérifiez le chemin du fichier et assurez‑vous que le format d'image est pris en charge.  
- **Bords noirs inattendus après expansion ?** Définissez une couleur d'arrière‑plan dans `JpegOptions` ou utilisez PNG pour la transparence.  
- **Problèmes de performance avec de grandes images ?** Augmentez la taille du tas Java (`-Xmx`) ou traitez les images par lots plus petits.  
- **Erreur courante :** Oublier d'appeler `cacheData()` peut entraîner un I/O plus lent lors des opérations suivantes.

## Questions fréquemment posées

**Q : Quels formats d'image Aspose.Imaging pour Java prend‑il en charge ?**  
R : JPEG, PNG, BMP, TIFF, GIF, ICO, PSD, et bien d'autres. Consultez la documentation officielle pour la liste complète.

**Q : Puis‑je effectuer d'autres manipulations d'image avec Aspose.Imaging pour Java ?**  
R : Absolument ! Redimensionnement, rotation, filtrage et conversion de format sont tous disponibles.

**Q : Aspose.Imaging pour Java est‑il adapté aux applications web ?**  
R : Oui. La bibliothèque est thread‑safe et fonctionne bien dans les conteneurs de servlets et les services Spring Boot.

**Q : Comment obtenir du support pour Aspose.Imaging pour Java ?**  
R : Consultez le [forum](https://forum.aspose.com/) pour l'aide de la communauté, ou ouvrez un ticket de support avec une licence valide.

**Q : Existe‑t‑il un essai gratuit disponible pour Aspose.Imaging pour Java ?**  
R : Oui, vous pouvez explorer la bibliothèque avec un essai gratuit. Téléchargez‑la depuis [ici](https://releases.aspose.com/).

## Conclusion
Vous avez maintenant appris **comment recadrer une image** en rectangle et même **étendre le canevas d'image** en utilisant l'API puissante d'Aspose.Imaging. En maîtrisant ces fondamentaux, vous pouvez créer des pipelines de traitement d'image robustes, améliorer la réactivité de l'interface utilisateur et fournir un contenu visuel soigné dans toute application Java.

---

**Dernière mise à jour :** 2026-05-03  
**Testé avec :** Aspose.Imaging for Java 24.11 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}