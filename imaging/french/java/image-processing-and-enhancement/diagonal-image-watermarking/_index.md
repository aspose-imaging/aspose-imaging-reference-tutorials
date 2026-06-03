---
date: 2026-01-09
description: Apprenez à ajouter un filigrane aux images avec Aspose.Imaging pour Java.
  Ce tutoriel de traitement d'images Java montre, étape par étape, comment créer rapidement
  un filigrane diagonal.
linktitle: Diagonal Image Watermarking
second_title: Aspose.Imaging Java Image Processing API
title: Comment ajouter un filigrane – Filigrane d'image en diagonale (Java)
url: /fr/java/image-processing-and-enhancement/diagonal-image-watermarking/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}

{{< blocks/products/pf/main-container >}}

{{< blocks/products/pf/tutorial-page-section >}}

# Comment ajouter un filigrane – Filigrane d'image diagonal (Java)

If you're looking to **how to add watermark** to your pictures with a stylish diagonal orientation, Aspose.Imaging for Java makes it painless. In this step‑by‑step tutorial we’ll walk through adding a 45‑degree rotated text watermark to a JPG (or any supported) image. You don’t need to be a Java wizard – each block is explained in plain language so you can replicate the result in minutes.

## Réponses rapides
- **Quelle bibliothèque est utilisée ?** Aspose.Imaging for Java  
- **Quel mot‑clé principal est couvert ?** how to add watermark  
- **Formats d’image pris en charge ?** JPEG, PNG, BMP, TIFF, GIF et plus encore  
- **Combien de code est nécessaire ?** Seulement sept blocs de code concis  
- **Ai‑je besoin d’une licence pour les tests ?** Un essai gratuit est disponible ; une licence est requise pour la production  

## Qu’est‑ce que le “how to add watermark” en traitement d’image ?
Ajouter un filigrane signifie superposer du texte ou des graphiques semi‑transparents sur une image afin de protéger la propriété ou de véhiculer une marque. Un filigrane diagonal est particulièrement efficace car il parcourt toute l’image et est plus difficile à recadrer.

## Pourquoi utiliser Aspose.Imaging for Java ?
Aspose.Imaging fournit une API de haut niveau qui abstrait la manipulation de pixels bas‑niveau, prend en charge des dizaines de formats et fonctionne sur n’importe quel runtime Java. Elle vous permet de vous concentrer sur *ce que* vous voulez réaliser — comme ajouter un filigrane diagonal—sans vous soucier des particularités des formats d’image.

## Prérequis

Avant de commencer, assurez‑vous d’avoir les éléments suivants :

1. **Aspose.Imaging for Java** – téléchargez la dernière version depuis le site officiel **[ici](https://releases.aspose.com/imaging/java/)**.  
2. **Environnement de développement Java** – JDK 8+ et votre IDE préféré (IntelliJ, Eclipse, VS Code, etc.).  
3. **Une image à filigraner** – placez un JPG/TIFF/PNG d’exemple dans un dossier que vous référencerez dans le code.

## Importer les packages

First, import the classes you’ll need. Keeping imports together makes the code easier to read and maintain.

```java
import com.aspose.imaging.*;
import com.aspose.imaging.brushes.*;
import com.aspose.imaging.fonts.*;
import com.aspose.imaging.graphics.*;
import com.aspose.imaging.imageoptions.*;
import com.aspose.imaging.text.*;
```

## Étape 1 : Charger une image existante

We start by loading the source picture. The `Image.load` method automatically detects the format.

```java
// The path to the documents directory.
String dataDir = "Your Document Directory" + "ModifyingImages/";

// Load an existing JPG image
try (Image image = Image.load(dataDir + "SampleTiff1.tiff"))
{
    // Rest of the code goes here
}
```

> **Astuce :** Encapsulez l’objet `Image` dans un bloc *try‑with‑resources* (comme montré) afin qu’il soit libéré automatiquement, évitant ainsi les fuites de mémoire.

## Étape 2 : Préparer le texte et les graphiques du filigrane

Create a `Graphics` object linked to the loaded image and store the image size for later calculations.

```java
// Declare a String object with Watermark Text
String theString = "45 Degree Rotated Text";

// Create and initialize an instance of Graphics class
Graphics graphics = new Graphics(image);

// Initialize an object of SizeF to store image Size
Size sz = graphics.getImage().getSize();
```

## Étape 3 : Définir la police et le pinceau

Choose a font that stands out and a brush that defines the watermark’s colour and opacity. Adjust the opacity to make the watermark semi‑transparent.

```java
// Create an instance of Font, initialize it with Font Face, Size, and Style
Font font = new Font("Times New Roman", 20, FontStyle.Bold);

// Create an instance of SolidBrush and set its various properties
SolidBrush brush = new SolidBrush();
brush.setColor(Color.getRed());
brush.setOpacity(0);
```

## Étape 4 : Formater votre texte

Set alignment and formatting flags so the text is centred when drawn.

```java
// Initialize an object of StringFormat class and set its various properties
StringFormat format = new StringFormat();
format.setAlignment(StringAlignment.Center);
format.setFormatFlags(StringFormatFlags.MeasureTrailingSpaces);
```

## Étape 5 : Appliquer la transformation

A transformation matrix lets us move the origin to the centre of the image and then rotate the text by ‑45° (clockwise).

```java
// Create an object of Matrix class for transformation
Matrix matrix = new Matrix();
// First a translation then a rotation
matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);
matrix.rotate(-45.0f);
// Set the Transformation through Matrix
graphics.setTransform(matrix);
```

## Étape 6 : Dessiner et enregistrer

Finally, render the string onto the image and write the result to disk.

```java
// Draw the string on Image
graphics.drawString(theString, font, brush, 0, 0, format);

// Save output to disk
image.save("Your Document Directory" + "AddDiagonalWatermarkToImage_out.jpg");
```

When you open `AddDiagonalWatermarkToImage_out.jpg` you’ll see the red, semi‑transparent text slanted across the centre of the picture.

## Problèmes courants & solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| Le filigrane apparaît trop pâle | Opacité réglée à 0 (complètement transparent) | Augmentez l’opacité, par ex. `brush.setOpacity(0.5f);` |
| Le texte est tronqué aux bords | Translation non centrée pour les images non carrées | Utilisez `matrix.translate(sz.getWidth() / 2f, sz.getHeight() / 2f);` comme indiqué, puis ajustez l’angle de rotation si nécessaire |
| Erreur de format d’image non pris en charge | Utilisation d’une version ancienne d’Aspose.Imaging | Mettez à jour vers la dernière version d’Aspose.Imaging |

## Questions fréquentes

### Q1 : Aspose.Imaging for Java convient‑il aux débutants ?

**R :** Absolument ! L’API est intuitive et la documentation propose des exemples clairs. Même les développeurs novices en traitement d’image peuvent suivre ce tutoriel et obtenir rapidement des résultats professionnels.

### Q2 : Puis‑je personnaliser le texte et le style du filigrane ?

**R :** Oui. Modifiez la variable `theString`, choisissez une autre `Font`, changez `brush.setColor(...)`, ou ajustez l’angle de rotation dans la matrice pour correspondre à votre identité visuelle.

### Q3 : Aspose.Imaging for Java prend‑il en charge d’autres formats d’image que le JPG ?

**R :** Oui. La bibliothèque fonctionne avec BMP, PNG, GIF, TIFF, PSD, et bien d’autres. Il suffit de pointer la méthode `Image.load` vers le fichier approprié.

### Q4 : Existe‑t‑il un essai gratuit d’Aspose.Imaging for Java ?

**R :** Oui, vous pouvez essayer Aspose.Imaging for Java avec un essai gratuit. Obtenez‑le **[ici](https://releases.aspose.com/)**.

### Q5 : Où puis‑je obtenir de l’aide ou du support pour Aspose.Imaging for Java ?

**R :** Pour des questions, des rapports de bugs ou des conseils de bonnes pratiques, rendez‑vous sur le forum de support Aspose.Imaging for Java **[ici](https://forum.aspose.com/)**.

---

**Dernière mise à jour :** 2026-01-09  
**Testé avec :** Aspose.Imaging for Java 24.11 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}