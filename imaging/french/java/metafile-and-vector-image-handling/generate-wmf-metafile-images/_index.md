---
"description": "Apprenez à créer des images de métafichiers WMF en Java avec Aspose.Imaging. Suivez ce guide étape par étape pour bénéficier de puissantes fonctionnalités de génération d'images."
"linktitle": "Générer des images de métafichier WMF"
"second_title": "API de traitement d'images Java Aspose.Imaging"
"title": "Création d'images WMF avec Aspose.Imaging pour Java"
"url": "/fr/java/metafile-and-vector-image-handling/generate-wmf-metafile-images/"
"weight": 10
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Création d'images WMF avec Aspose.Imaging pour Java

Vous souhaitez créer des images WMF (métafichiers Windows) avec vos applications Java ? Aspose.Imaging pour Java est un outil puissant qui vous permet de générer facilement des images WMF. Dans ce guide étape par étape, nous vous expliquerons comment utiliser Aspose.Imaging pour Java pour créer des images métafichiers WMF. 

## Prérequis

Avant de commencer, assurez-vous de disposer des prérequis suivants :

- Un environnement de développement Java configuré sur votre ordinateur.
- Bibliothèque Aspose.Imaging pour Java installée. Vous pouvez la télécharger depuis le [site web](https://releases.aspose.com/imaging/java/).
- Connaissances de base de la programmation Java.

## Importer des packages

Tout d’abord, importez les packages nécessaires à votre application Java pour utiliser Aspose.Imaging pour Java :

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.color.*;
import com.aspose.imaging.coreexceptions.ImageLoadException;
import com.aspose.imaging.imageoptions.WmfOptions;
import com.aspose.imaging.internal.system.drawing.*;
import com.aspose.imaging.internal.system.drawing.imaging.*;
import com.aspose.imaging.pen.*;
import com.aspose.imaging.system.drawing.*;
```

## Étape 1 : Créer un canevas

Pour commencer à créer votre image WMF, vous devez créer une toile sur laquelle vous pouvez dessiner des formes. `WmfRecorderGraphics2D` La classe vous fournit ce canevas. Voici comment en créer une instance :

```java
// Le chemin vers le répertoire des documents.
String dataDir = "Your Document Directory" + "ModifyingImages/";
WmfRecorderGraphics2D graphics = new WmfRecorderGraphics2D(new Rectangle(0, 0, 100, 100), 96);
```

Dans le code ci-dessus, nous spécifions les dimensions de la toile (100x100) et la résolution (96 DPI).

## Étape 2 : Définir la couleur d’arrière-plan

Ensuite, définissez la couleur d'arrière-plan de votre toile. Vous pouvez utiliser l'outil `setBackgroundColor` méthode pour définir la couleur d'arrière-plan :

```java
graphics.setBackgroundColor(Color.getWhiteSmoke());
```

Dans cet exemple, nous définissons la couleur d’arrière-plan sur fumée blanche.

## Étape 3 : Définir le stylo et le pinceau

Pour dessiner des formes sur la zone de travail, vous devez définir un stylo et un pinceau. Le stylo sert à tracer les contours, tandis que le pinceau sert à remplir les formes. Voici comment créer un stylo et un pinceau uni :

```java
Pen pen = new Pen(Color.getBlue());
Brush brush = new SolidBrush(Color.getYellowGreen());
```

Dans ce code, nous créons un stylo bleu et un pinceau solide jaune-vert.

## Étape 4 : Remplissez et dessinez des formes

Maintenant, remplissons et dessinons quelques formes simples sur la toile. Commençons par un polygone :

```java
graphics.fillPolygon(brush, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
graphics.drawPolygon(pen, new Point[] { new Point(2, 2), new Point(20, 20), new Point(20, 2) });
```

Ici, nous remplissons et dessinons un polygone à l'aide du stylo et du pinceau spécifiés. Vous pouvez ajuster les coordonnées et les formes selon vos besoins.

## Étape 5 : Utiliser HatchBrush

Pour ajouter des textures à vos formes, vous pouvez utiliser un `HatchBrush`. Par exemple:

```java
HatchBrush hatchBrush = new HatchBrush();
hatchBrush.setHatchStyle(HatchStyle.Cross);
hatchBrush.setBackgroundColor(Color.getWhite());
hatchBrush.setForegroundColor(Color.getSilver());
brush = hatchBrush;
```

Dans ce code, nous créons un pinceau hachuré avec des couleurs blanches et argentées.

## Étape 6 : Remplissez et dessinez l'ellipse

Remplissons et dessinons une ellipse sur la toile :

```java
graphics.fillEllipse(brush, new Rectangle(25, 2, 20, 20));
graphics.drawEllipse(pen, new Rectangle(25, 2, 20, 20));
```

Vous pouvez ajuster la position et la taille de l'ellipse selon vos besoins.

## Étape 7 : Dessiner un arc et une courbe de Bézier cubique

Il est également possible de dessiner des formes plus complexes. Voici comment dessiner un arc et une courbe de Bézier cubique :

```java
pen.setDashStyle(DashStyle.Dot);
pen.setColor(Color.getBlack());
graphics.drawArc(pen, new Rectangle(50, 2, 20, 20), 0, 180);

pen.setDashStyle(DashStyle.Solid);
pen.setColor(Color.getRed());
graphics.drawCubicBezier(pen, new Point(10, 25), new Point(20, 50), new Point(30, 50), new Point(40, 25));
```

Dans le code ci-dessus, nous dessinons d’abord un arc avec un style de ligne pointillée, puis nous dessinons une courbe de Bézier cubique avec un stylo rouge uni.

## Étape 8 : Ajouter des images

Vous pouvez également ajouter des images à votre métafichier WMF. Voici comment procéder :

```java
try (RasterImage rasterImage = (RasterImage)Image.load(dataDir + "WaterMark.bmp"))
{
    graphics.drawImage(rasterImage, new Point(50, 50));
}
```

Dans cette étape, nous chargeons une image et la plaçons sur le canevas aux coordonnées spécifiées (50, 50).

## Étape 9 : Tracez des lignes et des secteurs

Pour ajouter des lignes et des formes de tarte, vous pouvez suivre ces exemples :

```java
graphics.drawLine(pen, new Point(2, 98), new Point(2, 50));

brush = new SolidBrush(Color.getGreen());
pen.setColor(Color.getDarkGoldenrod());

graphics.fillPie(brush, new Rectangle(2, 38, 20, 20), 0, 45);
graphics.drawPie(pen, new Rectangle(2, 38, 20, 20), 0, 45);
```

Ici, nous dessinons une ligne et remplissons/dessinons une forme de tarte à l'aide du stylo et du pinceau spécifiés.

## Étape 10 : Dessiner une polyligne et du texte

L'ajout de texte et de polylignes est simple :

```java
graphics.drawPolyline(pen, new Point[] { new Point(50, 40), new Point(75, 40), new Point(75, 45), new Point(50, 45) });

Font font = new Font("Arial", 16);
graphics.drawString("Aspose", font, Color.getBlue(), 25, 75);
```

Vous pouvez personnaliser la police, le texte et les points de polyligne selon vos besoins.

## Étape 11 : Enregistrer l'image WMF

Une fois que vous avez créé votre image WMF, il est temps de l'enregistrer :

```java
try (WmfImage image = graphics.endRecording())
{
    image.save("Your Document Directory" + "CreateWMFMetaFileImage.wmf");
}
```

Ce code enregistrera l'image WMF dans le répertoire spécifié.

Et voilà ! Vous avez généré avec succès une image de métafichier WMF avec Aspose.Imaging pour Java.

## Conclusion

Dans ce tutoriel, nous avons découvert comment créer des images de métafichiers WMF avec Aspose.Imaging pour Java. Nous avons abordé les prérequis nécessaires, importé des packages et fourni des instructions étape par étape pour dessiner différentes formes, ajouter des textures, insérer des images et enregistrer l'image finale. Aspose.Imaging pour Java offre un ensemble puissant d'outils pour la manipulation et la création d'images, ce qui en fait une ressource précieuse pour vos applications Java.

## FAQ

### Q1 : Qu'est-ce qu'un format d'image WMF ?

A1 : WMF signifie Windows Metafile, un format graphique vectoriel utilisé pour stocker des images, des dessins et d'autres données graphiques. Il est couramment utilisé dans les applications Windows et peut être facilement mis à l'échelle sans perte de qualité.

### Q2 : Où puis-je télécharger Aspose.Imaging pour Java ?

A2 : Vous pouvez télécharger Aspose.Imaging pour Java à partir du [site web](https://releases.aspose.com/imaging/java/).

### Q3 : Ai-je besoin de compétences avancées en programmation pour utiliser Aspose.Imaging pour Java ?

A3 : Bien que des connaissances de base en programmation Java soient requises, Aspose.Imaging pour Java fournit une API conviviale qui simplifie les tâches de manipulation et de création d'images.

### Q4 : Puis-je utiliser Aspose.Imaging pour Java à des fins commerciales ?

A4 : Oui, Aspose.Imaging pour Java propose des licences commerciales pour les entreprises et les développeurs. Vous pouvez acheter une licence auprès de [ici](https://purchase.aspose.com/buy).

### Q5 : Où puis-je obtenir de l’aide ou poser des questions sur Aspose.Imaging pour Java ?

A5 : Vous pouvez trouver du soutien et interagir avec la communauté Aspose sur le [Forums Aspose.Imaging](https://forum.aspose.com/).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}